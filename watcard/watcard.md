### WatCard Service
#### 1. Check balance
__POST /watcard/balance__

Request body:
```
{
  "id": watcard id(8 digits),
  "pin" 6 digits pin
}
```
Example response:
```
$ 40.12
```
#### 2. View transaction history
__POST /watcard/transaction__

Request body:
```
{
  "id": watcard id(8 digits) ,
  "pin" 6 digits pin,
  "start_date": '01/01/2016',
  "end_date": '01/31/2016'
}
```
Response:
1. **date**: The date when transaction was made
2. **time**: The local time when transaction was made
3. **amount**: Transaction amount
4. **type** : Transaction type
5. **terminal**: location where transaction was made

Example response:
```
[
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  },
  {
    "date": "03/24/2016",
    "terminal": "(00426)WAT-TASK         ",
    "amount": "20.00",
    "type": "(003)PPAY ADMIN",
    "time": "17:31:19"
  }
]
```
#### 3. Add funds
__url:__ https://www.watcard.uwaterloo.ca/oneweb/addfunds.asp 
