# Sprawozdanie — Laboratorium 3

**Przedmiot:** Nauka o Danych I  
**Temat:** Wizualizacja danych w Pythonie  
**Wariant:** 14 – wydatki zdrowotne USA a modyfikowalne czynniki ryzyka (2016)  
**Środowisko:** Jupyter Notebook, Python, pandas, NumPy, Matplotlib, Plotly, plotnine  
**Autor / data:** do uzupełnienia

## 1. Cel ćwiczenia

Poznanie metod prezentacji i eksploracji danych przy użyciu trzech bibliotek: Matplotlib, Plotly oraz plotnine. Zrealizowano podstawowe i zaawansowane wykresy, ich formatowanie oraz przykłady wizualizacji geoprzestrzennych.

## 2. Dane i przygotowanie

Zbiór `IHME_USA_RISK_SPENDING_2016_Y2020M09D29.csv` zawiera 1241 wierszy i 15 kolumn, m.in. płeć, grupy wiekowe, czynniki ryzyka, przyczyny oraz wartości `mean`, `lower` i `upper`. Występuje 19 kategorii `risk_name` i 13 kategorii `cause_name`. Wykresy kategorii prezentują średnie po rekordach, a nie wydatki na mieszkańca.

## 3. Zakres realizacji

| Biblioteka | Wykonane przykłady |
|---|---|
| Matplotlib | Wykres liniowy, słupkowy, histogram, kołowy, punktowy, 3D, siatka, opisy i adnotacje |
| Plotly | Interaktywne wykresy, histogram, scatter, powierzchnia 3D, subploty, style |
| plotnine | Wykres punktowy, liniowy, słupkowy, histogram, trend, facetowanie, box plot i motywy |
| Geoprzestrzenne | Mapy punktowe, choropleth, gęstości i stanów — w części dane demonstracyjne |

## 4. Wyniki eksploracji

- Średnia wartości `mean`: **7 523,64 USD**.
- Mediana: **1 372,48 USD**.
- Maksimum: **238 503,41 USD**.

Średnia znacznie przekracza medianę, co sugeruje silnie prawostronny rozkład. Histogram umożliwia pokazanie tej asymetrii. Wśród kategorii ryzyka o wysokiej średniej wartości `mean` są wysokie skurczowe ciśnienie tętnicze oraz czynniki dietetyczne. To średnie rekordów, a nie sumy dla poszczególnych ryzyk.

## 5. Interpretacja wizualizacji

Wykres liniowy przedstawia uszeregowany ranking, a nie zmiany w czasie. Słupkowy służy do porównań kategorii, kołowy pokazuje udział liczby rekordów w podziale na płeć. Wykresy punktowe porównują `mean`, `upper` oraz szerokość przedziałów oszacowań. Matplotlib umożliwia statyczną prezentację, Plotly interakcję, a plotnine warstwową kompozycję.

## 6. Ograniczenia geoprzestrzenne

Plik nie zawiera podziału na stany USA ani współrzędnych. Mapy punktów, gęstości i stanów są demonstracjami możliwości biblioteki, a nie analizą rzeczywistego przestrzennego rozkładu wydatków.

## 7. Wnioski

1. Różne rodzaje wykresów pokazują inne aspekty danych: rozkład, porównania kategorii, zależności i wartości odstające.
2. Duża różnica między średnią a medianą dowodzi, że interpretacja samej średniej bywa myląca.
3. Dobór biblioteki zależy od celu: Matplotlib — statyczne wykresy, Plotly — interaktywność, plotnine — składanie warstw.
4. Mapy powinny opierać się na odpowiednio szczegółowych danych geograficznych, a przykłady syntetyczne muszą być jawnie oznaczone.

## 8. Repozytorium

https://github.com/Damhar/Nauka_o_Danych
