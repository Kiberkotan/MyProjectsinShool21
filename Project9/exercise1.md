## Особенности мобильного тестирования
Главная **особенность мобильного тестирования** – необходимость проверок на большом количестве конфигураций устройств. Ведь на каждой модели телефона приложение может вести себя по-своему.
Относительная лёгкость данного тестирования в том, что обычно в мобильных приложениях нет громоздкого функционала и нужды в объёмных тестах. А главная сложность – в ширине функционала. С каждым обновлением увеличивается аппаратная и программная опциональность, используются дополнительные приспособления: сим-карты, наушники, стилусы, bluetooth-устройства и прочее. 
Полноценное мобильное тестирование по времени может занять от нескольких часов до нескольких недель. Всё зависит от масштабности самого приложения и конкретных задач на текущий момент. 
- Мобильное приложение должно быть интуитивно понятным, удобным, работать бесперебойно, безопасно, круглосуточно и достаточно быстро реагировать на действия пользователя.
- Разработка мобильных приложений отличается от десктопных. Поэтому и в процессе тестирования инженер обязан провести проверки, обусловленные природой программных продуктов. Например, необходимо провести проверку установки обновлений.
- Разработчики операционных систем постоянно улучшают платформы и делают их более безопасными и производительными. Это формирует и новые требования к мобильным приложениям. Пользователь не должен испытывать каких-либо сложностей в процессе обновления. А если пользователь не устанавливает новые версии вовремя? Как на это отреагирует приложение? На эти вопросы тестировщик ищет ответы.
- Тестирование помогает выявить реакцию приложения на непредсказуемые пользовательские действия. Представьте, разблокированный гаджет оказался в кармане или сумке, и приложение должно корректно справляться с набором хаотичных и бессвязных действий.
- Ещё один вид проверок – оценка качества различного вида соединений. Такое тестирование проходит в лабораторных условиях, где возможно воссоздать максимально реалистичные условия связи. Этот вид проверки демонстрирует, как приложение будет вести себя в нестандартных ситуациях, например, когда сигнал Wi-Fi едва уловим.

### 5 методов тестирования мобильных приложений

**Функциональное тестирование**
В этом случае тестируется функционал ПО. Выясняется, соответствует ли он заявленным требованиям. Функциональное тестирование мобильных приложений предполагает наличие целого ряда проверок:
анализ процесса установки;
- тестирование процесса регистрации и авторизации;
- эксплуатационное тестирование;
- тестирование возможности обновлений;
- тестирование специфических для устройства функций;
- тестирование сервисов: работоспособность в офлайн- и онлайн-режиме.
- тестирование отправки и получения сообщений об ошибках;
- тестирование ресурсов: затраты памяти, автоматическое освобождение ресурсов и т.д.

**Внешние события или тестирование прерываний**

В этом случае специалист тестирует приложение на корректность работы в случае поступления звонков, получения сообщений и оповещений. Нужно понять, как будет вести себя программа при отсутствии и восстановлении соединения с интернетом, подключении и отключении от сети электропитания.

**Тестирование производительности**

Есть несколько типов такого тестирования:
- Проверка производительность устройства. Тестировщик выясняет, насколько стабильно работает программа на различных гаджетах. Благодаря этому разработчики могут исправить ошибки, которые ведут к задержкам или потерям данных при использовании приложения. Нужно понять, сколько памяти и ресурсов батареи затрачивает ПО. Плюс ко всему, специалист замеряет скорость работы программы.
- Проверка производительности сервера. Насколько быстро отвечает сервер? Оперативно ли обрабатываются данные? Тестировщику нужно ответить на эти и некоторые другие вопросы.
- Проверка производительность сети. Специалисту в первую очередь необходимо протестировать задержку и пропускную способность. Для этого нужно подключить устройство к различным сетям (3G-, 4G- и 5G-сети).

**Тестирование безопасности мобильного приложения**

Выявляются уязвимости ПО и оценивается безопасность приложения. Тестировщику нужно выяснить, могут ли третьи лица перехватить данные пользователя.

**Тестирование юзабилити**

Определяется, насколько удобна программа для пользователя. Специалисту необходимо учитывать важнейший параметр — пользовательский опыт. Объектами анализа становятся: кнопки, закладки, настройки, меню, контент, навигация и т.д.
```Бета-тестирование позволяет проверить программу на реальных пользователях. Таким образом, разработчики могут улучшить приложение перед выпуском. Бета-тестирование организовывается в виде внешнего приемочного тестирования. Это позволяет проанализировать отзывы клиентов.```

### Инструменты для тестирования мобильных приложений
**Эмуляторы устройств**

Чтобы протестировать программу, необходимо запустить её на большом количестве устройств с разным разрешением, диагональю, ОС и другими параметрами. Откуда же специалисту взять столько гаджетов? Решить эту проблему позволяют эмуляторы. Такие программы дают возможность имитировать работу мобильных устройств с различными характеристиками. У iOS — это симулятор `Apple iOS`, для Android — `Android Virtual Device`.

**DevTools**

Этот инструмент тестирования мобильных веб-приложений позволяет анализировать работу программ прямо в браузере. Специалист может оценить адаптивность вёрстки, смену ориентации экрана, разные скорости интернет-соединения.

**Сервисы TestFlight и Beta**

Чтобы обнаружить недочёты приложения, разработчики запускают бета-тестирование. Для этого используется почти готовая версия продукта и такие сервисы, как `TestFlight (iOS)` и `Beta (Android)`.

**Снифферы**

Снифферы помогают оценить взаимодействие с бэкендом. Речь идёт о части программы, которая работает на сервере. Сниффер представляет собой инструмент для анализа совокупности данных, которые отправляются с помощью компьютерных сетей (трафика). Такие программы позволяют изучать http-запросы, различные коды ответов и реакцию мобильного ПО на них. Наиболее распространенными вариантами являются `Fiddler` и `Charles`.

## Типы мобильных приложений
**Нативные приложения**

Разрабатываются для определённой платформы и устройства и по максимуму используют его возможности.
Нативные приложения сложные и дорогие в разработке, но у них высокая скорость работы, и они позволяют задействовать разные функции телефона — например, камеру.

**Веб-приложения**

Это не приложения, а интерфейсы сайтов, адаптированные под мобильные устройства для удобства пользователей.
Веб-приложения отличаются кросс-платформенностью, простотой в разработке и невысокой производительностью: загрузка файлов и обработка действий пользователя занимают больше времени, чем в нативном приложении.

**Гибридный тип**


Комбинация нативного приложения и веба. Разрабатывается сразу для двух платформ и пишется на универсальном языке программирования. Разработка такого приложения дешевле, и за счёт этого оно быстрее выходит на рынок.
Важный плюс — автономное обновление. Для гибридного приложения не нужно постоянно выпускать новую версию, достаточно добавить изменения на сервер.
Один из минусов — слабый визуальный стиль. Приложение пишется сразу для нескольких платформ, поэтому фирменный стиль не адаптируют для каждой из них.

## Различия в тестировании веб приложений
**Нативные приложения**:
- Тестируются на конкретной операционной системе и устройстве
- Имеют прямой доступ к ресурсам устройства, таким как камера и GPS-модуль
- Могут быть протестированы на устройствах разной производительности
- Требуют установки на устройство или симулятор, для чего нужно выполнить определенные шаги
  
**Веб-приложения**:
- Работают в браузере, вне зависимости от операционной системы
- Требуют подключения к Интернету
- Тестируются на разных браузерах
- Обычно имеют резиновый дизайн, чтобы подстраиваться под различные устройства и размеры экранов

**Гибридные приложения**:
- Код пишется один раз, но приложение может работать на разных операционных системах
- Часто используют библиотеки для доступа к ресурсам устройств
- Требуют установки на устройство, но также могут работать в браузере

**Общие моменты тестирования**:
- Нужно проверить работоспособность приложения на разных устройствах
- Необходимо проверить оптимизацию и производительность
- Особое внимание нужно уделить безопасности данных и пользовательской конфиденциальности
- На всех типах приложений можно проводить тестирование функциональности, надежности, удобства использования и дизайна интерфейса
