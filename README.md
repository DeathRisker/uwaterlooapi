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
[__GET /courses__](courses/courses.md)

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
