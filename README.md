Polski pakiet językowy dla Magento 2 
==========
Repozytorium zawiera gotowy komponent z językiem polskim dla Magento 2.

## Instalacja i aktualizacja

### U użyciem composera (zalecane)

#### Instalacja

* jeżeli chcemy trzymać się tylko oficjalnych wydań pakietu
```
$ composer require kkkonrad/magento2-translate-pl
```

* jeżeli zależy nam na wszystkich aktualnych zmianach
```
$ composer require kkkonrad/magento2-translate-pl dev-master
```

Na koniec instalujemy treści statyczne z pobranym przed chwilą pakietem i czyścimy pamięci podręczne sklepu:

```
$ php bin/magento setup:static-content:deploy pl_PL
$ php bin/magento cache:flush
```

#### Aktualizacja
```
$ composer update kkkonrad/magento2-translate-pl
$ php bin/magento setup:static-content:deploy pl_PL
$ php bin/magento cache:flush
```

### Manualna
Pobieramy zawartość repozytorium i umieszczamy jego zawartość w lokalizacji `app/i18n/kkkonrad/pl_pl/`.
Ostatecznie powinniśmy otrzymać następującą strukturę:
```
app/i18n/
└── kkkonrad
    └── pl_pl
        ├── composer.json
        ├── language.xml
        ├── pl_PL.csv
        ├── README.md
        └── registration.php
```

Na koniec instalujemy treści statyczne z pobranym przed chwilą pakietem i czyścimy pamięci podręczne sklepu:
```
$ php bin/magento setup:static-content:deploy pl_PL
$ php bin/magento cache:flush
```
