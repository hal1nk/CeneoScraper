# CeneoScraper
## Etap 1 - pobranie opinii o produkcie
### Etap 1.1 - pobranie składowych pojedynczej opinii
- pobranie kodu pojedynczej strony z opiniami o produkcie
- wydobycie z kodu strony fragmentu odpowiadającego pojedynczej opinii
-zapisanie do pojedynczych zmiennych wartości składowych opinii

|Składowa|Selektor CSS|Nazwa zmiennej|Typ danych|
|---------------|------------|--------------|----------|
|Opinia|div.js_product-review|opinion|bs4.element.Tag|
|Identyfikator opiniie|["data-entry-id"]|opinionId|str|
|Autor|span.user-post__author-name|author|str|
|Rekomendacja|span.user-post__author-recomendation > em|rcmd|bool|
|Liczba gwiazdek|span.user-post__score-count|stars|float|
|Treść opinii|div.user-post__text|content|str|
|Lista zalet|div[class*="positives"]~ div.review-feature__item|pros|list|
|Lista wad|div[class*="negatives"]~ div.review-feature__item|cons|list|
|Czy opinia potwierdzona zakupem|div.review-pz|purchased|bool|
|Data wystawienia opinii|span.user-post__published > time:nth-child(1)["datatime"]|publishDate|str|
|Data zakupu|span.user-post__published > time:nth-child(2)["datatime"]|purchaseDate|str|
|Dla ilu osób przydanta|span[id^="votes-yes"]|useful|int|
|Dla ilu osób nie przydanta|span[id^="votes-no"]|useless|int|
