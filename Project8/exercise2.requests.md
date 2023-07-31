1. **Запрос на сервер для получения списка типов товаров в шторке "Каталог":**  
```
POST https://sbermegamarket.ru/api/mobile/v1/catalogService/catalog/menu
```
2. **Запрос на сервер при использовании поиска товаров в каталоге:**  
```
POST https://sbermegamarket.ru/api/mobile/v1/catalogService/filters/search
POST https://sbermegamarket.ru/api/mobile/v3/catalogService/catalog/searchSuggest
POST https://sbermegamarket.ru/api/mobile/v1/catalogService/catalog/search
 ```
3. **Запрос на сервер при поиске региона или города в модалке выбора вашего региона:**    
```
POST https://sbermegamarket.ru/api/mobile/v1/addressSuggestService/address/suggest
```
