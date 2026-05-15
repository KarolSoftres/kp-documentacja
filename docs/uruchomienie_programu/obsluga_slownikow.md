Kolejnym ze standardów stosowanym w programie są wartości słownikowe. 
Poszczególne słowniki są obsługiwane przez formularze o charakterystycznym wyglądzie.  
Okno składa się z nawigatora danych, tablicy wartości słownikowych oraz klawiszy wyboru.  W zależności od trybu wywołania słownika widoczne są różne klawisze nawigatora i przycisków wyboru. 
![Okno słownik](screeny\slowniki_okno.png)
Jeżeli słownik wywołany jest w trybie, w którym użytkownik może dopisywać, usuwać i zmieniać dane widoczne są przyciski nawigatora danych:
![Przyciski nawigacyjne](screeny\slowniki_przyciski_1.png) - Rekord pierwszy, Poprzedni, Następny, Ostatni.

![Przyciski funkcyjne](screeny\slowniki_przeciski_2.png) - Dodaj rekord, Usuń rekord, Edytuj rekord.

![Przyciski funkcyjne](screeny\slowniki_przyciski_3.png) - Zatwierdź zmiany, Anuluj, Odśwież listę.

 Edycji danych dokonuje się bezpośrednio w tablicy wartości słownikowych, a wprowadzone zmiany akceptuje się przyciskiem potwierdzenia nawigatora danych. Jeżeli chcemy anulować ostatnią zmianę należy użyć przycisku `x` nawigatora. Przywrócona zostanie wartość poprzednia ze słownika lub nowo wprowadzony wiersz zostanie pominięty. Przyciśnięcie klawisza Wybierz (lub podwójne kliknięcie na rekordzie w tablicy) powoduje wybranie wartości i zamknięcie okna, jeżeli słownik został wywołany przez przycisk wyboru wartości.

 W uproszczonej wersji okna słownikowego mogą być stosowane 3 opcje: Nowy, Popraw, Usuń:
 ![Przyciski uproszczone](screeny\slowniki_przyciski_up.png)

 W niektórych miejscach programu (np. przy wyborze warunków dla filtrów) możliwe jest wybieranie wielu wartości jednocześnie. W tym celu należy trzymając wciśnięty klawisz Ctrl, wybierać z listy interesujące nas wartości. W tablicy wartości wybrane rekordy pozostaną zaznaczone niebieską belką.  
 Jeżeli w oknie widoczne są przyciski `Zatwierdź` i `Anuluj` oznacza to, że wprowadzone zmiany muszą być zatwierdzone klawiszem `Zatwierdź`, w przeciwnym wypadku wszystkie wprowadzone zmiany zostaną anulowane, a stan w bazie danych będzie jak przed wywołaniem słownika. Umożliwia to zatwierdzanie zmian, dopiero po upewnieniu się, że wprowadzone wartości są prawidłowe. Jeżeli popełniliśmy błąd możemy anulować wszystkie wprowadzone zmiany, bez utraty integralności danych.

<br><br>
 ## Lista unikalnych wartości

 Na zakładkach wyboru warunku wyszukiwania często używane są listy wartości unikalnych uruchamiane za pomocą przycisku ![](screeny\standardy_p_slownik.png). Przykładowe okno wyboru wartości unikalnych znajduje się poniżej: 

 ![Słownik unikalnych wartości](screeny\slowniki_lista.png)

 Wywołanie okienka powoduje przeszukanie bazy danych i podanie na liście wszystkich unikalnych wartości wprowadzonych w danym polu bazy danych. Zaznaczenie interesujących nas wartości powoduje przeniesienie ich do pola wywołującego słownik.



 <br><br>
 ## Obsługa filtrów

 W okienkach i zakładkach wyboru danych z bazy stosowane są specjalne pola umożliwiające zadawanie warunków wyboru.

![Filtrowanie](screeny\slowniki_filtrowanie.png)
 
 Możliwe warunki wyboru są zależne od typu danych, jaki jest przechowywany w bazie. Poza polami logicznymi (przyjmującymi tylko dwie wartości: TAK lub NIE) warunki zadawane są w polach edycyjnych zwanych konstruktorami. Konstruktor na ekranie wygląda jak zwykłe pole edycyjne, w które wprowadzane są dane, wg których wybierane są dane z bazy. Wprowadzenie wzorca, bez metaznaków opisanych poniżej, powoduje że program szuka w bazie dokładnie zadanego wzorca z uwzględnieniem wielkości liter. Np. wprowadzenie wzorca "PIOTR" spowoduje wybranie z bazy tylko tych wartości. Wartości takie jak "Piotr", "piotr", "PIOTREK" nie zostaną znalezione, ponieważ nie są identyczne jak podany wzorzec. W celu znalezienia danych wg niepełnych informacji możliwe jest zastosowanie tzw. metaznaków. W zależności od typu pola dozwolone jest stosowanie określonych metaznaków:

**Dla wszystkich typów pól dozwolone są metaznaki:**

- `=` - wyszukanie dokładnie wskazanej wartości. Jeżeli chcemy wyszukać konkretną wartość możemy pominąć ten znak, ponieważ jest on stosowany domyślnie jeżeli nie został podany inny metaznak. Konieczne staje sie użycie znaku "=" jeżeli chcemy wyszukać pola, które posiadają puste wartości. Np. w konstruktorze wprowadzając tylko znak "=", wyszukamy te rekordy, które nie mają wprowadzonych danych w tym polu. I tak jeżeli chcemy wyszukać osoby w bazie danych, które nie mają wprowadzonego imienia, musimy w konstruktorze Imię wprowadzić znak "=". W wyniku otrzymamy wszystkie osoby bez wprowadzonego imienia. 

- `<>` - - wyszukanie wartości różnej od podanej w warunku wyszukiwania. Np. podanie "<>1" wyszuka wszystkie wartości różne od liczby jeden. Analogicznie do metaznaku =, użycie w polu konstruktora samego metaznaku <>, spowoduje wyszukanie wartości, które nie są puste, tzn. posiadają przypisaną dowolną wartość. Np. w przykładzie powyżej zostaną wybrane tylko te osoby, które mają wprowadzone imię. Osoby bez wprowadzonego imienia zostaną odrzucone. 

- `>`, `<`, `>=`, `<=` - metaznaki większości, mniejszości, większe lub równe oraz mniejsze lub równe. Najczęściej stosowane są w polach liczbowych lub daty, gdzie po metaznaku podaje się wskazaną wartość, np. ">22", "<=0" lub ">=23-03-2002" - czyli wszystkie daty powyżej 22 marca 2002 roku (format dat podawanych w warunku jest zależny od ustawień systemowych). Dla pól tekstowych o większości lub mniejszości danego ciągu znaków świadczą kody przypisane poszczególnym literom. Kody te są uporządkowane wg alfabetu. O kolejności uporządkowania polskich liter decyduje baza danych, na której pracuje program. Dla większości współczesnych baz prawidłowe uporządkowanie polskich liter jest osiągalne i zależy od poprawnej instalacji motoru bazy danych i jego wersji. Na starszych serwerach baz danych polskie litery mogą być zawsze umieszczane na końcu. 

- `|` - metaznak `lub`. Jeżeli chcemy wyszukiwać kilka wartości naraz, należy je rozdzielić tym znakiem. Np. wpisanie warunku "1|2|3" spowoduje wybranie z bazy danych mających wartość 1, 2 lub 3. Możliwe jest podanie maksymalnie do 9 alternatywnych wartości.  

<br>

**Dla pól tekstowych:**

- `%` - zastępuje dowolny ciąg znaków. Przykłady:
    - "PLA%" - wyszuka wszystkie wartości zaczynające się od liter "PLA" czyli np. "PLA", "PLATNY", "PLAnowany" itp.   
    "%EK" - wyszuka wszystkie wartości kończące się na litery "EK" czyli np. "JUREK", "WOJTEK" itp.  
    "%IR%" - wyszuka ciąg zawierający litery "IR" czyli np. "FIRMA", "MIRAŻ" itp. 

- `_` - zastępuje pojedynczy znak w wyszukiwaniu. Przykładowo:
    "_LA" - wyszuka np. "ELA", "ALA", ale już nie "WIOLA" ponieważ wyszukujemy 3 znakowego słowa, w którym pierwsza litera przyjmuje dowolny znak, natomiast 2 i 3 są zdefiniowane. 

- Oba metaznaki można łączyć w jednym warunku wyszukiwania, np. "B_R%" spowoduje wyszukanie wszystkich słów zaczynających się od B i mających trzecią literę R, czyli np. "BURAK", "BORSUK" itp. Metaznaków % i _ nie można łączyć z metaznakami wymienionymi powyżej z wyjątkiem negacji, czyli metaznaku <>. Użycie tego metaznaku przed zadanym warunkiem odwraca wynik wyszukiwania. Inaczej mówiąc wyszukiwane są te wartości, które nie spełniają zadanego warunku wyszukiwania. Np. "<>P%" wybierze wszystkie dane, które nie zaczynają się od P. 

<br>

**Dla pól tekstowych, liczbowych lub kwotowych:**

- `:` - zadanie przedziału wybieranych wartości. Wybierany przedział jest przedziałem zamknietym, tzn. wartości graniczne są też wybierane. Np. dla warunku na polu liczbowym "1:10" zostaną wybrane wszystkie wartości od 1 do 10 włącznie z granicznymi wartościami 1 i 10. 

<br>

**Dla pól daty i czasu:**

- `..` - zadanie przedziału wybieranych wartości. Warunki wyboru są identyczne jak dla wyżej opisanych pól tekstowych i liczbowych, z tą różnicą, że zamiast znaku : używamy dwóch kropek .. . Np. jeżeli chcemy wybrać przedział dat, to musimy wprowadzić warunek "1-1-2002 .. 1-7-2002".