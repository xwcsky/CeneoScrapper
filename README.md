# CeneoScrapper

## Kod produktu
84514582

## Algorytm poierania opini o produktach z serwisu ceneo.pl
1. Wyslanie żądania dostepu do storny internetowej z opinmi o produkcie 
2. Jeżeli operacja zakończy sie powodzeniem,wyodrębniene z kodu stron opinii o produkcie.
3. Dla każdej opinii wyodrębnienie z kodu HTML poszczególnych składowych i przypisanie ichdo elementów zbiorowych struktury danych
4. Jeżeli istnieje kolejna strona z opiniami, przejście do niej z powtórzamu dla nie kroki 1-4
5. Zapisanie plików do bazy danych


## Struktura opinii w serwisie Ceneo
|Składowe|zmienna|selektor|
|--------|-------|--------|
|opinia|review|div.js_product-review|
|identyfikator opinii|review_id|[data-entry-id]|
|autor|author|	span.user-post__author-name|
|rekomendacje|recomendation|span.user-post__author-recomendation > em|
|liczba gwiazdek|stars|span.user-post__score-count|
|treść opinii|content|div.user-post__text|
|listę zalet|pros|div.review-feature__item--positives |
|listę wad|cons|div.review-feature__item--negatives|
|ile osób uznało opinię za przydatną|useful|button.vote-yes > span|
|ile osób uznało opinię za nieprzydatną|useless|button.vote-no > span|
|data wystawienia opinii|post_date|span.user-post__published > time:nth-child(1)[datetime]|
|data zakupu produktu|purchase_date|span.user-post__published > time:nth-child(2)[datetime]|



