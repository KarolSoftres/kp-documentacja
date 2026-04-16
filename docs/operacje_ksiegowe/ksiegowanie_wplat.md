Wprowadzanie wpłat jest to czynność najczęściej wykonywana przez użytkowników systemu, dlatego też program jest wyposażony w mechanizmy ułatwiające pracę w tym zakresie. Ze względu na dużą powtarzalność tych operacji zastosowano pewne uproszczenia, które czynią tę pracę przyjemną i wydajną. Program oferuje kilka sposobów dekretowania wpłat od podatników:

- Księgowanie przy użyciu przycisku / skrótu klawiszowego `Wpłata (F4)` ![](screeny\PODATKIKS_KW_wplata.png)  - na ekranie wyświetlony zostanie formularz z listą rat do zapłaty. 
![Okno wpłaty](screeny\PODATKIKS_KW_wplata_okno.png)
Pierwsza czynność to określenie dokumentu w którym ma się znaleźć wpłata (RK-raport kasowy, WB–wyciąg bankowy) ![](screeny\PODATKIKS_KW_wybierz_dok.png).


Następnie należy wprowadzić kwotę wpłaty i nacisnąć opcję ![](screeny\PODATKIKS_KW_auto_rozk.png), lub przejść do kolejnego pola - funkcja ta wykona automatyczne rozksięgowanie na należność główną – kolumna `Wpłata`, odsetki – `Odsetki` wpł. i koszty upomnień – `Koszty egzekucji`.

![]()

Automatyczne rozksięgowanie proponuje rozbicie wpłaty zgodne z Ordynacją Podatkową.

Zielone pola na formularzu to propozycja rozbicia wpłaty, którą użytkownik może zmienić poprzez kliknięcie w odpowiednią komórkę. W wyświetlonym formularzu pojawią pola z wartościami zaproponowanymi dla określonej raty podatku. Po dokonaniu modyfikacji należy zatwierdzić zmiany.


Kolejne parametry na formularzu to `Data rejestracji` i `Data dokumentu` oznaczają one odpowiednio datę wprowadzenia do dziennika oraz datę faktyczną wpłaty dokonanej przez podatnika (informacja na dokumencie źródłowym).

 Pole `Opis` służy do wprowadzenia dodatkowej adnotacji. Może to być np. symbol zewnętrzny, nr kwitu. 
 
 Identyfikator to wewnętrzny symbol nadawany automatycznie (np. ADM/1078/11/2009) składający się z  kilku członów: pierwszy dotyczy operatora, kolejny to unikalny numer nadawany w obrębie systemu, ostatnia część składa się z miesiąca i roku. 
 Pole `Konto Wn` jest integralnie związane z polem `Forma`, parametry te określają sposób przyjęcia wpłaty.  
 Gdy jest to `Kasa` parametry powinny przyjąć odpowiednio wartości **101-Kasa** i **KASA**.  
 W przypadku `Wpłaty` w banku **130-Rachunek bieżący** i **PRZELEW/KOMORNIK/INKASENT**.  
 Formularz zawiera również określenie osoby wpłacającej - domyślnie jest to główny podatnik. Istnieje możliwość jego zmiany poprzez wybór z listy współwłaścicieli lub słownika kontrahentów.  
Gdy zostaną wprowadzone wszystkie poprawki, należy zatwierdzić formularz.  
Przed zapisem dekretów do bazy program wyświetli numer dekretu z dziennika.  ![](screeny\kw_wplata_dekret.png)

Zbiorcza informacja o zaksięgowanych wpłatach będzie widoczna poprzez opcję `Dok. zbiorcze`, dostępną z panelu funkcji, tam też można wygenerować postanowienie o zarachowaniu wpłaty. 

<br><br>
## Księgowanie wpłaty bez ustalonego salda

W przypadku gdy wpłata dotyczy konta na którym nie widnieją salda rat do zapłaty, po uruchomieniu formularza `Wpłaty (F4)` należy użyć funkcji `Wpłata dowolna`, która pozwala na utworzenie dekretów wpłaty do rat bez ustalonego przypisu należności. 

![Dowolna wpłata](screeny\operacje_dowolna_wplata.png)

Wywołanie tej funkcji spowoduje wyświetlenie formularza, użytkownik wybiera numer raty, kwotę wpłaty (należność główna), ewentualnie odsetki oraz koszty, ostatnie pole to rok do którego mają być przyporządkowane wprowadzone powyżej wartości. Po zatwierdzeniu program powraca do formularza wpłaty, gdzie pojawia się odpowiedni rekord i tam ostatecznie zostanie zapisany dekret do bazy. 

## Kolejna wpłata

Aby usprawnić pracę w systemie można dokonywać księgowania wpłat poprzez funkcję – `Zaksięguj kolejną wpłatę` - klawisz ![](screeny\operacje_wplata_przycisk.png) w panelu funkcji - nie ma potrzeby wówczas wychodzić do listy głównej programu, a jedynie podać numer konta na które będzie dekretowana wpłata. 

![Okno F5](screeny\operacje_F5_okno.png)

Program wyświetli okno do podania numeru analityki, wystarczy podać ostatni człon konta, następnie zostanie wyszukane odpowiednie konto, a system zaproponuje pobranie pierwszej niezapłaconej raty, użytkownik może potwierdzić lub zmienić kwotę. Pozostałe czynności są identyczne jak przy dekretacji przy użycia klawisza F4.


## Księgowanie wpłat przy użyciu czytnika kodów kreskowych

Aby  można było w ten sposób dokonywać dekretacji należy przed wydrukiem na kwitariuszu umieścić parametr określający wywołanie kodu kreskowego (w takim przypadku należy skontaktować się z autorem programu – BUK „Softres”).  Tak umieszczony identyfikator będzie pozwalał na zaczytanie z druku numeru konta co pozwoli na wywołanie funkcji `Zaksięguj kolejną wpłatę`. Pozostałe czynności są identyczne jak przy dekretacji przy użycia klawisza F4.