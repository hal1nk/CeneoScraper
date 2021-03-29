# CeneoScraper
## Etap 1 - pobranie opinii o produkcie
### Etap 1.1 - pobranie składowych pojedynczej opinii
- pobranie kodu pojedynczej strony z opiniami o produkcie
- wydobycie z kodu strony fragmentu odpowiadającego pojedynczej opinii
-zapisanie do pojedynczych zmiennych wartości składowych opinii

|Składowa|Selektor CSS|Nazwa zmiennej|Typ danych|
|---------------|------------|--------------|----------|
|Opinia|div.js_product-review|opinion||
|Identyfikator opiniie|["data-entry-id"]|opinionId||
|Autor|span.user-post__author-name|author||
|Rekomendacja|span.user-post__author-recomendation > em|rcmd||
|Liczba gwiazdek|span.user-post__score-count|stars||
|Treść opinii|div.user-post__text|content||
|Lista zalet|div[class*="positives"]~ div.review-feature__item|pros||
|Lista wad|div[class*="negatives"]~ div.review-feature__item|cons||
|Czy opinia potwierdzona zakupem|div.review-pz|purchased||
|Data wystawienia opinii|span.user-post__published > time:nth-child(1)["datatime"]|publishDate||
|Data zakupu|span.user-post__published > time:nth-child(2)["datatime"]|purchaseDate||
|Dla ilu osób przydanta|span[id^="votes-yes"]|useful||
|Dla ilu osób nie przydanta|span[id^="votes-no"]|useless||
