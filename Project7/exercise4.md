## 1. Activities: получение списка активностей (GET)

1. **URL:** {{url}}/{{activ}}
2. **Ожидаемый результат:** открывается список активностей, код 200
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: b30b3ab1-dda5-4101-bce8-cadc7eb76c88
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 01:46:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:**  
```
{
        "id": 2,
        "title": "Activity 2",
        "dueDate": "2023-06-08T03:46:53.6920032+00:00",
        "completed": true
    }
```
## 2. Activities: добавить активность (POST​)

1. **URL:** {{url}}/{{activ}}
2. **Ожидаемый результат:** добавляется активность, код 200
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 07832200-e106-455d-80b1-487fab1099b8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-06-07T04:03:41.300Z",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 01:54:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:**  
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-07T04:03:41.3Z",
    "completed": true
}
```

## 3. Activities: добавить активность (POST​) некорректный JSON

1. **URL:** {{url}}/{{activ}}
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 25802190-3ca4-47e1-a1cf-7aef09e6e908
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 0,
 "title": "1",
 "dueDate": "2023-06-07T04:03:41.300Z"",
 "completed": true
```
}
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:00:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-06024c9ed6ade14483dea810a135b560-4b346f839b514440-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 6 | BytePositionInLine: 38."
        ]
    }
}
```
## 4. Activities: добавить активность (POST​) пустые строки

1. **URL:** {{url}}/{{activ}}
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f1db454d-b07b-4ba7-9762-1c038e41ddab
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": ,
 "title": "1",
 "dueDate": "2023-06-07T04:03:41.300Z"",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:07:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b7eaaf2b568bc0438472c7265a491b6b-463978231d4ad44d-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
        ]
    }
}
```
## 5. Activities: добавить активность (POST​) изменение типа вносимых данных

1. **URL:** {{url}}/{{activ}}
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4fee2d21-7429-4074-8e6d-ae11808dcfae
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 0 ,
 "title": "string",
 "dueDate": "2023-06-07T04:22:53.031Z",
 "completed": 1
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:10:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6feca12bb3cbd74f97d8ea5fe22e1272-078ddc7cf9cb534e-00",
    "errors": {
        "$.completed": [
            "The JSON value could not be converted to System.Boolean. Path: $.completed | LineNumber: 8 | BytePositionInLine: 15."
        ]
    }
}
```
## 6. Activities: получить активность (GET) с допустимым id

1. **URL:** {{url}}/{{activ}}/{{id_cor}}
2. **Ожидаемый результат:** в теле активность с id=1, код 200
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0240b9bf-6248-4e65-9654-f4b7c46e2680
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 02:15:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:**  
```
{
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-08T03:15:11.9699327+00:00",
    "completed": false
}
```
## 7. Activities: получить активность (GET) с некорректным id (более 10 символов)

1. **URL:** {{url}}/{{activ}}/12345678911
2. **Ожидаемый результат:** ошибка код 400
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e75b0039-402f-41df-accc-eb8a1dc52797
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:20:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b5a54c2b103e034f97d64917020cb5a6-b6af11e02d38df4b-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 8. Activities: получение списка активностей (GET) с несуществующим id

1. **URL:** {{url}}/{{activ}}/1234567891
2. **Ожидаемый результат:** ошибка код 404
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7266cec3-69b4-42ed-a772-e40d4faae497
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 02:24:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-e3ac8d606b03d24eb201e10d09d4f05b-91f8a8051984364a-00"
}
```
## 9. Activities: изменить активность (PUT) с допустимым id

1. **URL:** {{url}}/{{activ}}/1
2. **Ожидаемый результат:** активность изменилась, код 200
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 41089349-16c9-4cdb-90f0-11916eeae50b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 1,
 "title": "string",
 "dueDate": "2023-06-07T04:41:05.495Z",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 02:27:19 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:**  
```
{
    "id": 1,
    "title": "string",
    "dueDate": "2023-06-07T04:41:05.495Z",
    "completed": true
}
```
## 10. Activities: изменить активность (PUT) с некорректным id (более 10 символов) в теле запроса

1. **URL:** {{url}}/{{activ}}/1
2. **Ожидаемый результат:** ошибка код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 1998ec75-74bf-443b-b418-facc6c7ad1f2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 12345678911,
 "title": "string",
 "dueDate": "2023-06-07T04:41:05.495Z",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:43:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ee1130b21624ff46bbad93f7efaf85ea-7434fcb4cd8f3542-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```
## 11. Activities: изменить активность (PUT) с некорректным id (более 10 символов)

1. **URL:** {{url}}/{{activ}}/12345678911
2. **Ожидаемый результат:** ошибка код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2b50475e-047d-439a-a10f-aa589c7092bc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 1,
 "title": "string",
 "dueDate": "2023-06-07T04:41:05.495Z",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:48:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8bf8eceb9188a24182f0f7a2d920225b-092d61f5229ad44a-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 12. Activities: изменить активность (PUT) некорректный JSON

1. **URL:** {{url}}/{{activ}}/1
2. **Ожидаемый результат:** ошибка код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d8bc6a09-99a3-4a6b-a029-cdd14c059583
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
{
```
 "id": 1,
 "title": "string",
 "dueDate": "2023-06-07T04:41:05.495Z"",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:51:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-87d76fb0d4afb94a83d17a0abd587c7c-38aa7be13efd8f4c-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 38."
        ]
    }
}
```
## 13. Activities: изменить активность (PUT​) пустые строки

1. **URL:** {{url}}/{{activ}}/1
2. **Ожидаемый результат:** ошибка код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d546807d-c56c-41b4-b2db-2a64b5387c61
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": ,
 "title": "string",
 "dueDate": "2023-06-07T04:41:05.495Z",
 "completed": true
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:53:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-05d34b929c8c524690652db5174fcf06-cac3b8bdba9a2147-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## 14. Activities: изменить активность (PUT​) изменение типа вносимых данных

1. **URL:** {{url}}/{{activ}}/1
2. **Ожидаемый результат:** ошибка код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 01b379fe-cbd8-4794-aff6-4e4c3df47cd9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
```
{
 "id": 1,
 "title": "string",
 "dueDate": "2023-06-07T04:41:05.495Z",
 "completed": 1
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 02:58:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:**  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-96aa92de9cf1034486f495b63a260d08-f881b0c6e6ee9541-00",
    "errors": {
        "$.completed": [
            "The JSON value could not be converted to System.Boolean. Path: $.completed | LineNumber: 8 | BytePositionInLine: 15."
        ]
    }
}
```
## 15. Activities: удалить активность (DELETE​) с допустимым id

1. **URL:** {{url}}/{{activ}}/1
2. **Ожидаемый результат:** активность удалена, код 200
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4308a60e-d52e-435c-b06d-9b8ccdb9a158
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Length: 0
Date: Thu, 08 Jun 2023 03:00:34 GMT
Server: Kestrel
api-supported-versions: 1.0
```
6. **Тело ответа:**  

## 16. Activities: удалить активность  (DELETE) с некорректным id (более 10 символов)

1. **URL:** {{url}}/{{activ}}/12345678911
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fa4405d2-c0e0-4e6d-b89e-b19fa92b72db
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 03:03:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0a6e783219f95741b0ca056d7d701298-0eb54e164f285f4f-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 17. Authors: получение списка авторов (GET)

1. **URL:** {{url}}/{{auth}}
2. **Ожидаемый результат:** получен список авторов, код 200
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fd75b8e1-e559-4ec1-9a95-5f724ea24436
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:** 
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 03:34:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:** 
```
 {
         "id": 1,
         "idBook": 1,
         "firstName": "First Name 1",
        "lastName": "Last Name 1"
  }
```
>## 18. Authors: добавить автора (POST​)

1. **URL:** {{url}}/{{auth}}
2. **Ожидаемый результат:** добавлен автор, код 200
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 283a1d72-a26c-464c-ad49-f71db43cce7c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
```
{
 "id": 0,
 "idBook": 0,
 "firstName": "string",
 "lastName": "string"
}
```
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 03:38:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:** 
```
 {
    "id": 0,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
}
```
## 19. Authors: добавить автора (POST​) некорректный JSON

1. **URL:** {{url}}/{{auth}}
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 6b8cd63e-3284-4ed1-8fca-dbd8c7992782
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
```
{
 "id": 0,
 "idBook": 0,
 "firstName": "string"",
 "lastName": "string"
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 03:43:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-242b1235caff224fa01694e0012c08e0-c0add8d56f1db441-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 22."
        ]
    }
}
```
## 20. Authors: добавить автора (POST​) пустые строки

1. **URL:** {{url}}/{{auth}}
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a264b3f4-739b-49f1-8fcd-fb0432d252c2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
```
{
 "id": ,
 "idBook": ,
 "firstName": "string",
 "lastName": "string"
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 03:46:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3e565361dbadb3469c1db5138626d445-d0f54bf020c40247-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## 21. Authors: добавить автора (POST​) изменение типа вносимых данных

1. **URL:** {{url}}/{{auth}}
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 8e830353-7b4d-40e5-895c-8c95873663bb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
```
{
 "id": q,
 "idBook": q,
 "firstName": "string",
 "lastName": "string"
}
```
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 03:48:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-60513e20ff487b449cf2ea5b437d8a52-6c89f100595f464e-00",
    "errors": {
        "$.id": [
            "'q' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## 22. Authors: получить данные книги (GET) с допустимым id 

1. **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1
2. **Ожидаемый результат:** получены данные книги, код 200
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9138589c-961e-439a-9ef1-e38a243fea9a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 03:59:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:** 
```
{
 "id": 1,
 "idBook": 1,
 "firstName": "First Name 1",
 "lastName": "Last Name 1"
}
```
## 23. Authors: получить данные книги (GET) с некорректным id  (более 10 символов)

1. **URL:** <https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/12345678911>
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9138589c-961e-439a-9ef1-e38a243fea9a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 03:59:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d95ae3366bdf6b4b8fb6294371dedc8f-24f168957bb6db41-00",
    "errors": {
        "idBook": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 24. Authors: получить данные автора (GET) с допустимым id
1. **URL:** {{url}}/{{auth}}/1
2. **Ожидаемый результат:** получены данные автора, код 200
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9d6baa80-2040-4605-8aaa-d8eff565d724
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
5. **Заголовки ответа:**
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 04:04:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:** 
```
{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
}
```
## 25. Authors​: получить данные автора (GET) с некорректным id  (более 10 символов)
1. **URL:** {{url}}/{{auth}}/12345678911
2. **Ожидаемый результат:** ошибка, код 400
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: efe73ee9-b2b7-4a1c-bc77-e77ebf448d55
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 08 Jun 2023 04:07:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6d21d5e94c4fda4fafabe6f00080f180-5d35377273faec4e-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 26. Authors: получить данные автора (GET) с несуществующим id 
1. **URL:** {{url}}/{{auth}}/1234567891
2. **Ожидаемый результат:** ошибка, код 404
3. **Заголовки запроса:** 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4abf4c43-f3fd-4dec-9577-60a1e493c3d4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса:**
5. **Заголовки ответа:**
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 04:09:40 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-fcad808eff87f342b79f86e4caa67da2-c561f7ffa0a1c84b-00"
}
```
## 27. Authors: изменение данных автора (PUT) с допустимым id

**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: код 200, данные об авторе изменены

**Заголовки запроса**: 
``` 
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: ec68e16c-bad9-4fb7-947a-e0e8ccd7dc9d 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive 
```
**Тело запроса**:  

```
{ 
"id": 0, 
"idBook": 0, 
"firstName": "string", 
"lastName": "string" 
} 
```

**Заголовки ответа**: 
```
Content-Type: application/json; 
charset=utf-8; v=1.0 Date: Thu, 08 Jun 2023 05:56:40 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"id":0,
"idBook":0,
"firstName":"string",
"lastName":"string"
}
```

## 28. Authors: изменение данных автора (PUT) пустые строки
**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**:
```
 Content-Type: application/json 
 User-Agent: PostmanRuntime/7.32.2 
 Accept: */* 
 Cache-Control: no-cache 
 Postman-Token: 94dc6e2b-713a-431d-bd91-27fb21fef942 
 Host: fakerestapi.azurewebsites.net 
 Accept-Encoding: gzip, deflate, br 
 Connection: keep-alive
 ```
**Тело запроса**: 
```
{
 "id":, 
 "idBook":, 
 "firstName": "string", 
 "lastName": "string" 
 }
 ```
**Заголовки ответа**:  
```
Сontent-Type: application/problem+json; 
charset=utf-8 
Date: Thu, 08 Jun 2023 06:06:27 GMT 
Server: Kestrel 
Transfer-Encoding: chunked
```

**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,"
traceId":"00-cd9c8498d294ef44b2ac7d0580a406b9-fa2fafbc8e958a43-00",
"errors":{"$.id":["',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 6."]}
}
```
## 29. Authors: изменение данных автора (PUT) с некорректным id (более 10 символов)

**URL**: {{url}}/api/v1/Authors/{{id_m10}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: ab715645-1b46-430c-a000-13d005311a72 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```

**Тело запроса**: 
```
{
 "id": 0, 
 "idBook": 0,
 "firstName": "string", 
 "lastName": "string" 
 }
 ```
**Заголовки ответа**:  
```
Сontent-Type: application/problem+json; 
charset=utf-8
 Date: Thu, 08 Jun 2023 06:11:22 GMT 
 Server: Kestrel 
 Transfer-Encoding: chunked
 ```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-4bea4cdb8d0fa248a93ebca72fe0b1a0-c27f94e374e3f44e-00","
errors":{"id":["The value '12345678911' is not valid."]}
}
```

## 30.  Authors: изменение данных автора (PUT)  с некорректным id в теле(более 10 символов)
**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: ab715645-1b46-430c-a000-13d005311a72 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 12345678911, 
 "idBook": 0, 
 "firstName": "string",
  "lastName": "string" 
  }
  ```
**Заголовки ответа**: 
```
Сontent-Type: application/problem+json; 
charset=utf-8
 Date: Thu, 08 Jun 2023 06:11:22 GMT 
 Server: Kestrel 
 Transfer-Encoding: chunked
 ```
**Тело ответа**:  
```
{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-c86dc5fb9bc0c744829e9c0b81537a72-344703325cb9eb44-00",
"errors":{"$.id":["The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 18."]}}
 ```

## 31. Authors: изменение данных автора (PUT)  некорректный JSON
**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: ab715645-1b46-430c-a000-13d005311a72 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0, 
 "idBook": 0, 
 "firstName": "string", 
 "lastName": "string"" 
 }
 ```
**Заголовки ответа**: 
```
Сontent-Type: application/problem+json; 
charset=utf-8
 Date: Thu, 08 Jun 2023 06:12:25 GMT 
 Server: Kestrel 
 Transfer-Encoding: chunked
 ```

**Тело ответа**:
``` 
{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-1e5aee583653274384e607820f8103d3-3fad587ac7a1574d-00",
"errors":{"$":["'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 8 | BytePositionInLine: 21."]}}
```

## 32. Authors: изменение данных автора (PUT)  изменение типа вносимых данных (текст на число)
**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: ab715645-1b46-430c-a000-13d005311a72 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0,
  "idBook": 0, 
  "firstName": "string", 
  "lastName": 1 
  }
  ```
**Заголовки ответа**:  
```
Сontent-Type: application/problem+json; 
charset=utf-8
 Date: Thu, 08 Jun 2023 06:15:17 GMT 
 Server: Kestrel 
 Transfer-Encoding: chunked
 ```
**Тело ответа**: 
```
{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-232571411885da49b0873a0328d5638d-5f021e0a27753545-00",
"errors":{"$.lastName":["The JSON value could not be converted to System.String. Path: $.lastName | LineNumber: 8 | BytePositionInLine: 14."]}}
```

## 33. Authors: изменение данных автора (PUT) изменение типа вносимых данных (число на текст)
**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: cf28aea-fe4d-49d4-9852-5ea5646b9a82
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": q, 
 "idBook": 0, 
 "firstName": "string", 
 "lastName": "string"
  }
  ```
**Заголовки ответа**: 
```
Сontent-Type: application/problem+json; 
charset=utf-8
 Date: Thu, 08 Jun 2023 06:20:02 GMT 
 Server: Kestrel 
 Transfer-Encoding: chunked
 ```
**Тело ответа**:  
```
{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,"traceId":"00-7d84c239e41bab438e79f86b3422b1d6-0888611213abd948-00",
"errors":{"$.id":["'q' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}}
 ```

## 34. Authors: удаление автора (DELETE​) с допустимым id
**URL**: {{url}}/api/v1/Authors/{{id_cor}}

**Ожидаемый результат**: автор удален, код 200

**Заголовки запроса**: 
 ```
 User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2382bfb1-8b6d-493d-8f10-0972ac0eb3d4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
 ```
**Заголовки ответа**: 
 ```
 Content-Length: 0 
 Date: Thu, 08 Jun 2023 06:22:26 GMT 
 Server: Kestrel 
 api-supported-versions: 1.0
  ```

## 35. Authors: удаление автора (DELETE) с некорректным id (более 10 символов)
**URL**: {{url}}/api/v1/Authors/{{id_m10}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
 ```
 User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: dcf28aea-fe4d-49d4-9852-5ea5646b9a82
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
 ```
**Заголовки ответа**: 
 ```
 Content-Length: 0 
 Date: Thu, 08 Jun 2023 06:24:16 GMT 
 Server: Kestrel 
 api-supported-versions: 1.0
  ```

## 36. Books: получение списка книг (GET)
**URL**: {{url}}/api/v1/Books

**Ожидаемый результат**: список книг получен, код 200

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: dcf28aea-fe4d-49d4-9852-5ea5646b9a82 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:25:41 GMT 
Server: Kestrel Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
 "id": 1, 
 "title": "Book 1", 
 "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n", 
 "pageCount": 100, 
 "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n", 
 "publishDate": "2023-06-07T06:25:41.0565127+00:00" 
 }
 ```

## 37. Books: добавить книгу (POST​)
**URL**: {{url}}/api/v1/Books

**Ожидаемый результат**: книга добавлена, код 200

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: dcf28aea-fe4d-49d4-9852-5ea5646b9a82 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0,
  "title": "string", 
  "description": "string", 
  "pageCount": 0,
  "excerpt": "string", 
  "publishDate": "2023-06-07T07:40:29.925Z"
  }
  ```
**Заголовки ответа**: 
```
Content-Type: application/json; 
charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 06:28:41 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"id":0,
"title":"string",
"description":"string",
"pageCount":0,
"excerpt":"string",
"publishDate":"2023-06-07T07:40:29.925Z"
}
```

## 38. Books: добавить книгу (POST​) некорректный JSON
**URL**: {{url}}/api/v1/Books

**Ожидаемый результат**: ошибка, код 415

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: dcf28aea-fe4d-49d4-9852-5ea5646b9a82 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0, 
 "title": "string"", 
 "description": "string",
  "pageCount": 0, 
  "excerpt": "string", 
  "publishDate": "2023-06-07T07:40:29.925Z"
  }
  ```
**Заголовки ответа**:  
```
Content-Type: application/json; 
charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:29:58 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.13",
"title":"Unsupported Media Type",
"status":415,
"traceId":"00-f937d42a8577d04ca4952103622ae10c-e9c07a4f76837040-00"
}
```

## 39. Books: добавить книгу (POST​)  пустые строки
**URL**: {{url}}/api/v1/Books

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: de3231d1-c75a-44e3-8e7b-62e50f6c6a05 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": , 
 "title": "string", 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string", 
 "publishDate": "2023-06-07T07:40:29.925Z"
  }
  ```
**Заголовки ответа**: 
```
Content-Type: application/json; 
charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:31:58 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-2f922ff62b7cb0408244d4d723492562-fb31a25065a36945-00",
"errors":{"$.id":["',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 8."]}
}
```

## 40 Books: добавить книгу (POST​) изменение типа вносимых данных (число на текст)
**URL**: {{url}}/api/v1/Books

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: de3231d1-c75a-44e3-8e7b-62e50f6c6a05 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": q, 
 "title": "string", 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string", 
 "publishDate": "2023-06-07T07:40:29.925Z" 
 }
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; 
charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:32:35 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**:  
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-e9baf13575690a43852d4f5ed4148f27-bb0e7e731aa01e48-00",
"errors":{"$.id":["'q' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}
}
```

## 41.  Books: добавить книгу (POST​) изменение типа вносимых данных (текст на число)
**URL**: {{url}}/api/v1/Books

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: de3231d1-c75a-44e3-8e7b-86e9fe8fd21a 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0, 
 "title": 1, 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string", 
 "publishDate": "2023-06-07T07:40:29.925Z" 
 }
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; 
charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 06:37:15 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**:  
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-f153270af1e1db41bc8936e67b3947cc-2ec2805c5993ff42-00",
"errors":{"$.title":["The JSON value could not be converted to System.String. Path: $.title | LineNumber: 2 | BytePositionInLine: 11."]}
}
```

## 42. Books: получить информацию о книге (GET) с допустимым id
**URL**: {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**: информация получена, код 200

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* Cache-Control: no-cache 
Postman-Token: de3231d1-c75a-44e3-8e7b-86e9fe8fd21a 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Заголовки ответа**: 
```
Content-Type: application/json; 
charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:45:17 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"id":1,
"title":"Book 1",
"description":"Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
"pageCount":100,
"excerpt":"Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
"publishDate":"2023-06-07T06:45:36.2133615+00:00"
}
```
## 43. Books: получить информацию о книге (GET) с некорректным id (более 10 символов)
**URL**: {{url}}/api/v1/Books/{{id_m10}}

**Ожидаемый результат**:  ошибка, код 400

**Заголовки запроса**:  
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: de3231d1-c75a-44e3-8e7b-86e9fe8fd21a 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:51:23 GMT 
Server: Kestrel Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**:  
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-00f0e2e8a789c2438c7c806af7554821-b6400734371cc548-00",
"errors":{"id":["The value '12345678911' is not valid."]}
}
```

## 44. Books: получить информацию о книге (GET) с несуществующим id
**URL**: {{url}}/api/v1/Books/{{id_incor}}

**Ожидаемый результат**: ошибка - книга не найдена, код 404

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2
 Accept: */* Cache-Control: no-cache 
 Postman-Token: 39383260-296a-45b5-b41f-cb66b69d6d31 Host: fakerestapi.azurewebsites.net 
 Accept-Encoding: gzip, deflate, br 
 Connection: keep-alive
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:55:11 GMT 
Server: Kestrel Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4",
"title":"Not Found",
"status":404,"
traceId":"00-0f1f1d26d5864a43bdaaa1bf58689880-503d91328dbe154e-00"
}
```
 
## 45. Books: изменение данных книги (PUT) с допустимым id
**URL**: {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**: данные изменены, код 200

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 39383260-296a-45b5-b41f-cb66b69d6d31 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0, 
 "title": "string", 
 "description": "string", 
 "pageCount": 0,
  "excerpt": "string", 
  "publishDate": "2023-06-07T07:57:41.571Z" 
  }
  ```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 06:59:31 GMT 
Server: Kestrel Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"id":0,
"title":"string",
"description":"string",
"pageCount":0,
"excerpt":"string",
"publishDate":"2023-06-07T07:57:41.571Z"
}
```
## 46. Books: изменение данных книги (PUT) с некорректным id (более 10 символов)
**URL**: {{url}}/api/v1/Books/{{id_m10}}

**Ожидаемый результат**:  ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 390c71b72-ef45-4a75-a2d6-0a987b1790d4 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0, 
 "title": "string", 
 "description": "string", 
 "pageCount": 0,
  "excerpt": "string", 
  "publishDate": "2023-06-07T07:57:41.571Z" 
  }
  ```
**Заголовки ответа**:
``` 
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:40:31 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```

**Тело ответа**:
 ```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-adf93d50b1cc714997be9da9960bfb94-cb536c36dfad8b43-00",
"errors":{"id":["The value '12345678911' is not valid."]}
}
```

## 47. Books: изменение данных книги (PUT) с некорректным id в теле (более 10 символов)
**URL**: {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**:  ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 390c71b72-ef45-4a75-a2d6-0a987b1790d4 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 12345678911, 
 "title": "string", 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string", 
 "publishDate": "2023-06-07T07:57:41.571Z" 
 }
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:42:51 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-95cac724ccf08042bcec3c90b75fb9e7-1a97ba60ad7cc74a-00",
"errors":{"$.id":["The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 18."]}
}
```

## 48.  Books: изменение данных книги (PUT​) некорректный JSON
**URL**:  {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**:  ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2
 Accept: */* 
 Cache-Control: no-cache 
 Postman-Token: 390c71b72-ef45-4a75-a2d6-0a987b1790d4 
 Host: fakerestapi.azurewebsites.net 
 Accept-Encoding: gzip, deflate, br 
 Connection: keep-alive
 ```
 
**Тело запроса**:
```
 { 
 "id": 0, 
 "title": "string", 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string"", 
 "publishDate": "2023-06-07T08:32:23.711Z" 
 }
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:43:50 GMT 
erver: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```

**Тело ответа**:
 ```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-7fb47c19d9fd2e448e44cfc037dc5a7a-626ab57a87203c4f-00",
"errors":{"$":["'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 10 | BytePositionInLine: 20."]}
}
```


## 49. Books: изменение данных книги (PUT​) пустые строки
**URL**: {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* Cache-Control: no-cache 
Postman-Token: 390c71b72-ef45-4a75-a2d6-0a987b1790d4 
Host: fakerestapi.azurewebsites.net
 Accept-Encoding: gzip, deflate, br 
 Connection: keep-alive
 ```
 
**Тело запроса**: 
```
{
 "id": , 
 "title": "string", 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string"", 
 "publishDate": "2023-06-07T08:47:48.792Z" 
 }
 ```
**Заголовки ответа**:
```
 Content-Type: application/json; charset=utf-8; v=1.0
 Date: Thu, 08 Jun 2023 07:46:12 GMT 
 Server: Kestrel 
 Transfer-Encoding: chunked 
 api-supported-versions: 1.0
 ```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-2e9edaa763e1c6489a8ffc8a938fd844-7a1c2a138f997243-00",
"errors":{"$.id":["',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}
}
```
## 50. Books: изменение данных книги (PUT​) изменение типа вносимых данных (текст на число)
**URL**: {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 56cf7fc6-193c-4a39-b1ef-859691c014e2 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{
 "id": 0, 
 "title": 1,
  "description": "string", 
  "pageCount": 0, 
  "excerpt": "string", 
  "publishDate": "2023-06-07T07:57:41.571Z"
   }
   ```
**Заголовки ответа**:  
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:49:16 GMT
 Server: Kestrel 
 Transfer-Encoding: chunked api-supported-versions: 1.0
 ```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-f4d7e0773f5cb747bcdce0086a324b26-f42b6a4f09abcf48-00",
"errors":{"$.title":["The JSON value could not be converted to System.String. Path: $.title | LineNumber: 4 | BytePositionInLine: 11."]}
}
```

## 51. Books: изменение данных книги (PUT​) изменение типа вносимых данных (число на текст)
**URL**: {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2
 Accept: */* 
 Cache-Control: no-cache 
 Postman-Token: 56cf7fc6-193c-4a39-b1ef-859691c014e2 
 Host: fakerestapi.azurewebsites.net 
 Accept-Encoding: gzip, deflate, br 
 Connection: keep-alive
 ```
**Тело запроса**: 
```
{
 "id": q, 
 "title": "string", 
 "description": "string", 
 "pageCount": 0, 
 "excerpt": "string", 
 "publishDate": "2023-06-07T07:57:41.571Z" 
 }
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:52:32 GMT 
Server: Kestrel 
Transfer-Encoding: chunked api-supported-versions: 1.0
```

**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-6b109571763dbb47af2cfa9fa90bd861-f936cdf6cb47d342-00","errors":{"$.id":["'q' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}
}
```
## 52. Books: удаление книги (DELETE​) с допустимым id
**URL**:  {{url}}/api/v1/Books/{{id_cor}}

**Ожидаемый результат**:  Книга удалена, код 200

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 506420cb4-0d4b-4158-95b7-9864b0e01780 
Host: fakerestapi.azurewebsites.net
 Accept-Encoding: gzip, deflate, br 
 Connection: keep-alive
 ```
**Заголовки ответа**: 
```
Content-Length: 0 
Date: Thu, 08 Jun 2023 07:53:02 GMT 
Server: Kestrel 
api-supported-versions: 1.0
```



## 53. Books: удаление книги (DELETE​) с некорректным id (более 10 символов)
**URL**: {{url}}/api/v1/Books/{{id_m10}}

**Ожидаемый результат**:  ошибка, код 400

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 56cf7fc6-193c-4a39-b1ef-859691c014e2 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Заголовки ответа**: 
```
Content-Length: 0 
Date: Thu, 08 Jun 2023 07:55:34 GMT 
Server: Kestrel api-supported-versions: 1.0
```

## 54. Cover photos: получение списка обложек книг (GET)
**URL**: {{url}}/api/v1/CoverPhotos

**Ожидаемый результат**: список получен, код 200

**Заголовки запроса**: 
```
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 56cf7fc6-193c-4a39-b1ef-859691c014e2 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:58:34 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**:
```
{
 "id": 1, 
 "idBook": 1, 
 "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
  ```



## 55. Cover photos: добавить обложку книги (POST​)
**URL**: {{url}}/api/v1/CoverPhotos

**Ожидаемый результат**: обложка добавлена, код 200

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* Cache-Control: no-cache 
Postman-Token: 871888ec-7f2e-4e3b-b2f6-fef1d10fbe15 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{ "id": 0, "idBook": 0, "url": "string" }
```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:59:20 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{"id":0,"idBook":0,"url":"string"}
```

## 56.  Cover photos: добавить обложку книги (POST​) некорректный JSON
**URL**: {{url}}/api/v1/CoverPhotos

**Ожидаемый результат**:   ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */*
 Cache-Control: no-cache 
 Postman-Token: 871888ec-7f2e-4e3b-b2f6-fef1d10fbe15
  Host: fakerestapi.azurewebsites.net 
  Accept-Encoding: gzip, deflate, br 
  Connection: keep-alive
  ```
**Тело запроса**: 
```
{ "id": 0, "idBook": 0, "url"": "string" }
```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 07:59:20 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,"traceId":"00-56c5b2699fbf564984829e73204a3608-5ca70780fac2404b-00",
"errors":{"$":["'\"' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 6 | BytePositionInLine: 6."]}}
```

## 57. Cover photos: добавить обложку книги (POST​) пустые строки
**URL**:  {{url}}/api/v1/CoverPhotos

**Ожидаемый результат**:  ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 871888ec-7f2e-4e3b-b2f6-fef1d10fbe15 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{ "id": , "idBook": 0, "url": "string" }
```

**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 08 Jun 2023 08:03:21 GMT 
Server: Kestrel 
Transfer-Encoding: chunked api-supported-versions: 1.0
```

**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-e9ee5555cca2964681d9b09f394546a2-b789285c75165e43-00",
"errors":{"$.id":["',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}
}
```


## 58. Cover photos: добавить обложку книги (POST​) изменение типа вносимых данных (текст на число)
**URL**: {{url}}/api/v1/CoverPhotos

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* Cache-Control: no-cache 
Postman-Token: 871888ec-7f2e-4e3b-b2f6-fef1d10fbe15 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**:
```
 { "id": 0, "idBook": 0, "url": 1 }
 ```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 08:10:54 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-7b0d0dfb08137c4aab8ad6c96d22bcf2-326a70106c96394c-00",
"errors":{"$.url":["The JSON value could not be converted to System.Uri. Path: $.url | LineNumber: 6 | BytePositionInLine: 9."]}
}
```
## 59. Cover photos: добавить обложку книги (POST​) изменение типа вносимых данных (число на текст)
**URL**: {{url}}/api/v1/CoverPhotos

**Ожидаемый результат**: ошибка, код 400

**Заголовки запроса**: 
```
Content-Type: application/json 
User-Agent: PostmanRuntime/7.32.2 
Accept: */* 
Cache-Control: no-cache 
Postman-Token: 871888ec-7f2e-4e3b-b2f6-fef1d10fbe15 
Host: fakerestapi.azurewebsites.net 
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive
```
**Тело запроса**: 
```
{ "id": q, "idBook": 0, "url": "string" }
```
**Заголовки ответа**: 
```
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Thu, 08 Jun 2023 08:11:32 GMT 
Server: Kestrel 
Transfer-Encoding: chunked 
api-supported-versions: 1.0
```
**Тело ответа**: 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-7314f67a798baa4982dbd7f08b83aeb6-2f04a1b70e8cc84f-00",
"errors":{"$.id":["'q' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}
}
```
## 60. Cover photos: получение обложки книги (GET) с допустимым id
1. **URL** - {{url}}/api/v1/CoverPhotos/books/covers/1
2. **Ожидаемый результат** - код 200, получена обложка
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0998cbda-f30d-491a-abb0-79d7e6e26873
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 11:04:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    }
]
```
## 61. Cover photos: получение обложки книги (GET) с некорректным id (более 10 символов)
1. **URL** - {{url}}/api/v1/CoverPhotos/books/covers/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0998cbda-f30d-491a-abb0-79d7e6e26873
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 11:24:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f9e686c5f912f243841bcee38cd4ff4e-710446799da35e41-00",
    "errors": {
        "idBook": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 62. Cover photos: получение обложки фото (GET) с допустимым id
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - код 200, получена обложка
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2a8a2a37-dd96-4481-8eba-693467a235e9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 11:33:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
{
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
## 63. Cover photos: получение обложки фото (GET) с некорректным id (более 10 символов)
1. **URL** - {{url}}/api/v1/CoverPhotos/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e47a62a7-fc2e-49be-8ab0-56f8befe1747
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 11:36:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3ee1e716df063548b7b5c07da6fc2536-9f28f2644a3e1049-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 64. Cover photos: получение обложки фото (GET) с несуществующим id
1. **URL** - {{url}}/api/v1/CoverPhotos/1234567891
2. **Ожидаемый результат** - Код 404, введённый id не найден
3. **Заголовки запроса** 
```Accept: */*
Cache-Control: no-cache
Postman-Token: 067e780d-e009-4309-aa2c-7efedc8b1bbb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 11:38:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-f8ce6ed67d5b4643a655052a51036871-51c54e63f39d6d45-00"
}
```
## 65. Cover photos: изменение обложки фото (PUT) с допустимым id
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - код 200, обложка изменена 
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 533dffae-e44f-4f0c-ac6f-8da049d5c335
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
  "id": 1,
  "idBook": 1,
  "url": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 11:40:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
{
    "id": 1,
    "idBook": 1,
    "url": "string"
}
```
## 66. Cover photos: изменение обложки фото (PUT) с пустым телом запроса
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - Код 400, неверный Json
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 30fe8190-265b-4bea-8265-c625b655b437
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 11:51:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2983fdb2ce06d3429b40b49f5314027d-209c0912e7d30345-00",
    "errors": {
        "$": [
            "The input does not contain any JSON tokens. Expected the input to start with a valid JSON token, when isFinalBlock is true. Path: $ | LineNumber: 0 | BytePositionInLine: 1."
        ]
    }
}
```
## 67. Cover photos: изменение обложки фото (PUT) с некорректным id в теле запроса (более 10 символов)
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 321eae75-b71f-424a-9f7b-038db66d9d7a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
  "id": 12345678911,
  "idBook": 12345678911,
  "url": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 11:54:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-cce96382ad44b3468c3b8d6b2bb9465e-8b6e99a364bb5041-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 19."
        ]
    }
}
```
## 68. Cover photos: изменение обложки фото (PUT) некорректный JSON
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - Код 400, неверный синаксис
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 861f18cf-9fff-4bf3-a7e8-6b1d567e51ff
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "idBook": 1,
 "url": "string""
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 11:57:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a5f11ccf53e66b47acf385dd67b3479a-1b8ad3aefa27bd40-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 16."
        ]
    }
}
```
## 69. Cover photos: изменение обложки фото (PUT) изменение типа вносимых данных
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - Код 400, неверный синтаксис
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4a40eaf5-8988-4c40-b16d-e0ad2126ea59
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": q,
 "idBook": 1,
 "url": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 11:59:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-91ba1b7c84ac74479ab8e9f432173d51-b39ac9c23dd0484d-00",
    "errors": {
        "$.id": [
            "'q' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## 70. Cover photos: изменение обложки фото (PUT) с некорректным id (более 10 символов)
1. **URL** - {{url}}/api/v1/CoverPhotos/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 98d964e6-0306-40eb-b2c9-b3b9c88426b7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "idBook": 1,
 "url": "string""
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 12:16:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4549774d1fefaa478b9bba636eed846f-9be9907c436d2e40-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 16."
        ],
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```

## 71. Cover photos: удаление обложки фото (DELETE) с допустимым id
1. **URL** - {{url}}/api/v1/CoverPhotos/1
2. **Ожидаемый результат** - Код 200, Обложка удалена
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 8d9289f7-72bc-4ba1-9a11-69d4a08259dc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Length: 0
Date: Wed, 07 Jun 2023 12:50:03 GMT
Server: Kestrel
api-supported-versions: 1.0
```
## Cover photos: удаление обложки фото (DELETE) с некорректным id (более 10 символов)
1. **URL** - {{url}}/api/v1/CoverPhotos/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f9467e23-e0d5-4995-a5ac-d56c72153e8b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 12:51:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f70f2ec3a916a34ea1dbc41230a059d9-0e4f089e6c12a64b-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 72. Users: получение информации о юзере (GET)
1. **URL** - {{url}}//api/v1/Users
2. **Ожидаемый результат** - Код 200, информация получена
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f310ba03-0ff0-490b-bb4a-966e66ec4853
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 12:54:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
[
    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
    {
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
    },
    {
        "id": 3,
        "userName": "User 3",
        "password": "Password3"
    }
}
```
## 73. Users: добавление юзера (POST) c допустимым id в теле запроса
1. **URL** - {{url}}//api/v1/Users
2. **Ожидаемый результат** - Код 200, юзер добавлен
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ac8eca16-0b2c-4ac1-8858-4651ca2e19a5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 12:57:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
{
    "id": 1,
    "userName": "string",
    "password": "string"
}
```
## 74. Users: добавление юзера (POST) с некорректным id в теле запроса (более 10 символов
1. **URL** - {{url}}//api/v1/Users
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 87ae4b2f-99da-4806-8840-6fa9b3ef0eb9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 12345678911,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:00:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-953e285b9f76bb4d8b850e2881a96f8d-2f3cc362a3c8014a-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```
## 75. Users: добавление юзера (POST) с пустым телом запроса
1. **URL** - {{url}}//api/v1/Users
2. **Ожидаемый результат** - Код 400, неверный JSON
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c8fd9787-9ac7-4d6f-9652-78f4e2bbec9c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:02:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-bdc191fd63c2a34281147fff9149aa17-5b0510ff6393244a-00",
    "errors": {
        "$": [
            "The input does not contain any JSON tokens. Expected the input to start with a valid JSON token, when isFinalBlock is true. Path: $ | LineNumber: 0 | BytePositionInLine: 1."
        ]
    }
}
```
## 76. Users: добавление юзера (POST) некорректный JSON
1. **URL** - {{url}}//api/v1/Users
2. **Ожидаемый результат** - Код 400, неверный синтаксис
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: b2782af6-82b7-4924-a346-21cc52f3c8b1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 0,
 "userName": "string",
 "password": "string""
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:04:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-545d15f46c2cca46ba1c411d754c81d8-1ce5a6ba24c0e449-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 21."
        ]
    }
}
```
## 77. Users: добавление юзера (POST) некорректный JSON цифры на буквы
1. **URL** - {{url}}//api/v1/Users
2. **Ожидаемый результат** - Код 400, неверный синтаксис
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 023a3eaa-05d3-4ade-b163-36ee910fd413
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": q,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:07:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8c4d42638007fe4287d93c9c889d67b3-7871dcc86566ad48-00",
    "errors": {
        "$.id": [
            "'q' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## 78. Users: получение информации о юзере (GET) с допустимым id
1. **URL** - {{url}}//api/v1/Users/1
2. **Ожидаемый результат** - Код 200, информация получена
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 097fd543-d7ff-4dfa-98a1-5c9c318f7f43
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 13:12:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа** 
```
{
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
}
```
## 79. Users: получение информации о юзере (GET) с несуществующим id
1. **URL** - {{url}}//api/v1/Users/1234567891
2. **Ожидаемый результат** - Код 404, информация не найдена
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a2a8491a-efa0-4078-aa3b-cfebe7f578ec
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Wed, 07 Jun 2023 13:14:06 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-4ac12f150ff12344b5121026106ed4bd-09fe6ecce7df984e-00"
}
```
## 80. Users: получение информации о юзере (GET) с некорректным id (более 10 символов
1. **URL** - {{url}}//api/v1/Users/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7071ec23-ccec-4c03-abb5-1540006ee47b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:16:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f9eff5e776d6694aaab1fc48cff1fb00-5f470a3976b29840-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 81. Users: изменение данных юзера (PUT) c допустимым id
1. **URL** - {{url}}//api/v1/Users/1 
2. **Ожидаемый результат** - Код 200, данные изменены
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7071ec23-ccec-4c03-abb5-1540006ee47b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:16:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "id": 1,
    "userName": "string",
    "password": "string"
}
```
## 82. Users: изменение данных юзера (PUT) с некорректным id в теле запроса (более 10 символов)
1. **URL** - {{url}}//api/v1/Users/1 
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2dd0b1d2-7cee-4ce9-aa59-56fa48a89a80
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 12345678911,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:20:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-395e02be703dbf40a626f0d860a8ee4c-cbba79eafef0ad40-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```
## 83. Users: изменение данных юзера (PUT) с некорректным id (более 10 символов)
1. **URL** - {{url}}//api/v1/Users/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 105acd7e-28ab-4ce0-9b64-2ddd754ab91d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:46:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9eb40647bf63aa409bfca137a5bfc698-82b1a68e66f68b44-00",
    "errors": {
        "id": [
            "The value '12345678911' is not valid."
        ]
    }
}
```
## 84. Users: изменение данных юзера (PUT) некорректный JSON
1. **URL** - {{url}}//api/v1/Users/1
2. **Ожидаемый результат** - Код 400, неверный JSON
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2e3db480-3bb2-4433-ae04-6aaf1713acb7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "userName": "string"",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:48:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b93def8cf2c29346b66720a15a582bec-02546d083ba95847-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 21."
        ]
    }
}
```
## 85. Users: изменение данных юзера (PUT) некорректный JSON
1. **URL** - {{url}}//api/v1/Users/1
2. **Ожидаемый результат** - Код 400, неверный синтаксис
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 2e3db480-3bb2-4433-ae04-6aaf1713acb7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": 1,
 "userName": "string"",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 13:48:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b93def8cf2c29346b66720a15a582bec-02546d083ba95847-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 21."
        ]
    }
}
```
## 86. Users: изменение данных юзера (PUT) изменение типа вносимых данных
1. **URL** - {{url}}//api/v1/Users/1
2. **Ожидаемый результат** - Код 400, неверный синтаксис
3. **Заголовки запроса** 
```Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5716c5c2-11f5-4416-99ae-d9f3e67cf1a7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
4. **Тело запроса**
```
{
 "id": q,
 "userName": "string",
 "password": "string"
}
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 14:17:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
6. **Тело ответа**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-898d76cdbcac9b448a661d6eb512b5b5-854bd517f2f25348-00",
    "errors": {
        "$.id": [
            "'q' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## 87. Users: удаление юзера (DELETE) с допустимым id
1. **URL** - {{url}}//api/v1/Users/1
2. **Ожидаемый результат** - Код 200, юзер удалён
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d8795512-bf8b-40ce-a667-38a61633d4f5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
5. **Заголовки ответа**
```Content-Length: 0
Date: Wed, 07 Jun 2023 14:20:23 GMT
Server: Kestrel
api-supported-versions: 1.0
```
## 88. Users: удаление юзера (DELETE) с некорректным id (более 10 символов)
1. **URL** - {{url}}//api/v1/Users/12345678911
2. **Ожидаемый результат** - Код 400, введённое значение недопустимо
3. **Заголовки запроса** 
```User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7a8bc9fb-67f3-4a32-b5c7-f7b35358ec5e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive\
```
5. **Заголовки ответа**
```Content-Type: application/problem+json; charset=utf-8
Date: Wed, 07 Jun 2023 14:21:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
```







