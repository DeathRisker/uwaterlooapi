### Login
1. __POST /getLearnCookie__
2. __POST /getPortalCookie__

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
