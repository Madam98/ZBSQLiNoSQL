# Opis projektu

Na potrzeby laboratorium z przedmiotu "Zarządzanie Bazami SQL i NoSQL"

## Skład grupy

- Julia Bielecka
- Jakub Błażejowski
- Adam Miernicki

## Temat pracy

Aplikacja umożliwiająca zbieranie informacji o zakupionych produktach spożywczych i planowanie zakupów.

## Główne założenia

Część użytkowa aplikacji napisana będzie w języku Java, natomiast w celu składowania i przetwarzania danych używać będziemy bazy danych MySQL.

## Opis rzeczywistości

Konto umożliwia na dostęp i modyfikację danych. Każde konto powiązane jest z unikalnym adresem email i zabezpieczone hasłem. W ramach konta przechowywane są również informacje opcjonalne takie jak imię i nazwisko. Konto może należeć do administratora, moderatora lub użytkownika.

Z użytkownikiem powiązane są dodane przez niego produkty. Każdy produkt posiada nazwę, skład, wartości odżywcze i informację o dostępności produktu (możliwość archiwizacji jeżeli produkt przestanie być dostępny). Produkt opcjonalnie może też posiadać ocenę i recenzję napisaną przez użytkownika.

Produkty produkowane są przez producentów, o unikalnej nazwie firmy. Dla każdego producenta należy również wskazać adres firmy.

Produkty mogą być grupowane dzięki użyciu etykiet o unikalnej nazwie.

Przy zakupie produktu należy zapisać cenę za którą produkt został zakupiony, ilość, informację czy produkt był w promocji w momencie zakupu, a także sklep w którym dokonano transakcji.

Sklep charakteryzuje się adresem i nazwą, sklep może być również częścią większej sieci sklepów.

Użytkownik może ustalić sumę pieniędzy którą chciałby wydać w ustalonym czasie, zwaną budżetem. Budżet może dotyczyć wszystkich produktów lub produktów oznaczonych wybranymi etykietami. Budżety mogą również odnawiać się po dacie ich wygaśnięcia. Budżet może posiadać nazwę ułatwiającą jego identyfikację przez użytkownika.

Listy zakupów to zbiory wpisów czyli produktów już określonych, lub typów produktów. Wpis na liście zakupów musi zawierać informację o ilości produktu którą użytkownik chce zakupić, oraz ilości już zakupionej. Dla listy może być zdefiniowany okres w którym użytkownik powinien dokonać zakupu. Tak jak w przypadku budżetu, listy zakupów również mogą posiadać opcjonalną nazwę i odnawiać się cyklicznie.

<div style="page-break-after: always; break-after: page;"></div>

## Opis funkcjonalności aplikacji

Administrator ma mieć możliwość tworzenia kont moderatorów.

Administrator (tylko jeden, brak możliwości usunięcia) i moderator powinni móc usuwać inne konta.

Aplikacja powinna umożliwiać na tworzenie kont użytkowników, oraz logowanie się do wszystkich typów kont.

Użytkownik ma być głównym odbiorcą aplikacji. Dane wprowadzane przez użytkownika nie powinny w żaden sposób być dostępne dla innych użytkowników.

Użytkownik powinien mieć możliwość dodawania, usuwania i modyfikacji własnej bazy produktów, sklepów, producentów, etykiet, budżetów i list.

Dla każdego produktu użytkownik powinien móc wielokrotnie zadeklarować jego zakupienie, podając niezbędne dane.

Aplikacja powinna ostrzegać użytkownika przed wykonaniem potencjalnie niebezpiecznych akcji (usuwanie etykiet, sklepów, producentów), oraz wyświetlenie ich konsekwencji.

Aplikacja powinna informować użytkownika jeżeli ma on niezakupione towary na liście której termin ważności jest blisko, lub kiedy zbliża się do przekroczenia któregoś z budżetów.

Użytkownik powinien mieć wgląd w historię dokonanych operacji, wraz z przydatnymi statystykami.
