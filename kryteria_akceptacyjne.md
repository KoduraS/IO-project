# Obsługa klienta za pośrednictwem aplikacji mobilnej lub strony internetowej
---
## Jako klient chcę móc się zarejestrować do systemu aby móc korzystać z usług wypożyczalni

Kryteria funkcjonalne:
- Strona rejestracji wyświetla pola do wprowadzenia danych osobowych: imienia, nazwiska, daty urodzenia, nr telefonu, adres e-mail, oraz podwójnego wprowadzenia hasła
- Pola akceptują tylko poprawne formaty danych, pola z hasłem są zakropkowane
- System ocenia siłę hasła
- System weryfikuje e-mail poprzez wysłanie na niego wiadomości z kodem weryfikacyjnym
- Po zweryfikowaniu adresu e-mail możliwe jest zalogowanie, użytkownik jest przekierowany na stronę logowania
- Możliwa jest rejestracja przez popularne platformy, takie jak google

Kryteria pozafunkcjonalne:
- Dane użytkownika są szyfrowane
- E-mail do użytkownika jest wysyłany w ciągu 3 s od kliknięcia "Załóż konto" (w 95% przypadków)

## Jako klient chcę móc się zalogować do systemu aby móc korzystać z usług wypożyczalni

Kryteria funkcjonalne: 
- Strona logowania wyświetla pola na e-mail oraz hasło
- Pole e-mail akceptuje tylko poprawne formaty, a pole hasła jest zakropkowane
- Strona logowania ma opcję "Zapominałem hasła", która wysyła do użytkownika e-mail z numerem weryfikacyjnym, po jego wprowadzeniu możliwe jest ponowne wybranie hasła
- Możliwe jest zalogowanie przy użyciu popularnych platform, takich jak google
- Po zalogowaniu użytkownik przekierowywany jest do punktu nawigacyjnego

Kryteria pozafunkcjonalne:
- e-mail i hasło są szyfrowane
- E-mail do użytkownika jest wysyłany w ciągu 3 s od kliknięcia "Zapomniałem hasła" (w 95% przypadków)

## Jako klient chcę przeglądać listę wypożyczonego przeze mnie sprzętu wraz z informacją o terminie zwrotu, aby umiejętnie zagospodarować czas przeznaczony na wykorzystanie sprzętu

Kryteria funkcjonalne:
- System wyświetla listę wypożyczonego sprzętu posortowaną według czasu pozostałego do terminu zwrotu
- W przypadku przekroczenia terminu wyświetlana jest o tym informacja
- Istnieje możliwość zmiany sortowania, np. alfabetyczne
- Istnieje możliwość wyszukiwania sprzętu, np. nazwie, marce, dacie wypożyczenia, terminie zwrotu
- System wyświetla dodatkowe informacje o sprzęcie (nazwa, marka, opis, data wypożyczenia, termin oddania)
- W przypadku przekroczenia terminu wyświetlana jest również informacjo o dodatkowej opłacie

Kryteria pozafunkcjonalne:
- Opcja przeglądania sprzętu jest dostępna 24/7, czas niedostępności nie przekracza łącznie 1 dnia miesięcznie
- Po wydaniu albo zdaniu sprzętu lista wypożyczonego sprzętu jest aktualizowana w ciągu 10 s od wprowadzenia informacji do systemu (w 95% przypadków)

## Jako klient chcę wnioskować o przedłużenie wypożyczenia, aby móc elastycznie dostosowywać jego czas do zachodzących potrzeb oraz okazji wykorzystania

Kryteria funkcjonalne:
- System wyświetla listę wypożyczonych sprzętów i umożliwia zaznaczanie ich
- Po zaznaczeniu co najmniej jednego sprzętu i kliknięciu przycisku "Dalej" system umożliwia wybranie nowej daty zwrotu sprzętu
- Po wybraniu nowej daty, jeżeli sprzęt nie jest zarezerwowany, system umożliwia naciśnięcie przycisku "Wyślij wniosek", w przeciwnym razie wyświetlany jest odpowiedni komunikat
- Po kliknięciu "Wyślij wniosek" do operatora wypożyczeń wysyłany jest komunikat
- Jeżeli wniosek został zatwierdzony klient otrzymuje komunikat z potwierdzeniem oraz jest zobligowany do zapłaty
- Płatność można zrealizować od razu przy odebraniu potwierdzenia albo w dowolnym czasie przed nowym okresem.
- Jeżeli płatność nie zostanie zrealizowana za nieopłacony czas jest naliczania opłata tak jak za opóźnienie w oddaniu

Kryteria pozafunkcjonalne:
- Po wysłaniu wniosku komunikat trafia do operatora w ciągu 10 s (w 95% przypadków)
- Odpowiedź trafia do klienta w ciągu 10 s od wysłania (w 95% przypadków)

## Jako klient chcę dokonać płatności za przedłużenie wypożyczenia sprzętu za pośrednictwem platformy udostępnianej przez wypożyczalnię, aby zachować historię płatności w ramach tej platformy

Kryteria funkcjonalne:
- Podczas etapu dokonywania płatności przy wypożyczaniu sprzętu jedną z opcji jest płatność kontem Rental-aid
- Konto Rental-aid można doładowywać w aplikacji albo na stronie internetowej
- W opcjach konta użytkownika można zobaczyć historię płatności za wypożyczone sprzęty

Kryteria pozafunkcjonalne:
- Dla każdego użytkownika generowane jest konto w banku \<Nazwa Banku\>
- Poprawnością i bezpieczeństwem przelewów z i na konto zajmuje się \<Nazwa Banku\>

## Jako klient chcę przeglądać dostępne w magazynie wyposażenie do wypożyczenia, aby móc w wyprzedzeniem określić swoje zamiary w kwestii wypożyczenia lub zarezerwować sprzęt lub wypożyczyć (z wydaniem sprzętu w punkcie stacjonarnym) 
<!-- Jaka jest różnica miedzy wypożyczeniem a rezerwowaniem? -->

Kryteria funkcjonalne:
- System wyświetla listę dostępnego sprzętu
- Istnieje możliwość filtrowania sprzętu po nazwie i marce
- System wyświetla dodatkowe informacje o sprzęcie (nazwa, marka, opis, ilość dostępnych sztuk)
- Istnieje możliwość zaznaczenia sprzętu, jego ilości oraz wybrania "Zarezerwuj" lub "Wypożycz"
- Istnieje możliwość wybrania daty odebrania i zdania sprzętu
- Jeżeli w tym czasie sprzęt nie jest zarezerwowany system udostępnia przycisk "Potwierdź", który przekierowuje do płatności
- Po dokonaniu płatności do klienta wysyłany jest e-mail z potwierdzeniem a do operatora wypożyczeń komunikat z informacją o nowym zamówieniu

Kryteria pozafunkcjonalne:
- System obsługuje do 1000 jednoczesnych wypożyczeń bez zmiany wydajności
- Funkcja wypożyczania jest dostępna 24/7, dopuszczalny czas niedostępności nie przekracza 1% czasu miesięcznie
- e-mail do klienta oraz komunikat do operatora wysyłane są w ciągu 10 s od dokonania płatności (w 95% przypadków)

<!--
## Jako klient chcę rezerwować sprzęt na wybrany okres, aby uniknąć sytuacji, w której na miejscu dowiem się o braku szukanego przeze mnie wyposażenia
-->

## Jako klient chcę anulować rezerwację sprzętu, aby zwolnić go dla innych osób w sytuacji zmiany zdania

Kryteria funkcjonalne:
- System wyświetla listę zarezerwowanych sprzętów posortowana według czasu do odbioru
- Istnieje możliwość zmiany sortowania, np. alfabetycznie
- Istnieje możliwość wyszukiwania zarezerwowanego sprzęt po nazwie, marce, dacie odbioru i dacie zdania
- System wyświetla dodatkowe informacje o sprzęcie (nazwa, marka, opis, data odbioru, data zdania)
- Istnieje możliwość anulowania rezerwacji, środki powracają na konto Rental-aid użytkownika, do operatora wysyłany jest komunikat


Kryteria pozafunkcjonalne:
- Komunikat do operatora wysyłany jest w ciągu 10 s od anulowania (w 95% przypadków)
- Lista zarezerwowanych sprzętów jest dostępna 24/7, dopuszczalny czas niedostępności nie przekracza 1 dnia miesięcznie
 
## Jako klient chciałbym otrzymać powiadomienie z przypomnieniem o zbliżającym się terminie zwrotu sprzętu oraz w razie opóźnienia, aby nie zapomnieć o oddaniu sprzętu

Kryteria funkcjonalne:
- System wysyła do użytkownika e-mail oraz powiadomienie w aplikacji z przypomnieniem o zbliżającym się terminem oddania sprzętu
- e-mail wysyłany jest na trzy dni przed terminem zdania oraz na jeden dzień przed terminem
- System wysyła do użytkownika e-mail oraz powiadomienie w aplikacji z informacją o przekroczeniu  terminu oddania sprzętu oraz informację o dodatkowych opłatach przy zdaniu
- e-mail z informacją o przekroczeniu terminu wysyłany jest jeden dzień po przekroczeniu terminu, oraz trzy dni po przekroczeniu terminu

## Jako klient chciałbym mieć dostęp do historii wypożyczonych sprzętów, aby wiedzieć z jakich dokładnie sprzętów już korzystałem

Kryteria funkcjonalne:
- System wyświetla listę dawnych wypożyczonych sprzętów posortowaną od najnowszego do najstarszego
- Istnieje możliwość filtrowania sprzętów po nazwie, marce, dacie oddania, dacie odbioru
- Istnieje możliwość zmiany sortowania, np. alfabetycznie
- System wyświetla nazwę, markę, opis, okres wypożyczenia sprzętu

Kryteria pozafunkcjonalne:
- Historia wypożyczonych sprzętów jest dostępna 24/7, dopuszczalny czas niedostępności nie przekracza 1 dnia miesięcznie

<!--
## Jako klient chciałbym sprawdzić jakie jest moje opóźnienie w oddaniu sprzętu oraz jakie wiążą się z tym dodatkowe opłaty, aby znać całkowite koszty wynikające z wypożyczenia
-->

## Jako administrator chcę blokować konta klientów naruszających regulamin, aby ograniczać ryzyko strat w przyszłości

Kryteria funkcjonalne:
- System wyświetla listę użytkowników
- Istnieje możliwość filtrowania oraz wyszukiwania użytkowników po danych osobowych
- Istnieje możliwość blokowania konta użytkownika, należy podać uzasadnienie oraz odnośnik do punktu regulaminu
- Do zablokowanego użytkownika wysłany zostaje e-mail,
- W aplikacji oraz podczas próby zalogowania na stronie internetowej wyświetlany jest odpowiedni komunikat

Kryteria pozafunkcjonalne:
- E-mail do użytkownika zostaje wysłany w ciągu 10 s od zablokowania konta (w 95% przypadków)

# Operator wypożyczeń

## Jako operator wypożyczeń chcę zarejestrować klienta w bazie klientów, aby móc powiązać go z wypożyczeniem sprzętu

Kryteria funkcjonalne:
- System udostępnia formularz rejestracji klienta
- Formularz rejestracji zawiera obligatoryjne pola:
  - imię
  - nazwisko
  - unikalny identyfikator (PESEL/Nr innego dokumentu potwierdzającego tożsamość)
  - numer kontaktowy
  - adres do korespondencji pocztowej
- Formularz zawiera nieobligatoryjne pola:
  - adres email
- System zapisuje dane klienta w bazie danych po zatwierdzeniu przez operatora wypożyczeń
- Przy zapisie system generuje unikalny indentyfiaktor klienta w bazie danych
- System automatycznie zapisuej aktualną datę i godzinę jako czas wydania sprzętu
- Jeżeli w bazie istnieje już klient o tym samym unikalnym identyfikatorze, system odrzuca zapis nowego klienta do bazy i informuje operatora o występującym duplikacie
- Jeżeli obligatoryjne pole nie zostało uzupełnione, w momencie zatwierdzenia formularza system go odrzuci i wskaże nieuzupełnione pola
- Jeżeli pole zostało wypełnione niezgodnie z formatem (np. błędny zapis adresu email) system w momencie zatwierdzania odrzuci formularz i wskaże błędnie wypełnione pola

Kryteria pozafunkcjonalne:
- Zapis klienta do bazy danych odbywa się w ciągu co najwyżej 2 sekund (w 95% przypadków)

## Jako operator wypożyczeń chcę zarejestrować wydanie sprzętu klientowi, aby utrzymywać aktualny stan magazynowy i egzekwować zwrot wypożyczonego sprzętu 

Kryteria funkcjonalne:
- System udostępnia listę klientów obecnych w bazie danych
- System umożliwia dodanie klienta z listy klientów
- System udostępnia skrót do dodania nowego klienta, który automatycznie zostanie podpięty pod aktualnie rejestrowane wydanie sprzętu
- System udostępnia interfejs kalendarza pozwalający na wybranie okresu wypożyczenia
- System umożliwia wybranie sprzętu z przeglądu wyposażenia zawężonego do sprzętów dostępnych
- System udostępnia mechanizm powiadamiania magazyniera o konieczności wydania sprzętu z magazynu na stanowisko operatora wypożyczeń, wyzwalany w momencie potwierdzenia wyboru sprzętu w formularzu wydania
- System umożliwia zatwierdzenie wydania sprzętu

## Jako operator wypożyczeń chcę zarejestrować zwrot sprzętu przez klienta, aby uregulować ewentualne należności z tytułu uszkodzeń sprzętu lub opóźnionego zwrotu oraz uaktualnić stan magazynowy

Kryteria funkcjonalne:
- System umożliwa wyszukanie klienta w bazie danych
- System umożliwia wybranie klienta z bazy danych
- System udostępnia listę sprzętu wypożyczonego przez wybranego klienta
- System umożliwia wybranie sprzętu z listy sprzętów klienta celem przejścia do formularza zwrotu
- System umożliwia odnotowywanie zaistniałych w wyniku eksploatacji przez klienta usterek w polu tekstowym
- System automatycznie wypełnia pola 'data wypożycznia' i 'data zwrotu' zgodnie z zegarem systemowym
- System automatycznie oblicza wysokość należności z tytułu opóźnień w zwrocie sprzętu

## Jako operator wypożyczeń chcę przeglądać całe wyposażenie należące do wypożyczalni

Kryteria funkcjonalne:
- System udostępnia listę sprzętu sportowego
- System pozwala na wyszukiwanie sprzętu po nazwie lub unikalnym identyfikatorze sprzętu
- System umożliwia filtrowanie sprzętu według kategorii (np. sporty zimowe, wodne itd.)
- System udostępnia następujące klasy kategorii i podkategorii:
  - tematyczne:
    - sporty zimowe
      - narciarstwo
      - snowboarding
      - ...
    - sporty wodne
      - kajakarstwo
      - wędkowanie
      - nurkowanie
      - ...
    - kolarstwo
    - ...
  - dostępność:
    - dostępny
    - wypożyczony
    - w naprawie
- System umożliwia sortowanie sprzętu wg ceny wypożycznia na jeden dzień, liczby dni eksploatacji, popularności danego modelu sprzętu
- Sytem umożliwia sortowanie wg wielu kryteriów jednocześnie, wg wybranej hierarchi priorytetowości poszczególnych kryteriów
- System umożliwia rozpoczęcie procedury rejestracji wydania sprzętu z poziomu przeglądu szczegółów konkretnego sprzętu, pod warunkiem, że sprzęt jest dostępny
- System udostępnia historię sprzętu z poziomu przeglądu szczegółów sprzętu

## Jako operator wypożyczeń chcę rozpatrywać wnioski klientów o przedłużenie wypożyczenia, aby równoważyć potrzeby klientów posiadających wypożyczony sprzęt oraz chcących wypożyczyć

Kryteria funkcjonalne:
- System powiadamia operatorów o wnioskoach klientów poprzez SMS na nr służbowy
- System na głównym ekranie aplikacji wyświetla listę wniosków klientów
- System umożliwia przejście do szczegółów wniosku
- System umożliwia zatwierdzenie lub odrzucenie wniosku
- System udostępnia opcję zatwierdzenia wniosku na krótszy niż wskazany we wniosku okres z opcjonalną zgodą klienta na skrócony okres przedłużenia (brak zgody klienta jest równoznaczny z odrzuceniem wniosku)

## Jako operator wypożyczeń chciałbym mieć dostęp do historii wypożyczonych sprzętów klienta, aby móc lepiej doradzić klientowi w wyborze sprzętu

Kryteria funkcjonalne:
- System udostępnia listę klientów z bazy danych
- System udostępnia przegląd sprzętów wypożyczonych w przeszłości i aktualnie przez klienta na zasadach filtracji i sortowania dostępnych w głównym przeglądzie sprzętu
- System umożliwia filtrowanie sprzętów klienta na aktualnie wypożyczone i wypożyczone w przeszłości

## Jako operator wypożyczeń chciałbym mieć dostęp do historii danego sprzętu, aby móc prowadzić statystyki dotyczące wypożyczanego sprzętu oraz klientów
Kryteria funkcjonalne:
- System udostępnia przegląd okresów wypożyczeń sprzętu i okresów napraw
- Okres wypożyczenia zawiera:
  - datę początkową i końcową wypożyczenia,
  - pierwotnie planowaną datę zwrotu i wszystkie planowane daty końcowe zaistniałe w wyniku przedłużeń
  - dane klienta wypożyczającego sprzęt
  - ewentualny komentarz dotyczący usterek
  - koszt wypożyczenia (z uwzglęnieniem kosztu opoźnienia zwrotu oraz nie)
  - koszt opoźnienia w zwrocie
  - cenę wypożyczenia na jeden dzień
  - koszt opóźnienia w zwrocie o jeden dzień

# Magazynier
---
## Jako magazynier chcę potwierdzić wydanie sprzętu operatorowi wypożyczeń, aby uaktualnić stan magazynowy
Kryteria funkcjonalne:
- System udostępnia listę zleceń wydania sprzętu
- System umożliwia magazynierowi wybranie zlecenia
- Wybrane zlecenie znika z listy zleceń i zmienia status na 'w realizacji'
- System umożliwia potwierdzenie wydania sprzętu operatorowi wypożyczeń

## Jako magazynier chcę potwierdzić odbiór sprzętu od operatora wypożyczeń, aby uaktualnić stan magazynowy
Kryteria funkcjonalne:
- System udostępnia listę zleceń odbioru sprzętu
- System umożliwia magazynierowi wybranie zlecenia
- Wybrane zlecenie znika z listy zleceń i zmienia status na 'w realizacji'
- System umożliwia potwierdzenie odbioru sprzętu od operatora wypożyczeń

Jako magazynier chcę zgłaszać sprzęt do naprawy, aby utrzymać jego przydatność do użycia
Kryteria funkcjonalne
- System udostępnia formularz naprawy
- Formularz naprawy zawiera:
  - pole na identyfikator sprzętu
  - pole na komentarz dotyczący wymaganych napraw
- Po zatwierdzeniu formularza system oznacza sprzęt statusem 'w naprawie'
- System zapisuje czas utworzenia formularza

Jako magazynier chcę zatwierdzać oddanie sprzętu do naprawy, aby uaktualnić stan magazynowy
Kryteria funkcjonalne:
- System udostępnia listę zleceń wydania sprzętu do naprawy
- System umożliwia magazynierowi wybranie zlecenia
- Wybrane zlecenie znika z listy zleceń
- System umożliwia potwierdzenie wydania sprzętu podmiotowi realizującemu naprawę
  
Jako magazynier chcę potwierdzić odebranie sprzętu po naprawie, aby uaktualnić stan magazynowy
Kryteria funkcjonalne:
- System udostępnia listę zleceń odbioru sprzętu z naprawy
- System umożliwia magazynierowi wybranie zlecenia
- Wybrane zlecenie znika z listy zleceń
- System umożliwia potwierdzenie odbioru sprzętu od podmiotu realizującego naprawę
