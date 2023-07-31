- **Docker** — это платформа контейнеризации с открытым исходным кодом, с помощью которой можно автоматизировать создание приложений, их доставку и управление. Платформа позволяет быстрее тестировать и выкладывать приложения, запускать на одной машине требуемое количество контейнеров. Каждый контейнер включает все необходимое для работы приложения: библиотеки, системные инструменты, код и среду исполнения. Благодаря Docker можно быстро развертывать и масштабировать приложения в любой среде и сохранять уверенность в том, что код будет работать. Docker разработан для более быстрого выкладывания ваших приложений.

- **Docker** — это популярная платформа контейнеризации, которая позволяет разработчикам легко и портативно упаковывать и развертывать приложения. Напротив, **виртуальная машина (virtual mashine)** эмулирует физический компьютер, позволяя нескольким операционным системам работать на одном физическом хосте. Контейнеры и виртуальные машины решают одну задачу, но делают это по-разному. Контейнеры занимают меньше места, т.к. переиспользуют большее количество общих ресурсов хост-системы чем VM, т.к. в отличие от VM, обеспечивает виртуализацию на уровне ОС, а не аппаратного обеспечение. Такой подход обеспечивает меньший объем занимаемого места на жёстком диске, быстрое развертывание и более простое масштабирование. 

- **Docker Compose** — это средство для определения и запуска приложений Docker с несколькими контейнерами. При работе в Compose вы используете файл YAML для настройки служб приложения. Затем вы создаете и запускаете все службы из конфигурации путем выполнения одной команды. Технология Docker Compose, если описывать её упрощённо, позволяет, с помощью одной команды, запускать множество сервисов. Docker Compose используется для одновременного управления несколькими контейнерами, входящими в состав приложения. Этот инструмент предлагает те же возможности, что и Docker, но позволяет работать с более сложными приложениями.

- **Kubernetes** — это портативная расширяемая платформа с открытым исходным кодом для управления контейнеризованными рабочими нагрузками и сервисами, которая облегчает как декларативную настройку, так и автоматизацию. Контейнеры — отличный способ связать и запустить ваши приложения. В производственной среде необходимо управлять контейнерами, которые запускают приложения, и гарантировать отсутствие простоев. Например, если контейнер выходит из строя, необходимо запустить другой контейнер. Не было бы проще, если бы такое поведение обрабатывалось системой? Kubernetes дает вам фреймворк для гибкой работы распределенных систем. Он занимается масштабированием и обработкой ошибок в приложении, предоставляет шаблоны развертывания и многое другое. 