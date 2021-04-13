# SDA_SMOG_Wawelski

1 Załadowanie plików







2 Połączenie wszystkich df


3 Transformacja df







3.2 Połaczenie wartości z konkretnymi lokalizacjami wg ID sensoru

4 EDA

4.1. Ile jest Nan w danych kolumnach

4.2. Czy można znaleźć brakujące dane lub czymś je zastąpić

4.3. Jakie zastosować normy i ich zakresy dla stężenia pm10 w celu określenia jakości powietrza

Wnioski
> podejrzana wartość to `min = -1`. Poziom stężenia nie może być ujemny. Dane prawdopodobnie wymagają dalszego oczyszczenia. 

> niepokojąca jest też wartość `max=664` . Normy zaczynają sie od 25 a kończna na 150 .  Czy dla wartości powyżej 200 powinniśmy przyjąć własne normy ?

> Istotny jest fakt że 99% danych mieści się w zakresie od 0 do 282.  

> przyjęte normy i ich zakresy to 50/100/150.   Na powyższym wykresie widać wartości powyżej 200 a nawet 600. Czy są tą błędy pomiarowe czy i dla nich zrobić klasyfikację. Poniżej sprawdzę zakresy dla konkretnej stacji. 

Wnioski:
> Źródła zgodnie podają że stan powyżej 100 dla pm10 jest "alarmujący". Z uwagi że podaczas wysiku fizycznego na świerzym powietrzu pobiera się wiecej powietrza niż przy zwykłej aktywnośći uznaję że wszytkie pomiary powyżej 100 będą uznawane za szkodliwe dla zdrowia. 

> Zakresy dla PM10 które będę w dalszych krokach prowadziło to 0,25,50,100,150

5 Zmiana danych na kategoryczne - Rozbicie TimeSeries na dzień, miesiąc etc


6 Normalizacja współrzędnych - Standard scaller lub wzór (-50x1000)

7 Predykcja - szukanie najlepszego modelu

7.1 Regression

7.1.1 Regresja liniowa

7.1.1.2 Regresja liniowa Podstawowy model

7.1.1.3 Regresja liniowa - Dostrajanie modelu np grid search

7.1.2.1 RandomForestRegressor()

7.1.2.2 RandomForestRegressor() - Podstawowy model

7.1.2.3 RandomForestRegressor() - Dostrajanie modelu np grid search

7.2 Predykcja TimeSeries

7.2.1 arima (pmd arima auto-arima)

7.2.2 Profet

7.3 RNN

7.3.1 LSTM

7.3.1.1 LSTM - Podstawowy

7.3.1.2 LSTM - Dwukierunkowy

7.3.2 GRU

7.3.2.1 GRU - Podstawowy

7.3.2.2 GRU - Dwukierunkowy

8 Zestawienie wyników predykcji - wybranie najlepszego modelu do predykcji 

9 Obliczenie predykcji dla nowej daty dla wszystkich punktów pomiarowych 

10 Prototyp

10.1 Utworzenie siatki punktów w na terenie całego krakowa zlokalizowanych co 500m

10.2 Obliczenie predykcji dla wszystkich stacji pomiarowych dla konkretnej daty

> zastanawiam się czy model nie został przeuczony dla  wartości z małym stężeniem. Sprawdziłem proporacje w zbiorze i 40% wartości dla pm10 sa z zakresu 0-26.   Może trzeba pomyśleć o upsample/downsample . Nie pamiętam czy przy predykcji można ją stosować.    Co myślicie ?  Skoro ustalimy wcześniej zakrsy to może przerzucić się na klasyfikacje a nie regresję ?

> aby upewnić się trzeba zastosować predykcję dla dnia w którym na pewno było wysokie stęrzenie pm10

10.3 Utworzenie modelu K-najbliższych sąsiadów -regression (odległość, haversine distance- odległość km )
