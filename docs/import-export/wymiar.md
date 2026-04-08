`Import/Eksport > Przyjęcie danych z wymiaru` 

W zakresie wymiany danych o bieżącym stanie należności podatkowych program `PodatkiKS` współpracuje z systemem naliczającym. Informacje o otrzymanych paczkach danych są wyświetlane każdorazowo przy wejściu do programu lub poprzez wybór z menu `Import/Eksport` w opcji `Przyjęcie danych z wymiaru`.

![Import wymiaru](screeny\imp_wymiar.png)

W tabeli wyświetlą się informacje o Nazwie, Numerze systemowym, Koncie, Dacie naliczenia i eksportu  oraz Opłacie. 

Przesłane dane można przeglądać po wyborze przycisku `Pozycje`. W wyświetlonej tabeli dostępne są informacje o ratach należności podatkowych przesłanych z systemu naliczającego. 

Wczytanie danych powinno być poprzedzone wskazaniem dokumentu, do którego trafią przesłane dekrety. Następnie należy zaimportować zawarte w paczce informacje wybierając przycisk `Importuj`.  
W zależności od trybu pracy systemu wymiarowego, otrzymywane dokumenty mogą mieć status wymiaru lub zmiany.  
W przypadku trybu `Wymiar` otrzymywane dokumenty określane są jako `ZB – zobowiązania`, a ponowne przesłanie dokumentów powoduje nakrycie poprzednich zapisów. Ma to olbrzymie znaczenie z punktu widzenia elastyczności systemu, ponieważ operator nie jest obciążony  wymogiem każdorazowego kasowania wcześniejszych dekretacji. 

Podczas pracy systemu wymiarowego w trybie zmian otrzymywane dokumenty mają kod dekretacji `PR – Przypis` lub `OD – odpis`, są to zmiany wymiaru pierwotnego. Wczytywane zapisy są zaksięgowane do konta jako nowe dekrety uaktualniające stan należności podatnika wobec organu podatkowego.

`Przy trybie pracy - zmiany – systemu wymiarowego dokumenty nie są nadpisywane, każdorazowe przesłanie dokumentów na wybrane konto powoduje dopisanie tychże dekretów bez zmiany już istniejących.`

<br><br>
