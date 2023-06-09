### Zomato merchant API (unofficial) | 2022 - 2023


> NOTE: I can't guarantee you will not be blocked by using this method, although it has worked for me, [More details](https://shajin-sha.github.io/zomato-api/).



#### Features included -: 


- ✅ Multiple login
- ✅ Orders list
- ✅ Orders list filtering (By status)
- ✅ Accept  new order 
- ✅ Mark order ready
- ✅ Go online &  Offline - status
- ✅ Item list (Menu)
- ✅ Item list editing (Menu editing)
- ✅ This is't web sracping, So you will get native speed of Zomato.



#### Disclaimer

This project is not affiliated, associated, authorized, endorsed by, or in any way officially connected with Zomato or any of its subsidiaries or its affiliates. The official Zomato website can be found at https://zomato.com. "Zomato", "Zomato API", "Zomato *" as well as related names, marks, emblems and images are registered trademarks of their respective owners.


### Login
``` 
POST http://localhost:port/login
```
#### request body
```
{
    "phone":"123456789",
    "system_id":"demo_system"
}

```


### OTP
```
POST http://localhost:10000/OTP
```
call this after resived OTP, (call Login API request runnning), only after callig this /login will sent request.

#### request body
```
{
    "otp":"323232",
    "system_id":"demo_system"
}
```





