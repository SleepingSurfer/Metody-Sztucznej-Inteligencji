# Sesja 2 – sprawozdanie i mały przypadek

Zapis Markdown sporządzony z historii Codexa. Obejmuje wiadomości rozmowy oraz polecenia i wyniki związane z wykonaniem ćwiczenia. Pominięto metadane aplikacji i techniczne odczyty niezwiązane z wykonaniem skryptu.

## 18.11.2026, 22:15:47 · Student

# Sprawozdanie – laboratorium 1

**Repozytorium:** [link do repozytorium](https://github.com/UZYTKOWNIK/REPOZYTORIUM)

**Aplikacja:** [nazwa aplikacji]\
**Model:** [dokładna nazwa modelu widoczna w aplikacji]\
**Poziom rozumowania:** [poziom lub „niedostępny”]\
**Zmiany ustawień:** [brak / użyte modele i poziomy]

## 1. Cel zadania i dopuszczalne zmiany

**Zlecony wynik:**\
[Opisz, co należało uzyskać w zadaniu.]

**Dozwolone zmiany:**\
[Wymień, co agent mógł modyfikować, a czego nie.]

**Informacje wymagane do odbioru:**\
[Wymień, o jakie wyniki, potwierdzenia i pliki poproszono agenta.]

## 2. Proces generowania raportu

- **Dane wejściowe:** [pliki i ich lokalizacja].
- **Polecenie:** [polecenie wydane agentowi lub użyta komenda].
- **Narzędzie:** [użyty skrypt, program lub funkcja].
- **Środowisko:** [system, terminal, katalog roboczy].
- **Przebieg:** [krótki opis wykonanych czynności].
- **Wynik:** [czy wygenerowano raport i jak to potwierdzono].

**Raport końcowy:** [exercise-summary.json](https://github.com/UZYTKOWNIK/REPOZYTORIUM/blob/main/lab1/exercise-summary.json)

**Interpretacja liczebności:**

| Pole w raporcie | Liczebność | Wyjaśnienie       |
| --------------- | ---------- | ----------------- |
| [pole 1]        | [n]        | [co jest liczone] |
| [pole 2]        | [n]        | [co jest liczone] |
| [pole 3]        | [n]        | [co jest liczone] |

[Wyjaśnij, dlaczego otrzymano takie liczebności. Dostosuj tabelę do rzeczywistej struktury raportu.]

## 3. Analiza fragmentu dokumentacji lub kodu

**Analizowany fragment:**\
[Ścieżka pliku, nazwa funkcji lub sekcji, numery linii.]

**Własne wyjaśnienie:**\
[Opisz własnymi słowami, jak działa wybrany fragment.]

**Mały przypadek sprawdzający:**

- **Przykład:** [proste dane wejściowe].
- **Przewidywanie:** [jakiego wyniku oczekiwano i dlaczego].
- **Weryfikacja:** [jak sprawdzono przewidywanie].
- **Wynik:** [co otrzymano].
- **Wniosek:** [czy przewidywanie zostało potwierdzone].

## 4. Uruchomienie gotowego testu

**Nazwa testu:** [nazwa lub ścieżka].

**Sposób uruchomienia:** [komenda lub wykonane kroki].

**Wynik testu:** [zaliczony/niezaliczony, komunikat].

**Zakres sprawdzenia:**\
[Wyjaśnij, co dokładnie weryfikował test.]

## 5. Etap 2 – zmiana etykiety

**Wprowadzona zmiana:**\
Zmieniono etykietę `[stara etykieta]` na `[nowa etykieta]` w [nazwa pliku / rekordu].

**Przewidywany efekt:**\
[Opisz, które liczebności powinny ulec zmianie, o ile i dlaczego.]

**Wybrane operacje:**\
[Wymień operacje konieczne do uzyskania i potwierdzenia aktualnego wyniku, np. zmianę danych, ponowne uruchomienie generatora raportu i kontrolę wyniku. Wyjaśnij, dlaczego każda była potrzebna.]

**Porównanie wyników:**

| Wskaźnik         | Przed zmianą | Po zmianie | Różnica |
| ---------------- | ------------ | ---------- | ------- |
| [stara etykieta] | [n]          | [n]        | [±n]    |
| [nowa etykieta]  | [n]          | [n]        | [±n]    |
| [suma rekordów]  | [n]          | [n]        | [±n]    |

**Wniosek:**\
[Porównaj otrzymany wynik z przewidywaniem. Wyjaśnij, czy ponowne wykonanie procesu poprawnie uwzględniło zmodyfikowane dane.]

**Potwierdzenie w sesjach:**\
[Wskaż zapis sesji, w którym widoczne są raporty przed zmianą i po zmianie.]

## Załączniki

**Pełne zapisy sesji:** [folder sesje/](https://github.com/UZYTKOWNIK/REPOZYTORIUM/tree/main/lab1/sesje).

W folderze znajdują się wszystkie sesje w kolejności chronologicznej, w oryginalnym formacie eksportu aplikacji, łącznie z nieudanymi próbami.

**Commit końcowy:** [link do konkretnego commita].

uzupełnij sprawozdanie, w miejscach gdzie ja mam się wyrazić to zaznacz i zapytaj mnie o odpowiedź

## 18.11.2026, 22:16:15 · Student

[https://agents-ml-course-2026.czuba-przemyslaw.chatgpt.site/lab-1](https://agents-ml-course-2026.czuba-przemyslaw.chatgpt.site/lab-1) tutaj polecenie

## 18.11.2026, 22:16:19 · Codex

Sprawdzę polecenie z linku i uzupełnię `lab1/sprawozdanie.md` na podstawie wyników z sesji. Zaznaczę miejsca, które wymagają Twojej odpowiedzi.

## 18.11.2026, 22:16:57 · Codex

Do uzupełnienia Twoim głosem zostawię dwa miejsca. **1. Jaką nazwę modelu i poziom rozumowania widziałeś w aplikacji podczas laboratorium? Czy zmieniałeś te ustawienia?** Jeśli poziom nie był widoczny, wpisz „niedostępny”. **2. Jak własnymi słowami wyjaśnisz, po co w raporcie zapisano SHA-256 i skąd wiadomo, że po zmianie etykiety stary raport był nieaktualny?** Wystarczą 1–2 zdania.

## 18.11.2026, 22:19:31 · Codex

**Mały przypadek z polecenia:** wyobraź sobie dwa CSV o identycznych bajtach, o nazwach `a.csv` i `b.csv`. Co według Ciebie zmieni się między raportami w `input_file`, `input_sha256` i liczebnościach? Sprawdzę to po Twojej odpowiedzi. **Dopisz też krótko:** co potwierdził gotowy test i jakiej zmiany liczebności oczekiwałeś po zmianie etykiety w etapie 2? Jeśli tego przewidywania nie zapisałeś przed uruchomieniem, zaznacz to.

## 18.11.2026, 22:19:58 · Codex

Uzupełniłem [sprawozdanie z laboratorium 1](D:/MSI/lab1/sprawozdanie.md) zgodnie z [poleceniem](https://agents-ml-course-2026.czuba-przemyslaw.chatgpt.site/lab-1). Wpisałem rzeczywiste komendy, wynik testu i porównanie raportów przed zmianą etykiety i po niej. Miejsca na Twoje odpowiedzi oznaczyłem **DO UZUPEŁNIENIA**.

Odpowiedz proszę krótko, nawet po jednym zdaniu:

1. **Ustawienia.** Jaką dokładną nazwę modelu i poziom rozumowania widziałeś w Codexie? Czy zmieniałeś te ustawienia? Jeśli poziom był niewidoczny, wpisz „niedostępny”.
2. **SHA-256.** Po co Twoim zdaniem zapisujemy skrót pliku w raporcie? Gdyby dwa CSV miały identyczną zawartość, ale nazwy `a.csv` i `b.csv`, co według Ciebie zmieniłoby się w `input_file`, `input_sha256` i liczebnościach? Sprawdzę to po Twojej odpowiedzi.
3. **Test.** Co potwierdził gotowy test i co trzeba było osobno zweryfikować dla `exercise.csv`?
4. **Zmiana etykiety.** Jakiej zmiany liczby `ham`, `spam` i wszystkich wiadomości oczekiwałeś przed ponownym uruchomieniem? Jeśli nie zapisałeś wtedy przewidywania, opisz to jako wniosek po wykonaniu.

Do oddania pozostają pełne eksporty sesji i link do końcowego commita. Sprawozdanie linkuje do aktualnego wyniku pod nazwą `exercise-summary-after-label-change.json`; polecenie wskazuje dla pliku końcowego nazwę `exercise-summary.json`.

## 18.11.2026, 22:21:18 · Student

uzupełnij moje pola chyba że nadal coś nie będzie jasne to zadaj kilka pytań:
Hej chat połącz się z moim githubem https://github.com/SleepingSurfer/Metody-Sztucznej-Inteligencji.git

4 lis, 8:26
Połączyłem folder MSI z Twoim repozytorium jako origin. Repozytorium jest obecnie puste — nie ma jeszcze commitów.

Aby połączyć także konto GitHub w aplikacji, zainstaluj integrację GitHub i autoryzuj dostęp.

4 lis, 8:27
Połączenie działa — konto SleepingSurfer jest połączone, a dostęp do repozytorium obejmuje odczyt i zapis.

Repozytorium jest puste i sklonowane lokalnie do D:\MSI.

4 lis, 8:30
utwórz podfoldery zgodnie z taką strukturą: repozytorium/
├── lab1/
│   ├── sprawozdanie.md
│   └── sesje/
├── lab2/
│   ├── sprawozdanie.md
│   └── sesje/
└── …

4 lis, 8:33
Utworzyłem i wysłałem na GitHub foldery lab1 i lab2. Każdy zawiera pusty sprawozdanie.md oraz katalog sesje/ z plikiem .gitkeep.

Zmiany są też lokalnie w D:\MSI.

4 lis, 8:34

lab-1-project.zip
W pliku znajduje się projekt. Zapoznaj się z strukturą dokumentów. Sprawdź plik describe_data.py i powiedz jakie dane odczytuje i zapisuje.

21:07
describe_data.py odczytuje jeden plik CSV wskazany przez --data, zlicza zapisane w nim etykiety ham i spam, a następnie zapisuje raport JSON w ścieżce podanej przez --out. Oba argumenty są wymagane. W przykładzie z README.md wejściem jest data/exercise.csv, a wyjściem results/exercise-summary.json.

Co odczytuje. Skrypt oczekuje pliku CSV w UTF-8 z kolumnami message_id, text, label w tej kolejności. Jeden rekord odpowiada jednej wiadomości, nawet jeśli jej treść zajmuje kilka linii. Skrypt sprawdza, czy wszystkie pola są wypełnione, identyfikatory są unikatowe, a etykieta to ham (zwykła poczta) albo spam. Pole text służy tu do sprawdzenia, czy rekord jest kompletny. O zliczeniu wiadomości decyduje gotowa etykieta z CSV.

Co zapisuje. Raport JSON zawiera bezwzględną ścieżkę pliku wejściowego, jego sumę kontrolną SHA-256, łączną liczbę wiadomości, liczbę wiadomości z każdą etykietą oraz ścieżkę interpretera Pythona, jego wersję i katalog roboczy. Skrypt tworzy katalog wyjściowy, jeśli go brakuje, i zastępuje poprzedni raport przy ponownym użyciu tej samej ścieżki. Treść e-maili pozostaje w CSV.

W archiwum project/README.md opisuje ćwiczenie. data/ zawiera zestawy exercise.csv i demo.csv, źródłowe wiadomości .eml w raw/ oraz manifest.json z informacjami o pochodzeniu danych. Skrypt zlicza dane z wybranego CSV. Pliki .eml i manifest służą do sprawdzania źródeł. W tests/ jest osobny test z trzema syntetycznymi wiadomościami.

21:07
jaka jest instrukcja uruchomienia tego kodu?

21:10
Rozpakuj lab-1-project.zip i otwórz PowerShell w wypakowanym folderze project, w którym znajduje się describe_data.py.

Sprawdź, czy masz Pythona 3.10 lub nowszego:

py -3 --version
Uruchom skrypt na danych ćwiczeniowych:

py -3 describe_data.py --data data/exercise.csv --out results/exercise-summary.json
Po udanym uruchomieniu skrypt wypisze liczbę wiadomości i ścieżkę do raportu. Katalog results utworzy automatycznie. Raport możesz odczytać w PowerShellu:

Get-Content results/exercise-summary.json
21:11
Wyjaśnij mi działanie fragmentu kodu związanego z zwracaniem sumy SHA-256 do pliku .json. W jakim celu to liczymy oraz czy wykorzystana biblioteka jest wiarygodna.

21:18
Pole input_sha256 w raporcie JSON zawiera skrót SHA-256 pliku wejściowego CSV. Dzięki niemu możesz później sprawdzić, czy raport powstał z tej samej wersji danych, nawet jeśli nazwa pliku się nie zmieniła.

W describe_data.py dzieje się to w trzech krokach.

raw = input_path.read_bytes() odczytuje wszystkie bajty pliku CSV.
hashlib.sha256(raw).hexdigest() oblicza z tych bajtów skrót i zwraca go jako tekst złożony z 64 znaków szesnastkowych.
describe() zwraca słownik z tym tekstem pod kluczem input_sha256. Następnie main() zamienia słownik na JSON za pomocą json.dumps() i zapisuje go do pliku wskazanego przez --out.
Po co to liczymy? Jeśli zmienisz choćby jedną spację w exercise.csv, liczba wiadomości może pozostać taka sama, ale skrót się zmieni. Możesz porównać input_sha256 z wartością dla exercise.csv w data/manifest.json, żeby sprawdzić zgodność z plikiem dostarczonym do ćwiczenia. Takie porównanie sprawdza zgodność bajtów. Poprawność etykiet i wiarygodność źródła trzeba ocenić osobno.

Czy hashlib jest wiarygodna? Tak. hashlib jest częścią biblioteki standardowej Pythona, a sha256() implementuje algorytm SHA-256 zdefiniowany w standardzie NIST FIPS 180-4. To odpowiedni wybór do sprawdzania, czy plik się zmienił. Oficjalna dokumentacja Pythona

21:18

## 18.11.2026, 22:21:26 · Codex

Uzupełnię pola, które da się oprzeć na wklejonej rozmowie i wynikach laboratorium. Oddzielę wnioski po wykonaniu od przewidywań zapisanych przed próbą.

## 18.11.2026, 22:21:57 · Codex

Uzupełniłem [sprawozdanie](D:/MSI/lab1/sprawozdanie.md) o wyjaśnienie SHA-256, zakres gotowego testu i uzasadnienie zmiany liczebności. To ostatnie oznaczyłem jako wniosek zapisany po wykonaniu, ponieważ w zapisie sesji nie ma wcześniejszego przewidywania.

Zostały dwie rzeczy do doprecyzowania:

1. **Ustawienia Codexa.** Jaką dokładną nazwę modelu i jaki poziom rozumowania widziałeś podczas laboratorium? Czy zmieniałeś te ustawienia? Jeśli poziom nie był widoczny, wpisz „niedostępny”.
2. **Mały przypadek sprawdzający.** Dwa pliki mają identyczną zawartość, ale nazywają się `a.csv` i `b.csv`. Które pola w ich raportach, Twoim zdaniem, będą takie same, a które się zmienią: `input_file`, `input_sha256` i liczebności? Po Twojej odpowiedzi sprawdzę przewidywanie i dopiszę wynik.

## 18.11.2026, 22:29:45 · Student

no ja zakładałem, że w raporcie starym będzie wartość niezgodna z już zmienionym plikiem. odpowiednio mniejsza o 1 w ham i większa o 1 w spam, jak było w rzeczywistości? jeśli miałem racje to uzupełnij sprawko.

## 18.11.2026, 22:29:53 · Codex

Porównam zapisane raporty z aktualnym CSV i wpiszę do sprawozdania Twoje przewidywanie oraz wynik.

## 18.11.2026, 22:30:15 · Codex

Tak, przewidywanie się potwierdziło. Stary raport pokazywał **5 `ham` i 3 `spam`**, a po zmianie etykiety aktualny CSV i nowy raport zawierały **4 `ham` i 4 `spam`**. Czyli względem starego raportu ubyło jedno `ham`, przybyło jedno `spam`, a łączna liczba wiadomości nadal wynosiła 8.

Wpisałem Twoje przewidywanie i jego potwierdzenie do [sekcji 5 sprawozdania](D:/MSI/lab1/sprawozdanie.md:75).

## 18.11.2026, 22:31:14 · Student

okej używałem GPT-6.2 Sol High

## 18.11.2026, 22:31:23 · Codex

Wpiszę `GPT-6.2 Sol` jako model, a `High` jako poziom rozumowania.

## 18.11.2026, 22:31:40 · Codex

W [sprawozdaniu](D:/MSI/lab1/sprawozdanie.md:6) widnieje **GPT-6.2 Sol**, poziom rozumowania **High** i brak zgłoszonych zmian ustawień.

Zostało Twoje przewidywanie dla dwóch plików o identycznej zawartości i różnych nazwach. Które pola raportu się zmienią: `input_file`, `input_sha256` czy liczebności?

## 18.11.2026, 22:31:58 · Student

co zostało do uzupelnienia?

## 18.11.2026, 22:32:04 · Codex

Sprawdzę aktualne sprawozdanie i folder `sesje`, żeby wskazać, czego jeszcze brakuje.

## 18.11.2026, 22:32:14 · Codex

Merytorycznie w [sprawozdaniu](D:/MSI/lab1/sprawozdanie.md:52) brakuje tylko **małego przypadku sprawdzającego**. Twoja część to przewidzieć, co stanie się z `input_file`, `input_sha256` i liczebnościami dla dwóch plików o identycznej treści, ale różnych nazwach. Potem sprawdzę przewidywanie i dopiszę wynik.

Do oddania zostały jeszcze trzy rzeczy:

- Dołączyć pełne eksporty rozmów do `lab1/sesje/`. Obecnie jest tam tylko `.gitkeep`.
- Zapisać aktualny wynik pod wymaganą nazwą `exercise-summary.json` i zaktualizować link w sprawozdaniu. Pod tą nazwą jest obecnie raport sprzed zmiany etykiety.
- Opublikować pracę na GitHubie i uzupełnić link do końcowego commita.

## 18.11.2026, 22:33:56 · Student

zadaj mi to w formie prostych pytań, 1.... 2....

## 18.11.2026, 22:34:02 · Codex

Załóż, że `a.csv` i `b.csv` mają identyczną zawartość. Uruchamiasz skrypt osobno dla każdego pliku.

1. Czy pole `input_file` będzie takie samo w obu raportach?
2. Czy suma SHA-256 i liczby wiadomości `ham` oraz `spam` będą takie same w obu raportach? Dlaczego?

## 18.11.2026, 22:35:09 · Student

1. Pole input_file będzie się różnić ponieważ nazwa pliku jest inna, a to ona ma znaczenie.

## 18.11.2026, 22:35:21 · Codex

1. Tak. `input_file` zawiera pełną ścieżkę, a jej ostatnia część to nazwa pliku. Dlatego jedna ścieżka zakończy się na `a.csv`, a druga na `b.csv`.
2. A co przewidujesz dla sumy SHA-256 oraz liczby `ham` i `spam`, skoro oba pliki mają identyczną treść?

## 18.11.2026, 22:37:12 · Student

2. Suma SHA-256 bez zmian, bierze ona pod uwagę zawartość pliku a ta się nie zmienia. liczba ham i spam powinny być takie same dla obu plików zgodnie z działaniem logiki kodu.

## 18.11.2026, 22:37:30 · Codex

Sprawdzę Twoje przewidywanie na dwóch przykładach w pamięci, a potem dopiszę wynik do sprawozdania.

## 18.11.2026, 22:37:33 · Terminal

```powershell
$pythonPath = 'C:\Users\kamil\AppData\Local\Programs\Python\Python314\python.exe'
@'
import json
import runpy
from pathlib import Path
from types import SimpleNamespace

describe = runpy.run_path("describe_data.py")["describe"]
csv_bytes = b"message_id,text,label\n1,Spotkanie,ham\n2,Oferta,spam\n"

def describe_memory_csv(name):
    path = Path.cwd() / name
    source = SimpleNamespace(read_bytes=lambda: csv_bytes, resolve=lambda: path)
    result = describe(source)
    return {key: result[key] for key in
            ("input_file", "input_sha256", "total_messages", "label_counts")}

a = describe_memory_csv("a.csv")
b = describe_memory_csv("b.csv")
assert a["input_file"] != b["input_file"]
assert a["input_sha256"] == b["input_sha256"]
assert a["total_messages"] == b["total_messages"] == 2
assert a["label_counts"] == b["label_counts"] == {"ham": 1, "spam": 1}
print(json.dumps([a, b], indent=2))
'@ | & $pythonPath -B -
exit $LASTEXITCODE
```

Kod wyjścia polecenia terminalowego: 0.

```text
[
  {
    "input_file": "D:\\MSI\\lab1\\project\\a.csv",
    "input_sha256": "fe800d50c6e4db8d345f112b1e3f8c06fa31d15973c8dd3813683f4f478bb6e0",
    "total_messages": 2,
    "label_counts": {
      "ham": 1,
      "spam": 1
    }
  },
  {
    "input_file": "D:\\MSI\\lab1\\project\\b.csv",
    "input_sha256": "fe800d50c6e4db8d345f112b1e3f8c06fa31d15973c8dd3813683f4f478bb6e0",
    "total_messages": 2,
    "label_counts": {
      "ham": 1,
      "spam": 1
    }
  }
]
```

## 18.11.2026, 22:37:54 · Codex

Twoje przewidywanie się potwierdziło. `input_file` wskazało inną ścieżkę dla `a.csv` i `b.csv`. Suma SHA-256 była identyczna, a w obu wynikach skrypt policzył **1 `ham` i 1 `spam`**.

Dopisałem przewidywanie, sposób sprawdzenia i wynik do [sekcji 3 sprawozdania](D:/MSI/lab1/sprawozdanie.md:52).

## 18.11.2026, 22:38:12 · Student

co jeszcze zostało do zrobienia?

## 18.11.2026, 22:38:20 · Codex

Sprawdzę, czy po uzupełnieniu przykładu zostały jeszcze braki w plikach do oddania.

## 18.11.2026, 22:38:30 · Codex

**Część merytoryczna sprawozdania jest gotowa.** Zostało przygotowanie plików do oddania:

1. Dodać pełne eksporty sesji do `lab1/sesje/`. Na razie jest tam tylko `.gitkeep`.
2. Zapisać aktualny raport (**4 `ham`, 4 `spam`**) pod wymaganą nazwą `exercise-summary.json` i zaktualizować link w sprawozdaniu. Pod tą nazwą jest teraz raport sprzed zmiany.
3. Opublikować pliki na GitHubie i wpisać do sprawozdania link do commita z oddawaną pracą.

## 18.11.2026, 22:43:34 · Student

Przygotuj folder do przesłania wykładowcy i wstaw zmiany na github
