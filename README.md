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
- [__GET /courses/{courseID}/{contentID}__](courses/content_id.md)

### Portal Services:
##### 1. CrowdReport
- [__GET /crowdReport?locationID={location_id}__](crowd_report/crowd_report.md#1-get-a-location-crowdness) Get a location crowdness
- [__POST /crowdReport?locationID={location_id}__](crowd_report/crowd_report.md#2-update-the-crowdness-of-a-location) Report crowdness of a location

##### 2. Watcard
- [__POST /watcard/balance__](watcard/watcard.md#1-check-balance)
- [__POST /watcard/transaction__](watcard/watcard.md#2-view-transaction-history)
- [__POST /watcard/reset__](watcard/watcard.md#4-reset-pin)
