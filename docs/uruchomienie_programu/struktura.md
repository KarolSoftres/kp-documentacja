Program **PodatkiKS** opiera swoją strukturę o wycinek zakładowego planu kont – istniejącego w urzędzie. Wraz z wersją instalacyjną modułu dostarczany jest wzorcowy plan kont syntetycznych stosowanych jako główne węzły w budowie i rozliczaniu kont indywidualnych. 
Praca w programie, podobnie jak w systemie wymiarowym, odbywa się kontekstowo tzn. że użytkownik po zalogowaniu powinien wybrać jeden z trybów pracy. Domyślna grupa podatników to „Osoby fizyczne”.

![Konteksty](screeny\struktura_konteksty.png)

## Plan kont

Plan kont zbudowany jest w formie drzewa - każde konto syntetyczne może posiadać rozbudowane podsyntetyki, do których są podpięte konta indywidualne podatników. Opcja `Plan kont` służy w zasadzie tylko do przeglądania struktury ponieważ rozbudowa listy analityk wykonywana jest z poziomu funkcji obsługujących poszczególne grupy, są to:
- konta indywidualne 221
- konta hipoteczne 226
- konta pozabilansowe 991
Do przechodzenia pomiędzy poszczególnymi poziomami na liście syntetyk służą klawisze: ![](screeny\struktura_lista_kont_p.png) pierwszy z nich oznacza wejście w listę podrzędnych kont, a drugi wyjście do poziomu konta nadrzędnego.  

![Plan kont](screeny\struktura_plan_kont.png)

## Klasyfikacja budżetowa
Podobnie jak w przypadku planu kont słownik klasyfikacji budżetowej jest dostarczany wraz z wersją instalacyjną. Zawiera on analityki będące podstawą analizy dochodów w układzie budżetowym. Lista obsługiwana jest w identyczny sposób jak Plan kont.
Występuje tutaj standardowy pasek funkcyjny z omawianymi w poprzednim podrozdziale klawiszami.
Wartości z tego słownika będą wykorzystane przy definiowaniu parametrów głównych oraz są analizowane przy sporządzaniu sprawozdania RB-27S.

![Klasyfikacja budżetowa](screeny\struktura_klasyfikacja_bud.png)

<br><br>

## Kartoteka kontrahentów


Słownik omawiany w tym podrozdziale jest to główna baza osób wykorzystywana we wszystkich modułach ZSI „Sprawny Urząd”, stanowi on integralną część systemu. Znajdują się tutaj informacje teleadresowe podatników, dostawców, odbiorców itp. których dane są przetwarzane w poszczególnych programach. Formularz składa się z listy rekordów oraz panelu danych osobowych i zakładek tematycznych.

![Kartoteka kontrahentów](screeny\struktura_kartoteka_kth.png)

Lista rekordów może być sortowana wg zawartości każdej kolumny tzn. zgodnie z kolejnością alfabetyczną lub od wartości najmniejszej do największej.  

![Sortowanie](screeny\struktura_kartoteka_sortowanie.png)

Pole identyfikator jest złożeniem pól Nazwisko/Nazwa oraz Imię. Aby w liście wyszukać odpowiedni wpis, po przesortowaniu, należy rozpocząć wpisywanie wyszukiwanego wyrażenia. Pod listą system będzie wyświetlał wpisane znaki, a kursor w formie belki zostanie ustawiony na najbardziej zbliżonym wpisie w tabeli rekordów. 

![Wyszukiwanie](screeny\struktura_kartoteka_wyszukiwanie.png)

Wszystkie operacje jakie można wykonywać tzn. dodanie nowego, usunięcie, edycja, zatwierdzenie rekordu danych itd. wykonuje standardowy nawigator danych

`Ze względu na to baza, że baza jest wspólna dla wszystkich systemów nie należy w niej dublować rekordów aby zachować jednoznaczność wpisów. Oznacza to iż jeden kontrahent powinien widnieć tylko jeden raz w bazie danych.`

Zakładki tematyczne zawierają dane rozszerzone potrzebne do identyfikacji kontrahenta:

- `Dane adresowe` – dane teleadresowe, adres, adres do korespondencji, telefon, fax, e-mail, zgody na komunikację,

![Dane adresowe](screeny\zakladki_dane_adresowe.png)

- `Dane identyfikacyjne` - dodatkowe dane identyfikacyjne, imiona rodziców, data urodzenia/zgonu, paszport, dowód osobisty,

![Dane identyfikacyjne](screeny\zakladki_dane_identyfikacyjne.png)

- `Kategorie` - przyporządkowanie do określonej grupy, branży wg wartości słownikowych,

![Kategorie](screeny\zakladki_kategorie.png)

- `Osoby` - dodatkowe osoby reprezentujące,

- `Opis` - dodatkowy opis kontrahenta,

- `Dokumenty` - dokumenty i sprawy przyporządkowane do kontrahenta – powiązanie z Systemem Obiegu Dokumentów,

![Dokumenty](screeny\zakladki_dokumenty.png)

- `Funkcje` - operacje przetwarzające dane w bazie kontrahentów. Ukrywanie klientów, łączenie rekordów. Przed wykonaniem  tych operacji należy skonsultować się z producentem – ponieważ niektóre z funkcji są nieodwracalne – powinny być wykonywane po gruntownym przeszkoleniu.

![Funkcje](screeny\zakladki_funkcje.png)

- `Przetwarzanie danych osobowych` - informacje o odnotowanych udostępnieniach danych osobowych,

- `Karty, konta` - karty i konta w których występuje kontrahent,

![Karty](screeny\zakladki_karty.png)

- `Historia zmian` - zapis przebiegu historii edycji danych kontrahenta,

![Historia](screeny\zakladki_historia.png)

- `Małżonek` - oznaczenie danych małżonka.

<br><br><br>

## Definiowanie formatu numeratorów.

`Parametry > Formaty numerów`

System posiada rozbudowany kreator definiowania numeracji dokumentów. Wszystkie dostępne numeratory systemowe dostarczane są wraz z wersja instalacyjną programu. 

![Lista numeratorów](screeny\numeratory_lista.png)

Użytkownik posiada możliwość zdefiniowania kolejnych członów – maksymalnie może być ich siedem. 
Definicja numeratora składa się z części nagłówkowej oraz członów. Do część tytułowej można zaliczyć:

- `Kod` – unikalne oznaczenie numeratora definiowane w kodzie programu. 
- `Nazwa` – informacja opisowa dla specyfiki numeratora.

Definiowanie poszczególnych części  numeratora odbywa się indywidualnie, każdy człon składa się z pięciu parametrów opisujących jego charakter, typ oraz sposób użycia przy nadawaniu symbolu dla pisma.

- `Opis` – informacja opisowa o typie członu.
- `Typ` – charakter danych jakie będą umieszczone w członie.  
    ![Typ](screeny\numeratory_typy.png)   
- `Podpowiedź` – podpowiadana wartość.
- `Separator` – format separatora oddzielający poszczególne części.
- `Grupuj` – znaczenie członu lub członów wg których nastąpi numeracja – nadanie numeru kolejnego.


Poniższy rysunek zawiera przykład definicji numeratora dla „Decyzji o zarachowaniu wpłaty” składa się on z czterech członów – pierwszy z nich to oznaczenie jednostki (w tym przypadku referat Finanse-Budżet „FB”) drugi to teczka z Jednolitego Rzeczowego Wykazu Akt „3118”, w trzecim polu nadawany jest numer kolejny pisma w obrębie roku systemowego, opcja grupuj zaznaczona przy polu Rok – czwarte pole. 

![Numerator](screeny\numeratory_poprawa.png)

*Wprowadzanie modyfikacji do poszczególny członów numeratora jest dozwolone tylko i wyłącznie wtedy gdy do bazy pism danego typu nie została wprowadzona żadna pozycja. Dotyczy to przede wszystkim położenia pola „Numer kolejny”.*

<br><br><br>

## Parametry główne programu

Przed rozpoczęciem właściwej pracy z programem należy sprawdzić w menu Parametry -> Parametry główne zapisane tam informacje. Stanowią one propozycje wyjściowe, które zależnie od potrzeb, mogą być, a  w niektórych przypadkach muszą być modyfikowane oraz uaktualniane przez użytkownika stosownie do potrzeb. Ustawienia podzielone są na zakładki tematyczne:

**I. Parametry ogólne**
![Parametry ogólne](screeny\parametry_ogolne.png)

- Separator konta – definicja znaku jaki będzie użyty jako element oddzielający poszczególne segmenty konta,
- Automatyczne otwarcie okna z pozycjami dla nowego nagłówka,
- Minimalna kwota odsetek – bariera odsetkowa określająca minimalną kwotę jak będzie należna do pobrania od raty,
- koszty upomnienia - obowiązująca kwota kosztów upomnień, będzie dodawana – obciążała konto podatnika po wygenerowaniu upomnienia,
- Numer serii upomnień – domyślna seria podpowiadana przy generowaniu upomnień, powinna być zmieniona po zakończonej serii,
- Możliwość wprowadzania dokumentów stanowiących BO – parametr ten daje możliwość edycji i poprawy dokumentów z bilansu otwarcia. 
- Typy pozabilansowe – określenie typów dokumentów pozabilansowych, 
- Pokaż dokumenty pozabilansowe na koncie podatnika – parametr określający widoczność dokumentów pozabilansowych na koncie podatnika,
- Kolorować nagłówki na wydrukach – włączenie wyszarzeń w sekcjach nagłówkowych zestawień.
- Podsumowanie na kwitariuszu (suma z/do przeniesienia) – podsumowanie każdej strony kwitariusza.
- Import danych z kasy – domyślna dowolna data dekretu – zaznaczenie tej opcji daje użytkownikowi możliwość wprowadzenia dowolnej daty przyjęcia wpłat i data ta będzie domyślną dla wszystkich pozycji wybranego raportu kasowego. 
- Wpłata na koszty egzekucyjne - kolejność pobierania wpłaty na koszty.
- Wprowadź dodatkową ratę pomocniczą dla rozliczeń ratalnych

<br><br>

**II. Numeracja**

![Numeracja](screeny\parametry_numeracja.png)

- Numeracja dokumentów – wybór sposobu nadawania numerów kolejnych dla wprowadzanych dokumentów,  do wyboru są trzy opcje numeracja w obrębie roku, miesięczna oraz rejestrowa,
- Numerator dekretu – wskazanie formatu numeracji dla pozycji księgowych, 
- Sposób numerowania upomnienia – wybór sposobu numeracji upomnień, numeracja narastająca roczna lub w obrębie serii, typ numeratora.
- Prefiks numeru upomnienia
- Sufiks numeru upomnienia
- Decyzje o zarachowaniu wpłaty – wybór numeratora dla postanowień o zarachowaniu.
- Numerator tytułu wykonawczego - wybór numeratora dla tytułów wykonawczych.
- Numerator ZAS-W - wybór numeratora dla ZAS-W.
- Numerator pism do tytułów - wybór numeratora dla pism dla tytułów.
- Inicjały - sposób zapisywania inicjałów pracownika.

*Zmiana sposobu numeracji jest dozwolona tylko na początku roku obrachunkowego przed wprowadzeniem pierwszego zapisu do bazy.*

<br><br>

**III. Konteksty**

W  wersji instalacyjnej programu zdefiniowane są cztery podstawowe konteksty z przypisanymi paragrafami: 
    • Osoby fizyczne: podatki lokalne;
    • Osoby prawne: podatek od nieruchomości;
    • Osoby prawne: podatek rolny ;
    • Osoby prawne: podatek leśny;