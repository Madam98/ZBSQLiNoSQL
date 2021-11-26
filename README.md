# Projekt z przedmiotu zarządzania bazami danych SQL oraz NoSQL



## Skład grupy

- Julia Bielecka
- Jakub Błażejowski
- Adam Miernicki


## Opis bazy danych

### Opis rzeczywistości

Konto umożliwia na dostęp i modyfikację danych. Każde konto powiązane jest z unikalnym adresem email i zabezpieczone hasłem. W ramach konta przechowywane są również informacje opcjonalne takie jak imię i nazwisko. Konto może należeć do administratora, moderatora lub użytkownika.

Z użytkownikiem powiązane są dodane przez niego produkty. Każdy produkt posiada nazwę, skład, wartości odżywcze i informację o dostępności produktu (możliwość archiwizacji jeżeli produkt przestanie być dostępny). Produkt opcjonalnie może też posiadać ocenę i recenzję napisaną przez użytkownika.

Produkty produkowane są przez producentów, o unikalnej nazwie firmy. Dla każdego producenta należy również wskazać adres firmy.

Produkty mogą być grupowane dzięki użyciu etykiet o unikalnej nazwie.

Przy zakupie produktu należy zapisać cenę za którą produkt został zakupiony, ilość, informację czy produkt był w promocji w momencie zakupu, a także sklep w którym dokonano transakcji.

Sklep charakteryzuje się adresem i nazwą, sklep może być również częścią większej sieci sklepów.

Użytkownik może ustalić sumę pieniędzy którą chciałby wydać w ustalonym czasie, zwaną budżetem. Budżet może dotyczyć wszystkich produktów lub produktów oznaczonych wybranymi etykietami. Budżety mogą również odnawiać się po dacie ich wygaśnięcia. Budżet może posiadać nazwę ułatwiającą jego identyfikację przez użytkownika.

Listy zakupów to zbiory wpisów czyli produktów już określonych, lub typów produktów. Wpis na liście zakupów musi zawierać informację o ilości produktu którą użytkownik chce zakupić, oraz ilości już zakupionej. Dla listy może być zdefiniowany okres w którym użytkownik powinien dokonać zakupu. Tak jak w przypadku budżetu, listy zakupów również mogą posiadać opcjonalną nazwę i odnawiać się cyklicznie.

## Opis projektu

### Analiza wymagań

Poniżej przedstawiony zostanie opis świata przedstawionego. Został on sporządzony w oparciu o pomysły danych członków grupy po przeanalizowaniu oraz zapoznaniu się z zasadą działania systemów odpowiedzialnych za przetwarzanie informacji w sprawie produktów. Sam pomysł na projekt wynika po części też z potrzeb osobistych, gdzie twórcy samego projektu wiedzą jakie mają wymagania co do wyniku końcowego. Po scharakteryzowaniu środowiska zostaną przedstawieni autorzy, którzy odzwierciedlają rzeczywiste role oraz funkcje jakie system powinien spełniać.

### Wymagania funkcjonalne

1. **Tworzenie konta użytkownika przez osobę niezalogowaną**
1. **Logowanie się przez osobę niezalogowaną**
1. **Usuwanie swojego konta przez użytkownika lub moderatora**
1. **Definiowanie etykiet przez użytkownika**
1. **Wprowadzanie produktów do swojego zbioru produktów przez użytkownika**
1. **Wprowadzanie zakupionych produktów przez użytkownika**
1. **Definiowanie budżetów przez użytkownika**
   1. Definiowanie budżetów w wersji cyklicznej
1. **Definiowanie list zakupów przez użytkownika**
   1. Definiowanie list zakupów w wersji cyklicznej
1. **Przeglądanie danych dostępnych dla użytkownika**
   1. Sortowanie danych
1. **Edycja danych dostępnych dla użytkownika**
1. **Ocenianie produktów przez użytkownika**
   1. Wprowadzanie oceny punktowej
   1. Wprowadzenie recenzji
1. **Usuwanie danych dostępnych dla użytkownika**
1. **Ograniczony wgląd w dane użytkowników dla moderatora lub administratora**
1. **Usuwanie kont użytkowników przez moderatora lub administratora** 
1. **Tworzenie konta moderatora przez administratora**
1. **Usuwanie kont moderatorów przez administratora**

### Wymagania pozafunkcjonalne

1. **Aplikacja powinna posiadać wygodny i przejrzysty interfejs przeznaczony dla użytkownika w wersji graficznej**
1. **Baza danych powinna posiadać możliwość przechowywania haseł w postaci zaszyfrowanej**
1. **Aplikacją, którą będzie obsługiwał klient, zostanie zaimplementowana w języku Java (wersja 17)**
1. **Baza danych przechowywana będzie na serwerze MySQL**

### Aktorzy

1. **Osoba niezalogowana** - Osoba ta może utworzyć konto lub zalogować się na istniejące konto.
1. **Użytkownik** - Osoba korzystająca z swojej bazy produktów. Główne jego zadania to pamiętanie swojego loginu oraz hasła do swojego profilu.
1. **Moderator** - Osoba posiadająca uprawnienia większe niż użytkownik. Głównym zadaniem moderatora jest usuwanie klientów używających aplikacji w sposób nieodpowiedni.
1. **Administrator** - Osoba posiadająca uprawnienia większe niż moderator. Głównym zadaniem administratora jest tworzenie i usuwanie kont moderatorów.
