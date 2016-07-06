__GET /courses__ Returns a collection of courses' id and name

Request body:
```
{
  'Cookie': {learn_cookies}
}
```

Example Result:
```
[
  {
    "courseName": "My Course 1",
    "courseID": "10000"
  },
  {
    "courseName": "My Course 2",
    "courseID": "10001"
  }
  ...
]
```
__Error code:__

| Code        | Type           | Reason  |
| ------------- |:-------------:| -----:|
| 400      | Bad Request | Missing `Cookie` in request body|
| 401      | Unauthorized      |   Incorrect cookie or cookie expired |
| 503 | Connection Error| Unable to connect to server |
