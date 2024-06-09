# Wymagania

## Realizacja Celów Projektowych
1. **Definicja celów projektu:** Stworzenie modelu prognozującego cenę akcji polskich spółek na podstawie danych historycznych cen akcji i raportów kwartalnych przedsiębiorstw.
2. **Określenie wskaźników sukcesu:** Najlepiej dokładne przewidzenie ceny akcji w danym dniu na podstawie danych historycznych. Przewidywanie trendu wzrostowego i spadkowego.
3. **Wyznaczenie zakresu projektu:** Przeywidywanie cen akcji w danym dniu i ogólnie przewidywanie trendu wzrostowego/spadkowego.
4. **Określenie korzyści z realizacji:** Model który może prognozować przyszłość trendów na giełdzie, dzięki czemu możemy być odrobinę wcześniej uprzedzeni, że coś się może wydarzyć.

## Przegląd danych oraz czyszczenie
1. **Źródło danych:** ceny akcji ze [stooq.pl](https://stooq.pl), dane kwartalne dotyczące każdej spółki [bankier.pl](https://www.bankier.pl).
2. **Strategia przetwarzania danych:** Dane z [bankier.pl](https://www.bankier.pl) są zebrane przez nas za pomocą napisanego [scrappera](https://github.com/msobolewska/workshop-ai/blob/main/Scrapper.ipynb). Odrzucenie pustych plików. Połączenie plików w jeden główny. Usunięcie zbędnych kolumn. Poprawienie nazw kolumn. Posortowanie danych po dacie.
3. **Eksploracja danych:**
   - Przedział czasowy danych historycznych: 1587 dni czyli trochę ponad 37 lat. 
   - Wyświetlenie top 10 spółek z najwyższą średnią wolumenu.
   - Wyświetlenie minimalnej i maksymalnej daty notowań dla wybranych spółek.
   - Wyświetlenie wykresów cen zamknięcia dla top 10 spółek.
   - Wyświetlenie wykresów wolumenów sprzedaży dla top 10 spółek.
5. **Podział danych:** Skupiliśmy się na top 10 spółkach o największym wolumenie.
6. **Bezpieczeństwo:** 

## Modelowanie
1. **Inżynieria cech:** 
- DATE - Data
Ekstrakcja daty minimalnej i maksymalnej. Może to pomóc w identyfikacji sezonowości i trendów. Dane zawierają ten parametr w postaci stringu i formacie YYYY-MM-DD. Jest on konwertowany do postaci bardziej przyjaznej dla metod i funkcji w postaci Y-m-d.
- OPEN - Cena otwarcia
Cena akcji spółki na początku dnia handlowego. Jest to wskaźnik reprezentowany w walucie PLN.
- HIGH - Najwyższa cena w ciągu dnia
Najwyższa cena akcji spółki  w ciągu dnia handlowego. Jest to wskaźnik reprezentowany w walucie PLN.
- LOW - Najniższa cena w ciągu dnia
Najniższa cena akcji spółki  w ciągu dnia handlowego. Jest to wskaźnik reprezentowany w walucie PLN.
- CLOSE - Cena zamknięcia
Cena akcji spółki na koniec dnia handlowego. Jest to wskaźnik reprezentowany w walucie PLN.
- VOL - Wolumen obrotu
Całkowita liczba akcji, które zostały sprzedane i kupione w ciągu dnia handlowego. Wolumen obrotu jest często używany jako wskaźnik zainteresowania inwestorów daną spółką. Wyższy wolumen może wskazywać na większe zainteresowanie i aktywność inwestorów w danym dniu handlowym.
- TICKER - Identyfikator spółki

2. **Wybór algorytmów:** 
Wykorzystano Algorytm Prophet firmy Facebook do prognozowania szeregów czasowych. Prophet jest stosowany do modelowania i prognozowania danych czasowych z uwzględnieniem sezonowości i trendów.
3. **Trenowanie modeli:** 
Model Prophet jest trenowany na danych train, które zawierają dodatkowe regresory, takie jak VOL(Volumen), Przychody netto ze sprzedaży (tys.) oraz Liczba akcji (tys. szt.).
4. **Ocena modeli:** 
Średniego bezwzględnego błędu (MAE) i pierwiastka z średniego błędu kwadratowego (RMSE).
5. **Optymalizacja i dostrojenie:** 
Optymalizaja i dostrojenie jest wykonywania poprzez dodanie wspomnianych regresorów oraz dostosywanie parametrów algorymtu.

## Narzędzia i dokumentacja
1. **Dobór bibliotek:** prophet do prognozowania szeregów czasowych, pandas do analizy i manipulacji danymi, matplotlib, plotly, seaborn do tworzenia wszelakich wykresów.
2. **Określenie potrzeb sprzętowych:** 
3. **Zarządzanie kodem i wersjami:** Git
4. **Dokumentacja:** Projekt na GitHubie
