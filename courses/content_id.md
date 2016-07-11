### Content
__GET /courses/{courseID}/{contentID}__ Returns content information specified by IDs

Request Header:
```
{
  'Cookie': {learn_cookies}
}
```

Example Result:
```
{
  "files": [
    {
      "downloadURL": "https://learn.uwaterloo.ca/d2l/le/content/33088/topics/files/download/715250/DirectFileTopicDownload",
      "fileType": "docx",
      "fileID": "715250",
      "fileName": "201213PROGRAMBrochure-1-acting"
    },
    {
      "downloadURL": "https://learn.uwaterloo.ca/d2l/le/content/33088/topics/files/download/826586/DirectFileTopicDownload",
      "fileType": "pdf",
      "fileID": "826586",
      "fileName": "SuccessCoachingWorkshopsWinter2014"
    },
    {
      "downloadURL": "https://learn.uwaterloo.ca/d2l/le/content/33088/topics/files/download/826587/DirectFileTopicDownload",
      "fileType": "pdf",
      "fileID": "826587",
      "fileName": "TutorConnectPoster-2"
    },
    {
      "downloadURL": "https://learn.uwaterloo.ca/d2l/le/content/33088/topics/files/download/826588/DirectFileTopicDownload",
      "fileType": "pdf",
      "fileID": "826588",
      "fileName": "StudySessionsPosterWinter2014"
    },
    {
      "downloadURL": "https://learn.uwaterloo.ca/d2l/le/content/33088/topics/files/download/875657/DirectFileTopicDownload",
      "fileType": "pdf",
      "fileID": "875657",
      "fileName": "exam drop-in Math TC"
    }
  ],
  "contentID": "715246"
}
```
