### WatCard Service
#### 1. Check balance
__POST /watcard/balance__

Request body:
```
{
  "id": watcard id(8 digits student ID),
  "pin" 6 digits pin
}
```
Example response:
```
{
  "balance": 40.12
}
```
#### 2. View transaction history
__POST /watcard/transaction__ Returns the transaction history within specified begin date and end date.

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
1. **date**: The date when transaction was made.
2. **time**: The local time when transaction was made.
3. **amount**: Transaction amount.
4. **type** : Transaction type.
5. **terminal**: Location where transaction was made.

Example response:
```
[
  {
    "date": "04/08/2016",
    "terminal": "(00641)WAT-FS-THDC-EXPRE",
    "amount": "-4.83",
    "type": "(104)VEND FINCL",
    "time": "09:57:57"
  },
  {
    "date": "04/07/2016",
    "terminal": "(00112)VM_DC_DASANI",
    "amount": "-2.25",
    "type": "(004)VEND MONEY",
    "time": "21:19:01"
  },
  {
    "date": "04/07/2016",
    "terminal": "(00814)STARBUCKS STC1",
    "amount": "-3.94",
    "type": "(104)VEND FINCL",
    "time": "14:37:20"
  },
  {
    "date": "04/06/2016",
    "terminal": "(00636)VM_MC_DASANI",
    "amount": "-2.25",
    "type": "(004)VEND MONEY",
    "time": "20:35:54"
  }
]
```
#### 3. Add funds
__url:__ https://www.watcard.uwaterloo.ca/oneweb/addfunds.asp


#### 4. Reset pin
First Make a post call to __/watcard/requestReset__
with request body:
```
{
  "userid": quest login id,
  "password": quest password
}
```
Example response:
```
{
  'Cookie': cookie for PIN reset,
  'ID': WATIAM ID
}
```
Then

__POST /watcard/reset__
Request header:
```
{
  "Cookie": cookie from requestReset
}
```

Request Body:
```
{
  "newPin": new PIN (6 digits)
}
```
