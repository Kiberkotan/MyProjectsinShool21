﻿## Что такое операторы в SQL?

Операторы SQL — команды(состоят из символов и слов), которые помогают добывать нужные данные из огромных массивов информации (баз данных). 

## Каких типов бывают операторы SQL, для чего каждый из них используются?
**DDL  (Data Definition Language)** -это группа операторов определения данных.  DDL  Операторы используются для создания, изменения и удаления объектов базы данных, включая таблицы, представления, индексы и хранимые процедуры. Некоторые из наиболее распространенных  DDL  операторы включают:

-   **CREATE(TABLE/DATABASE)**: Этот оператор создает новый объект базы данных, такой как таблица, представление или индекс. 
- **USE**: С помощью этой  команды выбирается база данных, необходимая для дальнейшей работы с ней.

-   **ALTER**: Этот оператор используется для изменения существующего объекта базы данных. 

-   **DROP**: Этот оператор используется для удаления существующего объекта базы данных. 

-   **TRUNCATE**: Этот оператор используется для удаления всех строк в таблице, но в отличие от оператора  DROP  он сохраняет структуру таблицы и индексы.  
    
-   **RENAME**: Этот оператор используется для переименования существующего объекта базы данных.

**DML  (Data Manipulation Language)** - это подмножество языка SQL, который используется для манипулирования данными в базе данных.  DML  Операторы используются для вставки, обновления и удаления данных в базе данных. Некоторые из наиболее распространенных  DML  операторы включают:

-   **SELECT(FROM/WHERE)**: Этот оператор используется для получения данных из одной или нескольких таблиц базы данных. 

-   **INSERT**: Этот оператор используется для вставки новых данных в таблицу. 

-   **UPDATE**: Этот оператор используется для изменения существующих данных в таблице. 
-   **DELETE**: Этот оператор используется для удаления данных из таблицы.

**Data** **Control** **Language (DCL)**  – группа операторов определения доступа к данным. Иными словами, это операторы для управления разрешениями, с помощью них мы можем разрешать или запрещать выполнение определенных операций над объектами базы данных.
-   **GRANT** – предоставляет пользователю или группе разрешения на определённые операции с объектом;
-   **REVOKE** – отзывает выданные разрешения;
-   **DENY**– задаёт запрет, имеющий приоритет над разрешением.

**Transaction** **Control** **Language (TCL)**  – группа операторов для управления транзакциями. Транзакция – это команда или блок команд (инструкций), которые успешно завершаются как единое целое, при этом в базе данных все внесенные изменения фиксируются на постоянной основе или отменяются, т.е. все изменения, внесенные любой командой, входящей в транзакцию, будут отменены.

-   **BEGIN TRANSACTION** – служит для определения начала транзакции;
-   **COMMIT TRANSACTION** – применяет транзакцию;
-   **ROLLBACK TRANSACTION** – откатывает все изменения, сделанные в контексте текущей транзакции;
-   **SAVE TRANSACTION** – устанавливает промежуточную точку сохранения внутри транзакции.

## Часто ли применяется SQL? Приведите 3 примера реальных приложений, в которых используется SQL (укажите для чего именно).


Каждый день вы проверяете почту, переводите деньги другу, покупаете онлайн или пользуетесь поисковиком. Все они в своей работе используют базы данных и язык запросов SQL.
SQL используют в Facebook, Google, Amazon, Uber, Netflix, Airbnb. Например, для того, чтобы показывать пользователям персональные рекомендации на основе того, что они смотрят, читают и лайкают.
Язык SQL нужен разработчикам, тестировщикам, аналитикам данных, администраторам, маркетологам — всем тем, кому по работе нужно выгружать и обрабатывать большие объёмы данных. Правильно организованные запросы помогают извлекать полезную информацию о клиентах и пользователях, сортируют её по определённым категориям, анализируют работу сайта или бизнеса.
Например, интернет-магазин доставляет товары по всей стране. У него обширная база клиентов. Владелец магазина хочет понять, как улучшить доставку и на какие регионы обратить внимание. Для этого он ставит задачу аналитику, который с помощью SQL-запросов выгружает данные о каждом регионе и сортирует их по объёму заказов.
