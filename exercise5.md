## Activities

**1. GET /api/v1/Activities**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Activities

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-08-19T09:37:14.3525537+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-08-19T10:37:14.3525558+00:00",
    "completed": true
  },...
```

**2. POST /api/v1/Activities**

- **HTTP-метод**: POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Activities

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":1,\"title\":\"str\",\"dueDate\":\"2023-08-19T07:44:39.673Z\",\"completed\":true}"

- **Тело запроса:**

```plaintext
{
  "id": 1,
  "title": "str",
  "dueDate": "2023-08-19T07:44:39.673Z",
  "completed": true
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 1,
  "title": "str",
  "dueDate": "2023-08-19T07:44:39.673Z",
  "completed": true
}
```

**3. POST /api/v1/Activities**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Activities

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": str,  \"title\": \"str\",  \"dueDate\": \"2023-08-19T07:44:39.673Z\",  \"completed\": true}"

- **Тело запроса:**

```plaintext
{
  "id": str,
  "title": "str",
  "dueDate": "2023-08-19T07:44:39.673Z",
  "completed": true
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-465441c868f6ba499d93879cf07ffe7f-cd95c7bbce882549-00",
  "errors": {
    "$.id": [
      "'s' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
    ]
  }
}
```

**4. GET /api/v1/Activities/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Activities/5

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
{
  "id": 5,
  "title": "Activity 5",
  "dueDate": "2023-08-19T13:44:12.1309451+00:00",
  "completed": false
}
```

**5. GET /api/v1/Activities/{id}**

- **HTTP-метод:** GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/50

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 404
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-c86a36205bad184180d499aa40d73750-97d210757d36cd44-00"
}
```

**6. PUT /api/v1/Activities/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:**https://fakerestapi.azurewebsites.net/api/v1/Activities/5

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":5,\"title\":\"string\",\"dueDate\":\"2023-08-19T08:50:39.014Z\",\"completed\":true}"

- **Тело запроса:**

```plaintext
{
  "id": 5,
  "title": "string",
  "dueDate": "2023-08-19T08:50:39.014Z",
  "completed": true
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 5,
  "title": "string",
  "dueDate": "2023-08-19T08:50:39.014Z",
  "completed": true
}
```

**7. PUT /api/v1/Activities/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Activities/50

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": 50!,  \"title\": \"string\",  \"dueDate\": \"2023-08-19T08:50:39.014Z\",  \"completed\": true}"

- **Тело запроса:**

```plaintext
{
  "id": 50!,
  "title": "string",
  "dueDate": "2023-08-19T08:50:39.014Z",
  "completed": true
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b4930d39cf8c754cab82834428056253-8595c44464802347-00",
  "errors": {
    "$.id": [
      "'!' is an invalid end of a number. Expected a delimiter. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."
    ]
  }
}
```

**8. DELETE /api/v1/Activities/{id}**

- **HTTP-метод:** DELETE
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Activities/50

- **Заголовки запроса:** "accept: */*"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:** нет

## Authors

**9. GET /api/v1/Authors**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },...
```

**10. POST /api/v1/Authors**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"idBook\":0,\"firstName\":\"string\",\"lastName\":\"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

- Статус-код ответа: 200
- Тело ответа:

```plaintext
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

**11. POST /api/v1/Authors**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": 0!!,  \"idBook\": 0,  \"firstName\": \"string\",  \"lastName\": \"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0!!,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

- Статус-код ответа: 400
- Тело ответа:

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b59265f85521bd4a81e7bea775b7abd1-e465fb6813ae4749-00",
  "errors": {
    "$.id": [
      "'!' is an invalid end of a number. Expected a delimiter. Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
    ]
  }
}
```

**12. GET /api/v1/Authors/authors/books/{idBook}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/5

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса**: нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
[
  {
    "id": 14,
    "idBook": 5,
    "firstName": "First Name 14",
    "lastName": "Last Name 14"
  },
  {
    "id": 15,
    "idBook": 5,
    "firstName": "First Name 15",
    "lastName": "Last Name 15"
  },
  {
    "id": 16,
    "idBook": 5,
    "firstName": "First Name 16",
    "lastName": "Last Name 16"
  },
  {
    "id": 17,
    "idBook": 5,
    "firstName": "First Name 17",
    "lastName": "Last Name 17"
  }
]
```

**13. GET /api/v1/Authors/authors/books/{idBook}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/555555555555

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6d736857e737a244ac3133ba63709340-cb2609a2a62c4546-00",
  "errors": {
    "idBook": [
      "The value '555555555555' is not valid."
    ]
  }
}
```

**14. GET /api/v1/Authors/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/5

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 5,
  "idBook": 2,
  "firstName": "First Name 5",
  "lastName": "Last Name 5"
}
```

**15. GET /api/v1/Authors/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/55555555555

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-fcadbcc20b2dfe4e8779ceef4ab2e139-44c61cb231f2e942-00",
  "errors": {
    "id": [
      "The value '55555555555' is not valid."
    ]
  }
}
```



**16. PUT /api/v1/Authors/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/5

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"idBook\":0,\"firstName\":\"string\",\"lastName\":\"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

**17. PUT /api/v1/Authors/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/5

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": def,  \"idBook\": 0,  \"firstName\": \"string\",  \"lastName\": \"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": def,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-97b179148e6525478731e9353f785a16-7e9ffc4454d8aa4d-00",
  "errors": {
    "$.id": [
      "'d' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
    ]
  }
}
```

**18. DELETE /api/v1/Authors/{id}**

- **HTTP-метод:** DELETE
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Authors/5

- **Заголовки запроса:** accept: */*

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:** нет

## Books

**19. GET /api/v1/Books**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
esponse body
Download
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-08-18T22:18:48.4289383+00:00"
  },
  {
    "id": 2,
    "title": "Book 2",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 200,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-08-17T22:18:48.4289546+00:00"
  },...
```

**20. POST /api/v1/Books**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"title\":\"string\",\"description\":\"string\",\"pageCount\":0,\"excerpt\":\"string\",\"publishDate\":\"2023-08-19T22:21:37.758Z\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-19T22:20:56.866Z"
}
```

- Статус-код ответа: 200
- Тело ответа:

```plaintext
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-19T22:21:37.758Z"
}
```

**21. POST /api/v1/Books**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": ыек,  \"title\": \"string\",  \"description\": \"string\",  \"pageCount\": 0,  \"excerpt\": \"string\",  \"publishDate\": \"2023-08-19T22:21:37.758Z\"}"

- **Тело запроса:**

```plaintext
{
  "id": ыек,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-19T22:24:24.364Z"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-2135d829739cf147908bb3aa425e3e50-880d33157a72a249-00",
  "errors": {
    "$.id": [
      "'0xD1' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
    ]
  }
}
```

**22. GET /api/v1/Books/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books/5

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 5,
  "title": "Book 5",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 500,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-08-14T22:25:34.9753875+00:00"
}
```

**23. GET /api/v1/Books/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books/0000000000000000

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 404
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-149caaebdbecaa4e9439aebea5cfa0a3-9450e446b6c60949-00"
}
```

**24. PUT /api/v1/Books/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books/2

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"title\":\"string\",\"description\":\"string\",\"pageCount\":0,\"excerpt\":\"string\",\"publishDate\":\"2023-08-19T22:28:32.168Z\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-19T22:28:32.168Z"
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-08-19T22:28:32.168Z"
}
```

**25. PUT /api/v1/Books/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса**: https://fakerestapi.azurewebsites.net/api/v1/Books/22222222222

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":2,\"title\":\"str\",\"description\":\"string\",\"pageCount\":7777,\"excerpt\":\"string\",\"publishDate\":\"2023-08-19T22:28:32.168Z\"}"
- **Тело запроса:**

```plaintext
{
  "id": 2,
  "title": "str",
  "description": "string",
  "pageCount": 7777,
  "excerpt": "string",
  "publishDate": "2023-08-19T22:28:32.168Z"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-94ea05c641cd6c4f9230cc1c3f331935-e284a84fb382c74d-00",
  "errors": {
    "id": [
      "The value '22222222222' is not valid."
    ]
  }
}
```

**26. DELETE /api/v1/Books/{id}**

- **HTTP-метод:** DELETE
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Books/2

- **Заголовки запроса: **"accept: */*"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:** нет

## CoverPhotos

**27. GET /api/v1/CoverPhotos**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- **Заголовки запроса:**  "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
	
Response body
Download
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },...
```

**28. POST /api/v1/CoverPhotos**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- **Заголовки запроса:** “accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"idBook\":0,\"url\":\"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

**29. POST /api/v1/CoverPhotos**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": ыек,  \"idBook\": 0вап,  \"url\": \"string\"}"   

- **Тело запроса:**

```plaintext
{
  "id": ыек,
  "idBook": 0вап,
  "url": "string"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-2b9e52043377844382cf02296aa7493b-01bb6bdc7760714e-00",
  "errors": {
    "$.id": [
      "'0xD1' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
    ]
  }
}
```

**30. GET /api/v1/CoverPhotos/books/covers/{idBook}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/3

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
[
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  }
]
```

**31. GET /api/v1/CoverPhotos/books/covers/{idBook}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/33333333333333

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа**: 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-04f1a90761eb1542b830b532ec465279-1e50ad0fe729ef44-00",
  "errors": {
    "idBook": [
      "The value '33333333333333' is not valid."
    ]
  }
}
```

**32. GET /api/v1/CoverPhotos/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/6

- **Заголовки запроса:**  "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 6,
  "idBook": 6,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 6&w=250&h=350"
}
```

**33. GET /api/v1/CoverPhotos/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/6000000000000000

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-4134a5630895eb43b522849e21af8429-11d33aa681a71f48-00",
  "errors": {
    "id": [
      "The value '6000000000000000' is not valid."
    ]
  }
}
```

**34. PUT /api/v1/CoverPhotos/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10

- **Заголовки запроса:**  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":10,\"idBook\":0,\"url\":\"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 10,
  "idBook": 0,
  "url": "string"
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 10,
  "idBook": 0,
  "url": "string"
}
```

**35. PUT /api/v1/CoverPhotos/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:**https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10

- **Заголовки запроса:** "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": 1111ыва,  \"idBook\": 0,  \"url\": \"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 1111ыва,
  "idBook": 0,
  "url": "string"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-59e0561b3e7f1f499b82a9d71c6ba154-a32deb1c369b344a-00",
  "errors": {
    "$.id": [
      "'0xD1' is an invalid end of a number. Expected a delimiter. Path: $.id | LineNumber: 1 | BytePositionInLine: 12."
    ]
  }
}
```



**36. DELETE /api/v1/CoverPhotos/{id}**

- **HTTP-метод:** DELETE
- **Полный URL запроса:**https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/111

- **Заголовки запроса:** "accept: */*"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:** нет

## Users

**37. GET /api/v1/Users**

- **HTTP-метод:** GET
- **Полный URL запроса:**https://fakerestapi.azurewebsites.net/api/v1/Users

- **Заголовки запроса:** "accept: text/plain; v=1.0"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
	
Response body
Download
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
  },...
```

**38. POST /api/v1/Users**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Users

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"userName\":\"string\",\"password\":\"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

- Статус-код ответа: 200
- Тело ответа:

```plaintext
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

**39. POST /api/v1/Users**

- **HTTP-метод:** POST
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Users

- **Заголовки запроса:**  "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": ttt,  \"userName\": \"string\",  \"password\": \"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": ttt,
  "userName": "string",
  "password": "string"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-36ffdd30046e384cabdba2a71cceecd3-ed33314ac3cb554a-00",
  "errors": {
    "$.id": [
      "'ttt,\n  \"userName\": \"string\",\n  \"password\": \"string\"\n}' is an invalid JSON literal. Expected the literal 'true'. Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
    ]
  }
}
```

**40. GET /api/v1/Users/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса**:https://fakerestapi.azurewebsites.net/api/v1/Users/4

- **Заголовки запроса:** "accept: */*"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 4,
  "userName": "User 4",
  "password": "Password4"
}
```

**41. GET /api/v1/Users/{id}**

- **HTTP-метод:** GET
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Users/4444444444444444

- **Заголовки запроса:** "accept: */*"

- **Тело запроса:** нет
- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-260570f13d6d79409a9555a840d87991-efcd18b1ed09a640-00",
  "errors": {
    "id": [
      "The value '4444444444444444' is not valid."
    ]
  }
}
```

**42. PUT /api/v1/Users/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Users/7

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{\"id\":0,\"userName\":\"string\",\"password\":\"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

- **Статус-код ответа:** 200
- **Тело ответа:**

```plaintext
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

**43. PUT /api/v1/Users/{id}**

- **HTTP-метод:** PUT
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Users/7

- **Заголовки запроса:** "accept: */*" -H  "Content-Type: application/json; v=1.0" -d "{  \"id\": def,  \"userName\": \"string\",  \"password\": \"string\"}"

- **Тело запроса:**

```plaintext
{
  "id": def,
  "userName": "string",
  "password": "string"
}
```

- **Статус-код ответа:** 400
- **Тело ответа:**

```plaintext
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-216abdd976f8fb4d9646484e79bfeca0-7c305b9744c03e4c-00",
  "errors": {
    "$.id": [
      "'d' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
    ]
  }
}
```

**44. DELETE /api/v1/Users/{id}**

- **HTTP-метод:** DELETE
- **Полный URL запроса:** https://fakerestapi.azurewebsites.net/api/v1/Users/2

- **Заголовки запроса:** "accept: */*"

- **Тело запроса:** нет
- **Статус-код ответа:** 200
- **Тело ответа:** нет