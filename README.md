# SDA SMOG Wawelski - Rozkład jazdy

1 Załadowanie plików

2 Połączenie wszystkich df

3 Transformacja df

3.2 Połaczenie wartości z konkretnymi lokalizacjami wg ID sensoru

4 EDA

4.1. Ile jest Nan w danych kolumnach

4.2. Czy można znaleźć brakujące dane lub czymś je zastąpić

4.3. Jakie zastosować normy i ich zakresy dla stężenia pm10 w celu określenia jakości powietrza

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

10.3 Utworzenie modelu K-najbliższych sąsiadów -regression (odległość, haversine distance- odległość km )
