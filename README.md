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
- [__POST /getLearnCookie__](login/login.md)
- [__POST /getPortalCookie__](login/login.md)

### Learn Courses Information
- [__GET /courses__](courses/courses.md)
- [__GET /courses/{courseID}__](courses/course_id.md)
