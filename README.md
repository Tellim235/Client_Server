# Client_Server
### Что ткое HTTP и HTTPS

**HTTP (HyperText Transfer Protocol — «протокол передачи гипертекста»)** — `протокол прикладного уровня передачи данных, изначально — в виде гипертекстовых документов в формате HTML, в настоящее время используется для передачи произвольных данных.`

**HTTPS (HyperText Transfer Protocol Secure)** — `расширение протокола HTTP для поддержки шифрования в целях повышения безопасности. Данные в протоколе HTTPS передаются поверх криптографических протоколов TLS или устаревшего в 2015 году SSL. В отличие от HTTP с TCP - портом 80, для HTTPS по умолчанию используется TCP-порт 443.`


### HTTP методы

**GET** - `Метод GET запрашивает представление ресурса. Запросы с использованием этого метода могут только извлекать данные.`

**HEAD** - `HEAD запрашивает ресурс так же, как и метод GET, но без тела ответа.`

**POST** - `POST используется для отправки сущностей к определённому ресурсу. Часто вызывает изменение состояния или какие-то побочные эффекты на сервере.`

**PUT** - `PUT заменяет все текущие представления ресурса данными запроса.`

**DELETE** - `DELETE удаляет указанный ресурс.`

**CONNECT** - `CONNECT устанавливает "туннель" к серверу, определённому по ресурсу.`

**OPTIONS** - `OPTIONS используется для описания параметров соединения с ресурсом.`

**TRACE** - `TRACE выполняет вызов возвращаемого тестового сообщения с ресурса.`

**PATCH** - `PATCH используется для частичного изменения ресурса.`


### HTTP статус коды сервера

**1xx** - `Information`
+ 100 Continue

**2xx** - `Success`
+ 200 OK
+ 201 Created
+ 202 Accepted

**3xx** - `Redirect`
+ 301 Moved Permanently
+ 302 Moved Temporaty

**4xx** - `Client Error`
+ 400 Bad Request
+ 401 Unauthorised
+ 403 Forbidden
+ 404 Not Found
+ 405 Method Not Allowed
+ 418 I'am a teapot

**5xx** - `Server Error`
+ 500 Internal Server Error


### Что такое ядро браузера
`Ядро браузера можно разделить на две части: движок рендеринга (инженер макета или движок рендеринга) и движок JS. Он отвечает за получение содержимого веб-страницы (HTML, XML, изображения и т. д.), организацию информации (например, добавление CSS и т. д.) и расчет режима отображения веб-страницы, а затем вывод ее на монитор или принтер. Разница в ядре браузера будет по-разному интерпретировать синтаксис веб-страницы, поэтому эффект рендеринга будет другим. Все веб-браузеры, почтовые клиенты и другие приложения, которым необходимо редактировать и отображать сетевой контент, требуют ядра. Движок JS анализирует язык Javascript и выполняет язык Javascript для достижения динамических эффектов веб-страницы.`

### Какие браузеры какиие ядра используют

**WebKit** - `Ядро с открытым кодом, который разрабатывается Apple Computer.`
+ Safari
+ Konqueror

**Blink** - `Создан на основе WebKit, Blink используется для браузера Chromium и как следствие для его производных.`
+ Chromium
+ Google Chrome
+ Яндекс.Браузер
+ Opera
+ Vivaldi
+ Microsoft Edge

**Gecko** - `ядро с открытым кодом Gecko разработан Mozilla Foundation.`
+ Mozilla Firefox
+ SeaMonkey
+ Avant Browser
+ K-Meleon
+ Netscape Browser (использует как Gecko, так и Trident)

**KHTML** - `ядро с открытым кодом, разработанный в рамках KDE, послужил основой для WebKit.`
+ Konqueror
+ ABrowse

**Trident** - `Trident разработан Microsoft для Internet Explorer.`
+ Internet Explorer
+ Maxthon (прежде известный как MyIE2)
+ Slim Browser
+ GreenBrowser

**Presto** - `более не используется. Opera перешла на Blink. Opera (Presto) лицензирован Adobe и интегрирован в пакет Adobe Creative Suite.`
+ Opera

### Что такое API
**API** - `(Application Programming Interface или интерфейс программирования приложений) — это совокупность инструментов и функций в виде интерфейса для создания новых приложений, благодаря которому одна программа будет взаимодействовать с другой. Это позволяет разработчикам расширять функциональность своего продукта и связывать его с другими. Большинство крупных компаний разрабатывают API для клиентов или для внутреннего использования.`

### Что такое ендпоинты
`Это уникальная для вашего сервера комбинация URI и HTTP метода, которой соответствует определенная логика обработки запроса клиента.`

### URL (URI, URL, URN)
**URI (Uniform Resource Identifier)** –  `это строка символов, которая используется для идентификации какого-либо ресурса по его адресу или по его имени, либо по тому и тому вместе.`

**URL (Uniform Resource Locator)** – `это строка символов, которая используется для идентификации какого-либо ресурса, но только по его адресу, по его местоположению.`

**URN (Uniform Resource Name)** – `это строка символов, которая используется для идентификации какого-либо ресурса, но только по его имени.`

### Идемпотентные HTTP методы
`Метод HTTP является идемпотентным, если повторный идентичный запрос, сделанный один или несколько раз подряд, имеет один и тот же эффект, не изменяющий состояние сервера:`

**GET** - `запрашивает представление указанного ресурса.`

**HEAD** - `запрашивает заголовки, идентичные тем, что возвращаются, если указанный ресурс будет запрошен с помощью HTTP-метода GET. Такой запрос может быть выполнен перед загрузкой большого ресурса, например, для экономии пропускной способности.`

**PUT** - `создаёт новый ресурс или заменяет представление целевого ресурса, данными представленными в теле запроса.`

**DELETE** - `удаляет указанный ресурс.`

**OPTIONS** - `используется для описания параметров соединения с целевым ресурсом. Клиент может указать особый URL для обработки метода OPTIONS, или * (звёздочку) чтобы указать весь сервер целиком.`


### Безопасные HTTP методы
`Принято соглашение, что методы GET и HEAD никогда не должны иметь иного значения, кроме загрузки. Эти методы следует рассматривать как "безопасные". Это позволяет агентам пользователя представлять другие методы, такие как POST, PUT и DELETE, таким образом, чтобы пользователь был проинформирован о том, что он запрашивает выполнение потенциально опасного действия.`

### Иденфикация, Аутентификация, Авторизация
**Идентификация** — `процесс распознавания пользователя по его идентификатору.`

**Аутентификация** — `процедура проверки подлинности, доказательство что пользователь именно тот, за кого себя выдает.`

**Авторизация** — `предоставление определённых прав.`

### Что такое IP
**IP-адрес** – `это уникальный адрес, идентифицирующий устройство в интернете или локальной сети. IP означает «Интернет-протокол» – набор правил, регулирующих формат данных, отправляемых через интернет или локальную сеть. Это идентификатор, позволяющий передавать информацию между устройствами в сети: он содержит информацию о местоположении устройства и обеспечивает его доступность для связи. IP-адреса позволяют различать компьютеры, маршрутизаторы и веб-сайты в интернете и являются важным компонентом работы интернета.`

### Что такое октеты в DNS
**Октет** - `8-битный номер, 4 из которых составляют 32-битный IP-адрес. Они имеют диапазон 00000000-11111111, соответствующий десятичным значениям 0–255.`

`Заголовок DNS пакета, состоит из 12 октет.`

### Что такое порт, сколько портов у Linux сервера
**Порт (англ. port)** — `целое неотрицательное число, записываемое в заголовках протоколов транспортного уровня сетевой модели OSI (TCP, UDP, SCTP, DCCP). Обычно на хосте под управлением ОС в пространстве пользователя исполняется несколько процессов, в каждом из которых выполняется какая-либо программа. В случае если несколько программ используют компьютерную сеть, то ОС периодически получает по сети IP-пакет, предназначенный для одной из программ.`

`Количество портов ограничено с учётом 16-битной адресации (2 16 =65536, начало — «0»). Все порты разделены на три диапазона — общеизвестные (или системные, 0—1023), зарегистрированные (или пользовательские, 1024—49151) и динамические (или частные, 49152—65535).`

### Уровни OSI
**Открытая сетевая модель OSI (Open Systems Interconnection model)** `состоит из семи уровней. Что это за уровни, как устроена модель и какова ее роль при построении сетей — в статье.`

`Модель OSI является эталонной. Эталонная она потому, что полное название модели выглядит как «Basic Reference Model Open Systems Interconnection model», где Basic Reference Model означает «эталонная модель». Вначале рассмотрим общую информацию, а потом перейдем к частным аспектам.`

7. Прикладной (application)
6. Представления (presentation)
5. Сеансовый (session)
4. Транспортный (transport)
3. Сетевой (network)
2. Канальный (data link)
1. Физический (physical)

### Хедеры http запросов
**Все заголовки разделяются на четыре основных группы:**

+ General Headers (рус. Общие заголовки) — используются в запросах и ответах.
+ Request Headers (рус. Заголовки запроса) — используются только в запросах.
+ Response Headers (рус. Заголовки ответа) — используются только в ответах.
+ Entity Headers (рус. Заголовки сущности) — сопровождают каждую сущность сообщения. Используются в запросах и ответах.
