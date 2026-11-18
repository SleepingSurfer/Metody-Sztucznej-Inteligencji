# Sprawozdanie – laboratorium 1

**Repozytorium:** [SleepingSurfer/Metody-Sztucznej-Inteligencji](https://github.com/SleepingSurfer/Metody-Sztucznej-Inteligencji)

- **Aplikacja:** Codex (aplikacja komputerowa na Windows)
- **Model:** GPT-6.2 Sol
- **Poziom rozumowania:** High
- **Zmiany ustawień:** Brak zgłoszonych zmian.

[Polecenie laboratorium](https://agents-ml-course-2026.czuba-przemyslaw.chatgpt.site/lab-1)

## 1. Cel zadania i dopuszczalne zmiany

**Zlecony wynik.** Wygenerowanie raportu z liczebnością etykiet `ham` i `spam` dla `project/data/exercise.csv`, uruchomienie gotowego testu, a następnie uzyskanie aktualnego wyniku po zmianie jednej etykiety.

**Dozwolone zmiany.** W etapie 1 zakres obejmował rozpakowanie projektu, uruchomienie skryptu i testu oraz zapis raportu. Kod, dane i testy miały pozostać bez zmian. W etapie 2 można było zmienić tylko etykietę jednego rekordu, a później ponownie wygenerować raport.

**Informacje wymagane do odbioru.** Użyte polecenie, wersja Pythona, katalog roboczy, ścieżka wejścia i wyjścia, wynik procesu, treść wygenerowanego JSON-a, wynik testu wraz z informacją o błędach oraz identyfikator rekordu i obie etykiety w etapie 2.

## 2. Proces generowania raportu

- **Dane wejściowe.** `project/data/exercise.csv` z paczki do ćwiczenia. Na przykładzie `exercise-001` identyfikator `message_id` łączy rekord z plikiem `.eml`, `text` przechowuje temat i treść wiadomości, a `label` zawiera przypisaną kategorię.
- **Narzędzie i środowisko.** `describe_data.py`, PowerShell i Python 3.14.0 na lokalnym komputerze z Windows. Katalog roboczy procesu to `D:\MSI\lab1\project`.
- **Przebieg.** Agent odczytał `project/README.md` oraz `project/data/README.md`. Model wybrał polecenie, Codex przekazał je narzędziu terminalowemu, lokalny Python wykonał skrypt, a komunikaty i kod wyjścia wróciły do sesji. Launcher `py` nie wykrył interpretera, więc użyto pełnej ścieżki do `python.exe`.

Polecenie wykonane w etapie 1 z katalogu `project/`:

```powershell
& 'C:\Users\kamil\AppData\Local\Programs\Python\Python314\python.exe' describe_data.py --data data/exercise.csv --out results/exercise-summary.json
```

**Wynik.** Proces zwrócił kod `0` i podał miejsce zapisu. Odczytany JSON wskazał w polu `input_file` ścieżkę `D:\MSI\lab1\project\data\exercise.csv`. Pierwszy raport zawierał 8 rekordów, w tym 5 `ham` i 3 `spam`. Liczebności potwierdzono niezależnym odczytem CSV w PowerShellu, a `input_sha256` był zgodny z wynikiem `Get-FileHash` i sumą z `data/manifest.json`.

**Raport końcowy po zmianie etykiety.** [exercise-summary.json](exercise-summary.json)

| Pole w raporcie końcowym | Liczebność | Wyjaśnienie |
| --- | ---: | --- |
| `total_messages` | 8 | Liczba rekordów CSV. Treść jednej wiadomości może zajmować kilka linii. |
| `label_counts.ham` | 4 | Liczba rekordów z przypisaną etykietą `ham`. |
| `label_counts.spam` | 4 | Liczba rekordów z przypisaną etykietą `spam`. |

Skrypt zlicza etykiety odczytane z CSV. Zmiana etykiety jednego rekordu przeniosła go z jednej kategorii do drugiej, więc suma pozostała równa 8.

## 3. Analiza fragmentu kodu

**Analizowany fragment.** `project/describe_data.py`, funkcja `describe()`, linie 14 i 36. Zapis JSON następuje w funkcji `main()`, linie 55–60.

**Ustalenia z analizy.** `read_bytes()` wczytuje bajty CSV. Standardowy moduł `hashlib` oblicza z nich SHA-256, a `hexdigest()` zwraca go jako 64 znaki szesnastkowe. Skrypt umieszcza ten tekst w polu `input_sha256` przed zapisaniem JSON-a. Zestawienie skrótów pozwala porównać wersje pliku nawet przy identycznej ścieżce wejściowej. [Dokumentacja `hashlib`](https://docs.python.org/3/library/hashlib.html)

**Własne wyjaśnienie.** SHA-256 pozwala mi sprawdzić, z której wersji CSV powstał raport. Sama ścieżka mogła pozostać taka sama po poprawieniu etykiety, więc porównałem skrót zapisany w raporcie ze skrótem aktualnego pliku. Stary skrót zgadzał się z sumą w manifeście, a nowy z plikiem po edycji. To sprawdzenie dotyczy zgodności zawartości pliku. Poprawność etykiet trzeba ocenić osobno.

**Mały przypadek sprawdzający.** Wyobraź sobie dwa poprawne pliki CSV o identycznej zawartości bajtowej. Jeden nazywa się `a.csv`, a drugi `b.csv`. Skrypt otrzymuje je kolejno jako wejście.

- **Przewidywanie:** Pole `input_file` będzie się różnić, ponieważ pełna ścieżka zawiera nazwę pliku. SHA-256 zostanie taki sam, bo skrypt oblicza go z zawartości. Liczby wiadomości `ham` i `spam` też będą takie same, bo skrypt odczyta te same etykiety.
- **Weryfikacja:** Po zapisaniu przewidywania agent wywołał funkcję `describe()` dwa razy w pamięci. W obu próbach przekazał te same bajty CSV z dwiema wiadomościami (jedną `ham` i jedną `spam`), a ścieżki kończyły się na `a.csv` i `b.csv`.
- **Wynik i wniosek:** Przewidywanie się potwierdziło. Pole `input_file` wskazało inną nazwę w każdym wyniku. Oba wyniki miały identyczny skrót `fe800d50c6e4db8d345f112b1e3f8c06fa31d15973c8dd3813683f4f478bb6e0` i zawierały po 2 wiadomości (1 `ham` i 1 `spam`).

## 4. Uruchomienie gotowego testu

**Nazwa testu.** `test_cli_writes_expected_counts` w `project/tests/test_report.py`.

**Sposób uruchomienia.** Pierwsza próba zwróciła błąd zapisu w domyślnym katalogu tymczasowym. Przy drugiej próbie wskazano katalog tymczasowy dostępny z poziomu projektu i powtórzono to samo polecenie:

```powershell
$env:TMPDIR = 'D:\MSI\lab1\project\results'
& 'C:\Users\kamil\AppData\Local\Programs\Python\Python314\python.exe' -B -m unittest discover -s tests -v
```

**Wynik testu.** `Ran 1 test`, `OK`, kod wyjścia `0`.

**Zakres sprawdzenia.** Test uruchamia skrypt na trzech syntetycznych wiadomościach o wielowierszowej treści z `project/tests/fixtures/messages.csv`. Sprawdza kod wyjścia, powstanie i odczyt raportu JSON, zgodność `input_file` z plikiem testowym oraz oczekiwane liczebności `3`, `2 ham` i `1 spam`.

**Własne wyjaśnienie zakresu.** Z wyniku testu wiem, że dla trzech przykładowych wiadomości skrypt zapisał raport dla właściwego pliku i poprawnie policzył dwie etykiety `ham` i jedną `spam`, mimo że treść wiadomości zajmowała kilka linii. Raport dla `exercise.csv` sprawdziłem osobno przez porównanie ścieżki, liczebności i SHA-256 z danymi ćwiczeniowymi.

## 5. Etap 2 – zmiana etykiety

**Wprowadzona zmiana.** W `project/data/exercise.csv` zmieniono etykietę rekordu `exercise-001` z `ham` na `spam`. W czasie edycji sprawdzono, że zmieniło się wyłącznie to pole.

**Przewidywany efekt.** Zakładałem, że po edycji stary raport przestanie odpowiadać aktualnemu CSV. W nowym raporcie spodziewałem się o jedną wiadomość mniej w kategorii `ham` i o jedną więcej w kategorii `spam` względem starego raportu. Łączna liczba wiadomości miała pozostać taka sama, bo zmieniła się tylko etykieta jednego rekordu.

**Wykonane operacje i ich cel.**

1. Zmieniono jedną etykietę, żeby zasymulować zmianę danych wejściowych.
2. Ponownie uruchomiono generator na tym samym CSV. Użyto osobnego pliku wyjściowego, aby mieć dostęp do obu wyników. Proces zakończył się kodem `0`.
3. Odczytano nowy JSON, potwierdzono `input_file` oraz niezależnie porównano liczbę rekordów, etykiety i SHA-256 z aktualnym CSV. Ścieżka wejścia była taka sama w obu raportach, a skrót zmienił się z `95e9049f…` na `7dc8080d…`.

```powershell
& 'C:\Users\kamil\AppData\Local\Programs\Python\Python314\python.exe' describe_data.py --data data/exercise.csv --out results/exercise-summary-after-label-change.json
```

| Wskaźnik | Przed zmianą | Po zmianie | Różnica |
| --- | ---: | ---: | ---: |
| `ham` | 5 | 4 | −1 |
| `spam` | 3 | 4 | +1 |
| Suma rekordów | 8 | 8 | 0 |

**Wniosek.** Wynik potwierdził moje przewidywanie. Stary raport pokazywał 5 `ham` i 3 `spam`, a po ponownym uruchomieniu skrypt zapisał 4 `ham` i 4 `spam`. Oba raporty zawierały łącznie 8 wiadomości. SHA-256 z nowego raportu zgadzał się z aktualnym CSV, a skrót ze starego odpowiadał pierwotnej wersji zapisanej w manifeście.

**Potwierdzenie w sesjach.** W [zapisie głównej sesji](sesje/01-sesja-laboratorium.md) są widoczne polecenia, kody wyjścia i oba odczytane raporty JSON. Wersje plików można też porównać bezpośrednio: [przed zmianą](exercise-summary-before-label-change.json) i [po zmianie](exercise-summary.json).

## Załączniki

**Zapis sesji.** [01 – wykonanie laboratorium](sesje/01-sesja-laboratorium.md). To zapis Markdown przygotowany z historii Codexa, obejmujący główną rozmowę oraz polecenia i wyniki ćwiczenia, w tym nieudane próby.

**Commit z plikami oddania.** [6ea93ec – pliki laboratorium 1](https://github.com/SleepingSurfer/Metody-Sztucznej-Inteligencji/commit/6ea93ec3083ca2542bd03d689b1c5680d1feeccd).
