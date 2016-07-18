## Crowd Report
### 1. Get a location crowdness
__GET /crowdReport?locationID={location_id}__

Request Header:
```
{
  'Cookie': {portal_cookies}
}
```


Example Result:
```
{
  "title": "PAS central seating area  - PAS 2117",
  "value": 0,
  "alias": "PAS|PAS seats",
  "locationid": 28,
  "time": "/Date(1435255445303)/",
  "id": 28
}
```
### 2. Update the crowdness of a location
__POST /crowdReport__

URL parameters: __locationID = location id__, __value = [0,50,100]__

Request Header:
```
{
  'Cookie': {portal_cookies}
}
```

Example Result:
```
Successfully reported to server
```

__Error code:__

| Code        | Type           | Reason  |
| ------------- |:-------------:| -----:|
| 400      | Bad Request | Missing parameters |
| 404 | Not found      |  Location not found |
| 418 | Cookie Expired     |  Cookie expired |
| 429 | Too many requests    |  too many requests to one building |
| 503 | Connection Error| Unable to connect to server |

List of available buildings:
```
[
  {
    "locationid": 1,
    "title": "Weight room (CIF)"
  },
  {
    "locationid": 2,
    "title": "Weight room (PAC)"
  },
  {
    "locationid": 3,
    "title": "Pool (PAC)"
  },
  {
    "locationid": 4,
    "title": "Big gym (PAC)"
  },
  {
    "locationid": 5,
    "title": "BookStore (SCH)"
  },
  {
    "locationid": 6,
    "title": "Tim Hortons (DC)"
  },
  {
    "locationid": 7,
    "title": "Tim Hortons (ML)"
  },
  {
    "locationid": 8,
    "title": "Williams Fresh Café (EV3)"
  },
  {
    "locationid": 9,
    "title": "Computer Help & Information Place - CHIP (EC2)"
  },
  {
    "locationid": 10,
    "title": "Bombshelter (SLC)"
  },
  {
    "locationid": 11,
    "title": "Brubakers (SLC)"
  },
  {
    "locationid": 12,
    "title": "Subway (SLC)"
  },
  {
    "locationid": 13,
    "title": "Great Hall (SLC)"
  },
  {
    "locationid": 14,
    "title": "Bon Appetit (DC)"
  },
  {
    "locationid": 16,
    "title": "Environment Courtyard (EV1)"
  },
  {
    "locationid": 17,
    "title": "ES Coffee Shop (EV1 - 138)"
  },
  {
    "locationid": 18,
    "title": "EV3 Corridor (3838)"
  },
  {
    "locationid": 19,
    "title": "EV3 4214/4212"
  },
  {
    "locationid": 20,
    "title": "EV2 2802"
  },
  {
    "locationid": 21,
    "title": "Tim Hortons (SCH)"
  },
  {
    "locationid": 22,
    "title": "PAS Lounge (3rd floor)"
  },
  {
    "locationid": 23,
    "title": "Hagey Hall AFM Lounge – HH 2101"
  },
  {
    "locationid": 24,
    "title": "Modern Languages Café (ML)"
  },
  {
    "locationid": 25,
    "title": "Arts Lecture Hall computer area (AL 107A)"
  },
  {
    "locationid": 26,
    "title": "PoliSci lounge - HH 341"
  },
  {
    "locationid": 27,
    "title": "Arts Lecture Hall foyer (AL)"
  },
  {
    "locationid": 28,
    "title": "PAS central seating area  - PAS 2117"
  },
  {
    "locationid": 29,
    "title": "St. Jerome’s Atrium"
  },
  {
    "locationid": 30,
    "title": "Arts Quad benches"
  },
  {
    "locationid": 31,
    "title": "Dana Porter Library – 1st floor (by Rare Book room)"
  },
  {
    "locationid": 32,
    "title": "Dana Porter Library – main floor computers"
  },
  {
    "locationid": 33,
    "title": "Dana Porter Library – main floor printer area"
  },
  {
    "locationid": 34,
    "title": "Dana Porter Library – 3rd floor computers"
  },
  {
    "locationid": 35,
    "title": "Dana Porter Library – 5th floor computers"
  },
  {
    "locationid": 36,
    "title": "Dana Porter Library – 6th floor (quiet floor)"
  },
  {
    "locationid": 37,
    "title": "Dana Porter Library – 7th floor (quiet floor)"
  },
  {
    "locationid": 38,
    "title": "Dana Porter Library – 8th floor (silent floor)"
  },
  {
    "locationid": 39,
    "title": "Dana Porter Library – 9th floor (quiet floor)"
  },
  {
    "locationid": 40,
    "title": "Dana Porter Library – 10th floor (group student floor)"
  },
  {
    "locationid": 41,
    "title": "Davis Centre Library – Silent study carrels"
  },
  {
    "locationid": 42,
    "title": "Davis Centre Library – Silent study room"
  },
  {
    "locationid": 43,
    "title": "Davis Centre Library – Main floor computers"
  },
  {
    "locationid": 44,
    "title": "Davis Centre Library – Main floor printers"
  },
  {
    "locationid": 45,
    "title": "Musagetes Architecture Library"
  },
  {
    "locationid": 46,
    "title": "Witer Learning Resource Centre"
  },
  {
    "locationid": 47,
    "title": "POETS (CPH)"
  },
  {
    "locationid": 48,
    "title": "Engineering Machine Shop (E5)"
  },
  {
    "locationid": 49,
    "title": "Engineering C&D (CPH)"
  },
  {
    "locationid": 50,
    "title": "Media.Doc Center (MC)"
  },
  {
    "locationid": 51,
    "title": "Math Coffee & Donut (MC)"
  },
  {
    "locationid": 52,
    "title": "Math Comfy Lounge (MC)"
  },
  {
    "locationid": 53,
    "title": "MathSoc Office (MC)"
  },
  {
    "locationid": 54,
    "title": "Math Undergraduate Office (MC)"
  },
  {
    "locationid": 55,
    "title": "Math Tutorial Centre (MC)"
  },
  {
    "locationid": 56,
    "title": "5th Floor Study Areas (MC)"
  },
  {
    "locationid": 57,
    "title": "6th Floor Study Areas (MC) "
  },
  {
    "locationid": 58,
    "title": "Tim Hortons Express (DC) "
  },
  {
    "locationid": 59,
    "title": "CS Advising Office (DC)"
  },
  {
    "locationid": 60,
    "title": "Math Atrium (M3)"
  },
  {
    "locationid": 61,
    "title": "1st Floor Group Study Space (M3)"
  },
  {
    "locationid": 62,
    "title": "1st Floor Silent Study Space (M3)"
  },
  {
    "locationid": 63,
    "title": "2nd Floor Study Areas (M3)"
  },
  {
    "locationid": 64,
    "title": "Math/Business Program Office (M3)"
  },
  {
    "locationid": 65,
    "title": "3rd Floor Study Areas (M3)"
  },
  {
    "locationid": 66,
    "title": "4th Floor Study Areas (M3)"
  },
  {
    "locationid": 67,
    "title": "Actuarial Science and Statistics Advising Office (M3)"
  },
  {
    "locationid": 68,
    "title": "Festival Room (SCH)"
  },
  {
    "locationid": 69,
    "title": "Campus Bubble (SLC)"
  },
  {
    "locationid": 70,
    "title": "CEIT Cafe (EIT)"
  },
  {
    "locationid": 71,
    "title": "Mudie's Village 1 (V1)"
  },
  {
    "locationid": 72,
    "title": "Pastry Plus (NH)"
  },
  {
    "locationid": 73,
    "title": "Revelation (REV)"
  },
  {
    "locationid": 74,
    "title": "The Dispensary (PHR)"
  },
  {
    "locationid": 75,
    "title": "Eye Opener Cafe (OPT)"
  },
  {
    "locationid": 76,
    "title": "Wasabi (SLC)"
  },
  {
    "locationid": 77,
    "title": "University Club (UC)"
  },
  {
    "locationid": 78,
    "title": "Pastry Plus (TC)"
  },
  {
    "locationid": 79,
    "title": "Pastry Plus (BMH)"
  },
  {
    "locationid": 80,
    "title": "IST Service Desk (EC2)"
  },
  {
    "locationid": 81,
    "title": "PAS Lounge (PAS)"
  },
  {
    "locationid": 82,
    "title": "BMH Lounge"
  },
  {
    "locationid": 83,
    "title": "Fireplace Lounge (BMH)"
  },
  {
    "locationid": 84,
    "title": "Computer Lab (BMH)"
  },
  {
    "locationid": 85,
    "title": "Liquid Assets (HH)"
  },
  {
    "locationid": 86,
    "title": "3rd floor quiet study room (SLC)"
  },
  {
    "locationid": 87,
    "title": "International News (SLC)"
  },
  {
    "locationid": 88,
    "title": "Tim Hortons (SLC)"
  },
  {
    "locationid": 89,
    "title": "CIBC (SLC)"
  },
  {
    "locationid": 90,
    "title": "Turnkey Desk (SLC)"
  },
  {
    "locationid": 91,
    "title": "Grad House (GH)"
  },
  {
    "locationid": 92,
    "title": "Browsers café (DP)"
  },
  {
    "locationid": 93,
    "title": "Tim Hortons (UWP)"
  },
  {
    "locationid": 94,
    "title": "Grand Commons (UWP)"
  },
  {
    "locationid": 95,
    "title": "UW Farm Market (SLC)"
  },
  {
    "locationid": 96,
    "title": "Renison Great Hall (REN)"
  },
  {
    "locationid": 97,
    "title": "Lusi Wong Library (REN)"
  },
  {
    "locationid": 98,
    "title": "Renison Ministry Centre (REN)"
  },
  {
    "locationid": 99,
    "title": "Math Advising Office (MC 4018F)"
  },
  {
    "locationid": 100,
    "title": "General Use Lab 1 (EV2 1011)"
  },
  {
    "locationid": 101,
    "title": "General Use Lab 2 (EV1-136)"
  },
  {
    "locationid": 102,
    "title": "Village 1 (V1) Cafeteria lineup"
  },
  {
    "locationid": 103,
    "title": "Ron Eydt Village (REV) Cafeteria lineup"
  },
  {
    "locationid": 104,
    "title": "Village 1 (V1) Laundry machines"
  },
  {
    "locationid": 105,
    "title": "Ron Eydt Village (REV) Laundry machines"
  },
  {
    "locationid": 106,
    "title": "Minota Hagey (MH) laundry machines"
  },
  {
    "locationid": 107,
    "title": "MKV laundry machines"
  },
  {
    "locationid": 108,
    "title": "Columbia Lake Village (CLV) laundry machines"
  },
  {
    "locationid": 109,
    "title": "UWP Eby Hall laundry machines"
  },
  {
    "locationid": 110,
    "title": "UWP Beck Hall laundry machines"
  },
  {
    "locationid": 111,
    "title": "UWP Wellesley court north laundry machines"
  },
  {
    "locationid": 112,
    "title": "UWP Wellesley court south laundry machines"
  },
  {
    "locationid": 113,
    "title": "UWP Wilmot court north laundry machines"
  },
  {
    "locationid": 114,
    "title": "UWP Wilmot court south laundry machines"
  },
  {
    "locationid": 115,
    "title": "UWP Woolwich court north laundry machines"
  },
  {
    "locationid": 116,
    "title": "UWP Woolwich court south laundry machines"
  },
  {
    "locationid": 117,
    "title": "UWP Waterloo court north laundry machines"
  },
  {
    "locationid": 118,
    "title": "UWP Waterloo court south laundry machines"
  },
  {
    "locationid": 119,
    "title": "Registrar's Office - Undergrad (NH)"
  },
  {
    "locationid": 120,
    "title": "Student Success Office (SCH)"
  },
  {
    "locationid": 121,
    "title": "AccessAbility Services (NH)"
  },
  {
    "locationid": 122,
    "title": "Media.Doc & Campus Tech (SLC)"
  },
  {
    "locationid": 123,
    "title": "Media.Doc Centre (EIT)"
  },
  {
    "locationid": 124,
    "title": "Media.Doc Centre (DC)"
  },
  {
    "locationid": 125,
    "title": "Media.Doc Centre (DP)"
  },
  {
    "locationid": 126,
    "title": "Writing Centre (SCH)"
  },
  {
    "locationid": 127,
    "title": "Science C&D (B1)"
  },
  {
    "locationid": 128,
    "title": "Haunted House (Physics) - Tuesday, Sept 8"
  },
  {
    "locationid": 129,
    "title": "Hypnotist Show (HH Theatre) - Tuesday, Sept 8"
  },
  {
    "locationid": 130,
    "title": "Monte Carlo (SLC) - Thursday, Sept 10"
  },
  {
    "locationid": 131,
    "title": "Monte Carlo (PAC) - Thursday, Sept 10"
  },
  {
    "locationid": 132,
    "title": "Improv \"Bizprov\" (M3) - Saturday, Sept 12"
  },
  {
    "locationid": 133,
    "title": "Magician show (M3) - Saturday, Sept 12"
  },
  {
    "locationid": 134,
    "title": "Carnival (Warrior Field) - Saturday, Sept 12"
  },
  {
    "locationid": 135,
    "title": "Toga at Twilight (BMH Green) - Saturday, Sept 12"
  },
  {
    "locationid": 136,
    "title": "Warrior Welcome (PAC) - Sunday, Sept 6"
  },
  {
    "locationid": 137,
    "title": "Warrior Welcome (PAC) - Monday, Sept 6"
  },
  {
    "locationid": 138,
    "title": "Feds Used Books (SLC)"
  },
  {
    "locationid": 139,
    "title": "St Jerome's Cafeteria (SJU)"
  },
  {
    "locationid": 140,
    "title": "Parking Services Office (COM)"
  },
  {
    "locationid": 141,
    "title": "Fed Hall - student study space (FED)"
  },
  {
    "locationid": 142,
    "title": "Davis Centre Library IT Service Desk (DC)"
  },
  {
    "locationid": 143,
    "title": "Arts Computing Office (PAS)"
  },
  {
    "locationid": 144,
    "title": "Computer Science Help Desk (DC)"
  },
  {
    "locationid": 145,
    "title": "Engineering Computing"
  },
  {
    "locationid": 146,
    "title": "Math Faculty Computing Facility (MC)"
  },
  {
    "locationid": 147,
    "title": "Environment Computing (EV2)"
  },
  {
    "locationid": 148,
    "title": "Applied Health Services Computing (BMH)"
  },
  {
    "locationid": 149,
    "title": "Student Accounts (NH)"
  },
  {
    "locationid": 150,
    "title": "Starbucks (STC)"
  },
  {
    "locationid": 151,
    "title": "Velocity Start (SCH)"
  }
]
```
