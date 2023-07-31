
# Local Storage

| № | Ресурс                     | Ключ                                                                                             | Значение                                                                                    | Краткое описание                                                                             |
|---|----------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| 1 | https://www.wildberries.ru | historySearch                                                                                    | ["herbalife чай","herbalife","h"]                                                           | Сохраняется история поиска в порядке от последнего к первому для анализа запросов и их связи |
| 2 | https://www.wildberries.ru | user-info-w7TDssOkw7PCu8KywrPCucKwwrbCtsK4wrc=                                                   | {"thirdName":"","firstName":"А*                                                             | Сохраняются данные пользователя                                                              |
| 3 | https://market.yandex.ru/  | offerStatus                                                                                      | {"keys":[],"data":{},"meta":{},"timestamp":1686808546799,"version":"2023.185.0.t1790952605"}| Сосстояние ключа о статусе какого то предложения                                             |
| 4 | https://statistic.yandex.ru| uxs_uid                                                                                          | {"49cdade0-11ee-90e2-d79c18981248":168606}                                                  | Уникальный идентификатор пользователя                                                        |
| 5 | https://www.ozon.ru/       | TSDK:https://www.ozon.ru/ozonid                                                                  | {pageViewId: "daaf3394-0dd8-41bb-2f84-ae20", pageType: "id_static_pages"}                   | Ключ для хранения информации о личном кабинете пользователя                                  |
| 6 | https://www.ozon.ru/       | TSDK:https://www.ozon.ru/seller/ivery-lab-1043440/profile/?_fr=1686816581&miniapp=seller_1043440 | {"pageViewId":"3cb0f747-a476-41ad-cf8f-0cd8638584ec","pageType":"seller"}                   | Ключ хранит информацию о магазине в который переходил пользователь                           |

# Session Storage

| № | Ресурс                       | Ключ               | Значение                                                                          | Краткое описание                                                                                               |
|---|------------------------------|--------------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 1 | https://www.wildberries.ru   | wbAnalitic         | {"l":"DLV","iid":1,"s":"popular"}                                                 | Данные о выбранной категории и фильтре                                                                         |
| 2 | https://www.wildberries.ru   | lats_search_type   | Suggest&&футболка мужская\|топ женский\|топ\|твое\|шорты женские\|шорты\|консилер | Данные о последнем запросе  с подтягивание доп тегов                                                           |
| 3 | https://market.yandex.ru/    | DEV_TOOLS_OPEN_KEY | false                                                                             | Отслеживание открыт ли Devtools у юзера                                                                        |
| 4 | https://statistic.yandex.ru/ | UXS_update_time    | "1686809827167"                                                                   | Хранение времени последнего обновления (или обращения) к ключу UXS_session_value                               |
| 5 | https://www.ozon.ru/         | TSDK:pageData      | {pageViewId: "bd0bcbd4-be23-4551-4272", pageType: "home"}                         | Ключ "TSDK:pageData" может использоваться для хранения и передачи различных данных между страницами приложения |
| 6 | https://www.ozon.ru/         | referrer           | https://www.google.com/                                                           | Ключ использоваться для хранения информации о странице, с которой пользователь перешел на текущую страницу     |

# Добавление объектов в веб-хранилища
**1. Результат выполнения команд для добавления и получения объекта в "Session Storage"**  

**Введено:** sessionStorage.setItem("PROJECT10", "FIRSTSCREEN"); sessionStorage.getItem("PROJECT10");    
**Результат:** ключ:PROJECT10 значение:FIRSTSCREEN  

![clipboard](https://i.imgur.com/yQLJJAz.png)

**2. Состояние "Session Storage" после добавления объекта**

![clipboard](https://i.imgur.com/TDMp7eX.png)

**3. Результат выполнения команд для добавления и получения объекта в "Local Storage"**

**Введено:** localStorage.setItem("PROJECT10_2", "SECONDSCREEN"); localStorage.getItem("PROJECT10_2");  
**Результат:** ключ:PROJECT10_2 значение:SECONDSCREEN  

![clipboard](https://i.imgur.com/Jc7CUFf.png)

**4. Состояние "Local Storage" после добавления объекта**

![clipboard](https://i.imgur.com/ABzBwSQ.png)
