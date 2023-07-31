# Задание 3.2. XPath’ы на сайте «СберСтрахование» на страницах «1.Выбор полиса» и «2.Оформление» 
## Кнопки
| №  | Наименование кнопки                            | XPath                                                                                                    |
|----|------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| 1  | Квартира                                       | //button[@id='mat-button-toggle-1-button']                                                               |
| 2  | Дом                                            | //button[@id='mat-button-toggle-2-button']                                                               |
| 3  | Сдается в аренду: да                           | //button[@id='mat-button-toggle-22-button']                                                              |
| 4  | Сдается в аренду: нет                          | //button[@id='mat-button-toggle-23-button']                                                              |
| 5  | Расположена на первом или последнем этаже: да  | //button[@id='mat-button-toggle-25-button']                                                              |
| 6  | Расположена на первом или последнем этаже: нет | //button[@id='mat-button-toggle-26-button']                                                              |
| 7  | Установлена охранная сигнализация: да          | //button[@id='mat-button-toggle-28-button']                                                              |
| 8  | Установлена охранная сигнализация: нет         | //button[@id='mat-button-toggle-29-button']                                                              |
| 9  | Применение промокода                           | //button[@class='mat-focus-indicator action-back mat-stroked-button mat-button-base']                    |
| 10 | Оформить 1стр.                                 | //button[@class='mat-focus-indicator mat-stroked-button mat-button-base mat-accent mat-button-disabled'] |
| 11 | Заполнить по Сбер ID                           | //button[@class='mat-focus-indicator sber-id-button mat-flat-button mat-button-base mat-primary']        |
| 12 | Пол мужской                                    | //button[@id='mat-button-toggle-85-button']                                                              |
| 13 | Пол женский                                    | //button[@id='mat-button-toggle-85-button']                                                              |
| 14 | Вернуться                                      | //button[@class='mat-focus-indicator action-back mat-stroked-button mat-button-base']                    |
| 15 | Оформить 2стр.                                 | //button[@class='mat-focus-indicator mat-flat-button mat-button-base mat-accent']                        |

## Поля для ввода текста
| №  | Наименование поля        | XPath                                                |
|----|--------------------------|------------------------------------------------------|
| 1  | Промокод                 | //div[@class='mat-form-field-wrapper ng-tns-c61-2']  |
| 2  | Фамилия                  | //div[@class='mat-form-field-wrapper ng-tns-c61-5']  |
| 3  | Имя                      | //div[@class='mat-form-field-wrapper ng-tns-c61-6']  |
| 4  | Отчество                 | //div[@class='mat-form-field-wrapper ng-tns-c61-7']  |
| 5  | Серия                    | //div[@class='mat-form-field-wrapper ng-tns-c61-9']  |
| 6  | Номер                    | //div[@class='mat-form-field-wrapper ng-tns-c61-10'] |
| 7  | Кем выдан                | //div[@class='mat-form-field-wrapper ng-tns-c61-12'] |
| 8  | Код подразделения        | //div[@class='mat-form-field-wrapper ng-tns-c61-13'] |
| 9  | Город                    | //div[@class='mat-form-field-wrapper ng-tns-c61-15'] |
| 10 | Улица                    | //div[@class='mat-form-field-wrapper ng-tns-c61-16'] |
| 11 | Дом                      | //div[@class='mat-form-field-wrapper ng-tns-c61-17'] |
| 12 | Квартира                 | //div[@class='mat-form-field-wrapper ng-tns-c61-18'] |
| 13 | Телефон                  | //div[@class='mat-form-field-wrapper ng-tns-c61-19'] |
| 14 | Электронная почта        | //div[@class='mat-form-field-wrapper ng-tns-c61-20'] |
| 15 | Повтор электронной почты | //div[@class='mat-form-field-wrapper ng-tns-c61-21'] |
## Чек-боксы
| № | Наименование чек-бокса    | XPath                               |
|---|----------------------|-------------------------------------|
| 1 | Отчество отсутствует | //input[@id='mat-checkbox-1-input'] |
| 2 | Улица отсутствует    | //input[@id='mat-checkbox-2-input'] |
## Датапикеры
| № | Наименование датапикера   | XPath                                                |
|---|---------------------------|------------------------------------------------------|
| 1 | Срок действия страхования | //div[@class='mat-form-field-wrapper ng-tns-c61-1']  |
| 2 | Дата рождения             | //div[@class='mat-form-field-wrapper ng-tns-c61-8']  |
| 3 | Дата выдачи          | //div[@class='mat-form-field-wrapper ng-tns-c61-11'] |

## Остальное
| № | Наименование                                             | XPath                                                     |
|---|----------------------------------------------------------|-----------------------------------------------------------|
| 1 | Слайдер в блоке выбора суммы                             | //div[@class='mat-slider-wrapper']                        |
| 2 | Логотип СберСтрахование                                  | //div[@class='sber-logo']                                 |
| 3 | Хедер «Что будет застраховано?»                          | //h4[@class='block-header']                               |
| 4 | Текстовый блок Мебель, техника и ваши вещи               | //div[text()=' Мебель, техника и ваши вещи ']             |
| 5 | Текстовый блок Падение летательных аппаратов и их частей | //div[text()='Падение летательных аппаратов и их частей'] |
| 6 | Страховая защита включенная в программу Левая колонка    | //div[text()='Чрезвычайная ситуация']/ancestor::ul        |
| 7 | Страховая защита включенная в программу Правая колонка   | //div[text()='Стихийные бедствия']/ancestor::ul           |