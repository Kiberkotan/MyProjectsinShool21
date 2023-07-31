# Баг-репорты

## Баг-репорт №1 

**Заголовок:** Ошибка во время загрузки ресурсов (502 Bad Gateway)

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль  

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Перейти на сайт <https://sbermegamarket.ru/>  

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:  
```
 GET
 https://sbermegamarketru.webim.ru/button.php
[HTTP/1.1 502 Bad Gateway 583ms]
```
**Окружение:** Firefox Version 114.0



## Баг-репорт №2 

**Заголовок:** Ошибка определения типа данных в JS коде (TypeError, window.webim.api is undefined)

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Перейти на сайт <https://sbermegamarket.ru/>  

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:
```
page url: https://sbermegamarket.ru/; message: watcher callback; details: TypeError, window.webim.api is undefined, resetWebimVisitor@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:403345
setup/<@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:146542
nn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:536746
h@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:526877
st/b.run@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:527600
er@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:542996
vn/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:537828
ln@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:537227
promise callback*sn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:537317
vn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:537891
tr@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:543614
20144/Tn</e.prototype.update@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:540966
20144/we</e.prototype.notify@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:522899
set@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:524702
setProfile@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:377684
fetchProfile@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:378553
async*mounted@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:154220
nn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:536759
zn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:542500
insert@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:546239
E@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:581518
20144/xi</<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:582431
20144/</e.prototype._update@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:558809
r@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:589761
20144/Tn</e.prototype.get@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:540297
e@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:540210
20144/Lr.prototype.$mount/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:589785
20144/Lr.prototype.$mount@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:590003
52038/<@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:299793
async*78345/Te.prototype.transitionTo/</<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:505844
78345/Te.prototype.transitionTo/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:505822
78345/Te.prototype.confirmTransition/</<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:507706
r@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503571
r@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503609
Ce@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503618
78345/Te.prototype.confirmTransition/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:507609
r@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503571
r/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503600
v/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:507314
Me/</</c<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503928
Re/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:504584
promise callback*Me/</<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:504104
je/</<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:504295
je/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:504271
je@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:504221
Me/<@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503682
v@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:506949
r@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503580
r@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503609
Ce@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:503618
78345/Te.prototype.confirmTransition@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:507340
78345/Te.prototype.transitionTo@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:505665
78345/qe.prototype.init@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:512844
beforeCreate@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:515129
nn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:536759
zn@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:542500
20144/</e.prototype._init@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:556900
Lr@https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2:554416
52038/xa<@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:294838
52038@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:294979
d@https://extra-cdn.sbermegamarket.ru/static/dist/rtm.ee00827d.js:1:157
@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:928424
d.O@https://extra-cdn.sbermegamarket.ru/static/dist/rtm.ee00827d.js:1:480
@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:928444
a@https://extra-cdn.sbermegamarket.ru/static/dist/rtm.ee00827d.js:1:10037
@https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1:81
```

**Окружение:** Firefox Version 114.0

## Баг-репорт №3 

**Заголовок:** Ошибка не удалось выполнить запрос CORS

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль  

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Перейти на сайт <https://sbermegamarket.ru/>  

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:  
```
Запрос из постороннего источника заблокирован: Политика одного источника запрещает чтение удаленного ресурса на https://cms-res.online.sberbank.ru/sberid/BlackList/Button/No_Button.json. (Причина: не удалось выполнить запрос CORS). Код состояния: (null).
```
**Окружение:** Firefox Version 114.0

## Баг-репорт №4 

**Заголовок:** Ошибка сервера при авторизации (400 Bad Request) 

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 
4. Открыть сайт <https://sbermegamarket.ru/>  

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Находясь на главной странице, нажать кнопку Войти

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:  
```
GET
https://online.sberbank.ru/CSAFront/api/oidc/sbid?client_id=52cd75e2-76e1-43ba-ade6-938b2c7d4e7a
[HTTP/1.1 400 Bad Request 2037ms]
```
**Окружение:** Firefox Version 114.0

## Баг-репорт №5 

**Заголовок:** Ошибка пользовательского события 

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 
4. Открыть сайт <https://sbermegamarket.ru/>  

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Находясь на главной странице, нажать кнопку Мега Выгода

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:  
```
TypeError: DDManager Custom Event "Viewed Campaign" Error
```
**Окружение:** Firefox Version 114.0


## Баг-репорт №6 

**Заголовок:** Неуспешная отправка запроса на чтение удаленного ресурса vk.com

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 
4. Открыть сайт <https://sbermegamarket.ru/>  

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Перейти на страницу <https://sbermegamarket.ru/info/partners/> 

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:  
```
Запрос из постороннего источника заблокирован: Политика одного источника запрещает чтение удаленного ресурса на «https://vk.com/rtrg?p=VK-RTRG-1421183-77G99&products_event=view_other&price_list_id=1&e=1&i=0&metatag_url=%2F%2Fsbermegamarket.ru%2Finfo%2Fpartners%2F&metatag_title=%D0%A1%D0%B1%D0%B5%D1%80%D0%9C%D0%B5%D0%B3%D0%B0%D0%9C%D0%B0%D1%80%D0%BA%D0%B5%D1%82%20-%20%D0%BF%D0%B0%D1%80%D1%82%D0%BD%D1%91%D1%80%D0%B0%D0%BC%20-%20%D0%9C%D0%B0%D1%80%D0%BA%D0%B5%D1%82%D0%BF%D0%BB%D0%B5%D0%B9%D1%81%20SberMegaMarket.ru». (Причина: Учётные данные не поддерживаются, если заголовок CORS «Access-Control-Allow-Origin» установлен в «*»).
```
**Окружение:** Firefox Version 114.0

## Баг-репорт №7 

**Заголовок:** Ошибка:Open api access error

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 
4. Открыть сайт <https://sbermegamarket.ru/>  

**Серьезность:** Minor

**Шаги для воспроизведения:** 
1. Перейти на страницу <https://sbermegamarket.ru/info/partners/> 

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:  
```
Open api access error node_modules.89ca50aa.js:2:383012
    v https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    onerror https://vk.com/js/api/openapi.js?169:672
    s https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    (Асинхронный: EventHandlerNonNull)
    u https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    d https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    d https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    v https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    makeRequest https://vk.com/js/api/openapi.js?169:678
    ProductEvent https://vk.com/js/api/openapi.js?169:3137
    onViewedOther https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    onViewedOther https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    flushQueue https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    n https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    s https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    (Асинхронный: setInterval handler)
    l https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    init https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    onLoadInitiated https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:2
    loadIntegration https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    queueIntegrationLoad https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    s https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    s https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireEvent https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireUnfiredEvents https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    fireUnfiredEvents https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    push https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
    H https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    $ https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    te https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    setLocationInfo https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    fetchCurrentLocation https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    fetchLocationData https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    identifyRegion https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    mounted https://extra-cdn.sbermegamarket.ru/static/dist/main.564c87f0.js:1
    nn https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    zn https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
    insert https://extra-cdn.sbermegamarket.ru/static/dist/node_modules.89ca50aa.js:2
```
**Окружение:** Firefox Version 114.0

## Баг-репорт №8 

**Заголовок:** Ошибка запроса GET (404 Not Found - сервер не может найти запрашиваемый ресурс desktop.css)

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 
4. Открыть сайт <https://sbermegamarket.ru/>  

**Серьезность:** Major

**Шаги для воспроизведения:** 
1. Перейти на страницу <https://sbermegamarket.ru> 
2. Проскролить до футера
3. Кликнуть на ссылку "О компании"

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка: 
``` 
GET
https://sbermegamarket.ru/info/about-sbermegamarket-ru/desktop/css/desktop.css
[HTTP/2 404 Not Found 168ms]
```
**Окружение:** Firefox Version 114.0

## Баг-репорт №9 

**Заголовок:** Ошибка запроса шрифта

**Предшествующие условия:**
1. Открыть браузер Firefox
2. Открыть Инструменты веб-разработчика
3. Открыть вкладку Консоль 
4. Открыть сайт <https://sbermegamarket.ru/>  

**Серьезность:** Major

**Шаги для воспроизведения:** 
1. Перейти на страницу <https://sbermegamarket.ru> 
2. Проскролить до футера
3. Кликнуть на ссылку "О компании"

**Ожидаемый результат:** 
- В консоле отсутствуют ошибки

**Фактический результат:** 
- Ошибка:
```  
downloadable font: rejected by sanitizer (font-family: "Graphik LCG" style:normal weight:400 stretch:100 src index:0) source: https://main-cdn.sbermegamarket.ru/upload/static_pages/e/ab/738/eab738ad5e489ec2e334cf82dd047923/desktop/fonts/GraphikLCGRegular.eot
```
**Окружение:** Firefox Version 114.0
