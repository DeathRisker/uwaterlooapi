__GET /courses/{courseID}__ Returns course information specified by ID

Request Header:
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
