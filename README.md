# App Planning
***This application will be a personal finance manager application***

### **App**

    - accessKey
    - secretKey
    - item_types
    - users
        - email
        - password
        - usernames
        - purchases
            - Date
                - list of purchases on that date
                    - item_name
                    - item_type
                    - item_price
                    - purchase_time

## Api Planning
```
-> Signing up an user
    route: /signup
    method: POST
    request_body:
        type: form-data
        data: name
              email
              password
              username
    response_body: "User signed up successfully"
```

### -> Logging in user

```
    route: /login
    method: POST
    request_body:
        type: form-data
        data: email/username
              password
    response_body: user_idx
                   message
```
### -> Add a purchase

<!-- -> Delete a purchase -->

### -> Get all purchases for today
```
    route: /get_purchases_today
    method: GET
    request_body:
        data: user_idx
    response_body:
        list of all purchases in the following format:
            [
                {
                    "item_name": "", "item_price":"", "item_type":"", "purchase_time":""
                }
            ]
```
-> Get all purchases from start date and end date

-> Get the average amount of purchase till now

-> Get the most purchased item

# Planning APIs as admin user
