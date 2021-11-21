# Projekt z przedmiotu zarządzania bazami danych SQL oraz NoSQL



## Skład grupy

- Julia Bielecka
- Jakub Błażejowski
- Adam Miernicki



## Opis projektu

#### 1. Analiza wymagań

Poniżej przedstawiony zostanie opis świata przedstawionego. Został on sporządzony w oparciu o pomysły danych członków grupy po przeanalizowaniu oraz zapoznaniu się z zasadą działania systemów odpowiedzialnych za przetwarzanie informacji w sprawie produktów. Sam pomysł na projekt wynika po części też z potrzeb osobistych, gdzie twórcy samego projektu wiedzą jakie mają wymagania co do wyniku końcowego. Po scharakteryzowaniu środowiska zostaną przedstawieni autorzy, którzy odzwierciedlają rzeczywiste role oraz funkcje jakie system powinien spełniać.



#### 2.Opis środowiska

Celem projektu jest utworzenie systemu służącego do zarządzania kupionymi produktami przez użytkownika. Tworzony system ma pomagać użytkownikowi zapisanie oraz odtworzenie informacji w sprawie swoich zakupionych produktów. Główne funkcje, które powinien wspomagać system to zapisywanie klientów wraz z ich zakupionymi produktami oraz możliwość rozszerzenia bazy o nowe produkty nie będące w systemie. Ważną kwestią także, z punktu widzenia systemu, będzie zapewnienie ochrony danych wszystkich podmiotów.

Z perspektywy klienta, oprócz możliwości zapisywania swoich zakupów, istotny będzie system planowania swoich wydatków na podstawie różnych kryteriów (np. zakres możliwego budżetu użytkownika lub wymagana ilość do kupienia produktów w miesiącu). Użytkownik powinien mieć jak największą dowolność jeśli chodzi o tworzenie swoich danych produktów - w przypadku nie występowania takiego produktu w bazie użytkownik powinien mieć możliwość jego utworzenia. Dodatkowo użytkownik powinien mieć dostęp, w ramach swojego konta, dostęp do systemu ocen innych użytkowników. Pozwoli to użytkownikowi dobierać produkty nie tylko ze względu na cenę ale także na podstawie innych użytkowników. 

Zapewnienie wszystkich wymienionych wyżej funkcjonalności jest związane z potrzebą przechowywania danych o klientach, produktach oraz ich producentów.



#### 3. Wymagania funkcjonalne

1. **Tworzenie konta przez użytkownika**

   ​    1.1 Utworzenie użytkownika w systemie

   ​    1.2 Zaszyfrowanie podanego hasła w systemie

2. **Możliwość wprowadzania zakupionych produktów**

3. **Narzędzia umożliwiające użytkownikowi segregację danych**

   ​	3.1 Sortowanie danych po nazwie

   ​	3.2 Sortowanie danych po cenie 

4. **Możliwość wprowadzania nowych produktów do bazy**

   ​	4.1 Wprowadzenie nazwy produktu

   ​	4.2 Wprowadzenie ceny produktu

   ​	4.3 Wprowadzenie producenta

5. **Możliwość automatyzacji i kontroli pracy z danymi z bazy produktów**

   ​	5.1 Zaplanowanie w kalendarzu przyszłych zakupów w bazie

   ​	5.2 Wprowadzenie limitów do bazy przez użytkownika 

   ​			5.2.1 Tworzenie ograniczeń na sumę kosztów na produkty na dany okres czasu

   ​			5.2.2 Tworzenie ograniczeń na ilość możliwych zakupionych produktów na dany okres czasu

6. **Prowadzenie systemu ocen użytkowników**

   ​	6.1 Użytkownik każdemu produktowi może wystawić ocenę zadowolenia z produktu

7. **Prowadzenie kontroli bazy**

   ​	7.1 Usuwanie i dodawanie produktów z bazy przez moderatorów produktów

   ​	7.2 Usuwanie klientów przez moderatorów klientów

   

#### 4. Wymagania niefunkcjonalne

1. Aplikacja powinna posiadać wygodny i przejrzysty interfejs przeznaczony dla użytkownika w wersji graficznej
2. Baza danych powinna posiadać możliwość przechowywania haseł oraz loginów w postaci zaszyfrowanej
3. Aplikacją, którą będzie obsługiwał klient, zostanie zaimplementowana w języku Java (wersja 15)
4. Baza przechowywana będzie na serwerze MySQL



#### 5. Aktorzy

**Osoba niezalogowana** - osoba oglądająca bazę produktów. Osoba ta może zobaczyć tylko jakie produkty znajdują się w bazie.

**Użytkownik** - osoba korzystająca z bazy produktów. Główne jej zadania to pamiętanie swojego loginu oraz hasła do swojego profilu. Ma możliwość ustalenia i przygotowania swojej listy zakupów, wgląd w swoje poprzednie zakupione produkty oraz planowanie nowych zakupów 

**Moderator produktów** - osoba posiadająca uprawnienia większe niż zalogowany użytkownik. Głównym zadaniem moderatora jest kontrola wprowadzanych produktów do bazy. W przypadku wykrycia pewnych nieścisłości ma możliwość usuwania oraz dodawania nowych produktów. Moderator nie może usuwać klientów z bazy.

**Moderator w sprawie klientów** - osoba posiadająca uprawnienia większe niż zalogowany użytkownik. Głównym zadaniem moderatora jest usuwanie pewnych klientów.

**Administrator** - *(poprawcie tutaj o co chodziło z tym logowaniem mnie)* osoba będąca też zalogowana do bazy z wszystkimi dostępami. Głównym jej zadaniem jest przydzielanie dostępów moderatorom.

**Sama baza danych** - *tutaj też powiedzcie czy to jest potrzebne*





