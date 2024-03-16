# Workshop AI

## Informacje o danych

Dane, na których operujemy, pochodzą ze strony stooq.pl i zawierają informacje o spółkach notowanych na Giełdzie Papierów Wartościowych w Warszawie (GPW). Każda spółka jest reprezentowana osobnym plikiem, gdzie każdy wiersz zawiera następujące dane:

- `<TICKER>`: Symbol danej spółki.
- `<PER>`: Zawsze 'D' (dla dniowych), co nie jest istotne dla projektu.
- `<DATE>`: Data.
- `<TIME>`: Zawsze 000000, prawdopodobnie oznaczająca północ, co również nie jest istotne dla projektu.
- `<OPEN>`: Cena akcji przy otwarciu sesji giełdowej.
- `<HIGH>`: Najwyższa cena w trakcie sesji.
- `<LOW>`: Najniższa cena w trakcie sesji.
- `<CLOSE>`: Cena akcji po zakończeniu sesji giełdowej.
- `<VOL>`: Wolumen sprzedaży.
- `<OPENINT>`: Zawsze 0 w każdym pliku, co również nie jest istotne dla projektu.

Dodatkowo, chcemy rozszerzyć te dane o kwartalne dane dotyczące danej spółki, pobrane za pomocą scrapera ze strony bankier.pl.

## Cel projektu

Rozwiązanie ma na celu wykorzystanie danych historycznych do szacowania przyszłych wartości `<CLOSE>`.

## Podobne rozwiązania

Istnieją podobne rozwiązania, choć nie identyczne. Przykłady obejmują skrypty na platformie TradingView, takie jak [Machine Learning kNN-based Strategy](https://www.tradingview.com/script/GpcT4M6T-Machine-Learning-kNN-based-Strategy/) oraz [Flawless Victory Strategy](https://pl.tradingview.com/script/i3Uc79fF-Flawless-Victory-Strategy-15min-BTC-Machine-Learning-Strategy/). Ponadto, istnieje wiele konkursów i prac na platformie Kaggle.com, takich jak konkurs [JPX Tokyo Stock Exchange Prediction](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data).

## Mierzenie wydajności modelu

Wydajność modelu będzie mierzona poprzez podział danych historycznych na dane treningowe i dane testowe. Nie będziemy dążyć do pełnej niezawodności, ale raczej do stworzenia modelu, który będzie w stanie względnie określić szanse na wzrosty/spadki cen.
