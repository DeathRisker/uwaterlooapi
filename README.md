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
### [Login](login/login.md)


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
