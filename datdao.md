- guide: https://jasonwatmore.com/post/2018/08/06/nodejs-jwt-authentication-tutorial-with-example-api
- express-jwt: https://www.npmjs.com/package/express-jwt
- code
  - use middleware: jwt
  - api route: /users
```bash
tree -I node_modules
.
├── _helpers
│   ├── error-handler.js
│   └── jwt.js
├── config.json
├── server.js
└── users
    ├── user.service.js
    └── users.controller.js

2 directories, 11 files
```
- request
```bash
url: http://localhost:4000/users/authenticate
header:
----------------------
X-Powered-By: Express
Access-Control-Allow-Origin: *
Content-Type: application/json; charset=utf-8
Content-Length: 190
ETag: W/"be-jAR1aWhEJAQQ42n6u6cAsak734k"
Date: Mon, 04 Jan 2021 06:43:41 GMT
Connection: keep-alive
----------------------
body:
----------------------
{
    "username": "test",
    "password": "test"
}
```
```bash
url: http://localhost:4000/users
header:
----------------------
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOjEsImlhdCI6MTYwOTc0MjAzNX0.URPyx2OGtI6Nv2DSUpl35VhPOskUeam9yW5yl9BSGfo
Content-Type: application/json
User-Agent: PostmanRuntime/7.26.8
Accept: */*
Postman-Token: ca6e3553-0b56-4b6f-85a3-9a4f88a2f3a4
Host: localhost:4000
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 50
```