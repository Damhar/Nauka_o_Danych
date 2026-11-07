# Sprawozdanie – Laboratorium 2, wariant 14

**Przedmiot:** Nauka o Danych I  
**Temat:** Praktyczne zastosowanie podstawowych funkcji statystycznych w analizie danych  
**Środowisko:** Python, Jupyter Notebook, NumPy, pandas, matplotlib  
**Autor / data:** do uzupełnienia

## 1. Cel ćwiczenia

Obliczenie średniej arytmetycznej, mediany, odchylenia standardowego, wariancji, korelacji Pearsona i kowariancji zgodnie z instrukcją „NaukaoDanychI_Zaj2.pdf”.

## 2. Dane

Zbiór: `IHME_USA_RISK_SPENDING_2016_Y2020M09D29.csv` – wariant 14, wydatki na opiekę zdrowotną w USA przypisywane modyfikowalnym czynnikom ryzyka w 2016 r. Zawiera **1241 rekordów i 15 kolumn**. Do analiz jednowymiarowych zastosowano `mean`, zaś do korelacji i kowariancji parę `mean` oraz `upper` (górną granicę oszacowania).

## 3. Metody i wyniki

| Miara | Metoda NumPy | Wynik |
|---|---|---:|
| Średnia arytmetyczna | `np.mean(x)` | 7 523,6427 USD |
| Mediana | `np.median(x)` | 1 372,4768 USD |
| Odchylenie standardowe populacyjne | `np.std(x, ddof=0)` | 18 436,0191 USD |
| Wariancja populacyjna | `np.var(x, ddof=0)` | 339 886 798,7129 USD² |
| Korelacja Pearsona (`mean`, `upper`) | `np.corrcoef(x,y)[0,1]` | 0,996407 |
| Kowariancja populacyjna (`mean`, `upper`) | `np.cov(x,y,bias=True)[0,1]` | 391 426 004,1567 USD² |

W obliczeniach odchylenia standardowego, wariancji i kowariancji zastosowano dzielenie przez `n`, odpowiadające wzorom w instrukcji.

## 4. Wizualizacje

Notebook zawiera histogram rozkładu wartości `mean` z oznaczonymi średnią i medianą oraz wykres punktowy zależności `mean`–`upper`.

## 5. Wnioski

1. Średnia przewyższa medianę, co wskazuje na silną prawostronną asymetrię rozkładu rekordów.
2. Wysokie odchylenie standardowe odzwierciedla znaczną rozpiętość wartości `mean`.
3. Korelacja `r = 0,996407` oznacza bardzo silną dodatnią zależność liniową. Warto pamiętać, że `upper` jest granicą przedziału dla tego samego oszacowania, a więc nie opisuje niezależnego zjawiska.
4. Średnia z kolumny `mean` jest średnią z **rekordów** zestawienia, a nie średnim wydatkiem na jednego mieszkańca USA.

## 6. Materiały

- [Notebook z wynikami](NOD1_Lab2_Wariant14_wyniki.ipynb)
- [Notebook źródłowy](NOD1_Lab2_Wariant14.ipynb)
- [Dane CSV](IHME_USA_RISK_SPENDING_2016_Y2020M09D29.csv)

Wersje do pobrania poza repozytorium: sprawozdanie PDF i DOCX oraz eksport notebooka PDF.
