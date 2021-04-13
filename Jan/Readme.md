#### Inspiracja:

Zrobienie predhcjo na całe 24h i dodanie do folium prze

K-najbliższych sąsiadów -regression (odległość, haversine distance- odległość km )  
https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.haversine_distances.html 
https://stackoverflow.com/a/29958276


Wyznaczenie punktów -   haversine distance 

https://stackoverflow.com/a/40343603   

https://stackoverflow.com/questions/55199436/generate-grid-of-latitude-longitude-coordinates-that-fall-within-polygon   



https://www.jpytr.com/post/analysinggeographicdatawithfolium/       

# Wnioski
[11.04]
Dane:
usunięte wszystkie nulle, wartości bez normalizacji, dodatkowe cechy to: miesiac, dzień, godzina. Dane nie zostały podzielone na zbiór treningowy i testowy. 

Model:
DecisionTreeRegressor na domyślnych parametrach.

> Model przewidział wartość P10 = 6.37 , podczas gdy prawidłowa wartość to 6.00 . Uznaje że jest to marginalna pomyłka. Jutro sprawdzę predykcje na innych modelach oraz zastosuję metryki oceny predykcji modelów  aby mieć co porównywać
 

[12.04]
Dane:
usunięte wszystkie nulle, wartości bez normalizacji, dodatkowe cechy to: miesiac, dzień, godzina. Dane nie zostały podzielone na zbiór treningowy i testowy. 

Model:
LinearRegression na domyślnych parametrach.

> Model przewidział wartość P10 = 1.60 , podczas gdy prawidłowa wartość to 6.00 . Uznaje że jest to marginalna pomyłka. Jutro sprawdzę predykcje na innych modelach oraz zastosuję metryki oceny predykcji modelów  aby mieć co porównywać
