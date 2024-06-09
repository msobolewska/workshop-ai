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
2. **Wybór algorytmów:** 
3. **Trenowanie modeli:** 
4. **Ocena modeli:** 
5. **Optymalizacja i dostrojenie:** 

## Narzędzia i dokumentacja
1. **Dobór bibliotek:** prophet do prognozowania szeregów czasowych, pandas do analizy i manipulacji danymi, matplotlib, plotly, seaborn do tworzenia wszelakich wykresów.
2. **Określenie potrzeb sprzętowych:** 
3. **Zarządzanie kodem i wersjami:** Git
4. **Dokumentacja:** Projekt na GitHubie
