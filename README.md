# UWaterloo Magic API (v1.0)
### Features:
- [x] Login to Learn
- [x] Login to Portal
- [x] Portal Crowd Report Service
- [x] Fetch courses resources from Learn

### Make an API call
`
https://0mcv9x2by9.execute-api.us-west-2.amazonaws.com/beta/{endpoint_path}
`
with __request header__:

`x-api-key: PuA2B7LWGw1Af7CRdC9sD2jbzMzdEHJW3QitNgT6`

## Endpoints
### Login
1. __POST */getLearnCookie*__
2. __POST */getPortalCookie*__

Call this endpoint to get the Learn or Portal cookies

__Request body__:
```
{
  'userid': WATIAM_ID,
  'password': password
}
```

__Example Result__
```
{
  "Cookie": "CASTGC=TGT-1099336-gko7dZ4TgEAf1OvcarEHQeGl5EyKvmy2tKcWmI2xBKCepD3or5-cas;JSESSIONID=097800E29FFF2DDFF59C30BD7EE63AB5;ShibbolethSSO=LE;d2lSecureSessionVal=5XTAM9YINb0HGs92nwrQrtD3W;d2lSessionVal=hLScSsI5Wds2Vt0KEwarkmVmO"
}
```
__Error code:__

| Code        | Type           | Reason  |
| ------------- |:-------------:| -----:|
| 400      | Bad Request | Missing parameters |
| 401      | Unauthorized      |   Incorrect login credentials |
| 404 | Unknown      |  Unknown error occurred |
| 503 | Connection Error| Unable to connect to server |

### Learn Courses Information
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

__GET /courses/{courseID}__ Returns course information specified by ID
Request body:
```
{
  'Cookie': {learn_cookies}
}
```
Example Result:
```
{
  "courseID": "33088",
  "tableContents": [
  {
    "contentName": "Office Hours",
    "parentCourseID": "33088",
    "contentID": "619504"
  },
  {
    "contentName": "Actsc Waitlist",
    "parentCourseID": "33088",
    "contentID": "619508"
  },
  {
    "contentName": "Info Sessions",
    "parentCourseID": "33088",
    "contentID": "715246"
  }
  ...
  ]
}
```
__Error code:__

| Code        | Type           | Reason  |
| ------------- |:-------------:| -----:|
| 403      | Forbidden | Incorrect cookie or cookie expired or wrong course id|
