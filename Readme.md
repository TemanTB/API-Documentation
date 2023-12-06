# TemanTB-API

## URL
url structure:
```json
https://temantb-api.et.r.appspot.com/
```

## Users

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| POST   | /users        | 201 | JSON | Create new users |
| GET    | /users        | 200 | JSON | List data of users    |

POST data users body:

 - `userID`: STRING / UUID
 - `name`: STRING
 - `email`: STRING
 - `phone`: STRING
 - `password`: STRING
 - `refresh_token`: TEXT
   
POST data users structure:

```json
{
    "name": "user1",
    "email": "user@gmail.com",
    "phone": 123123
    "password": "123123",
    "confPassword": "123123"
}
```

GET data users structure:

```json
{
    "data": [
        {
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
            "name": "user",
            "email": "user@gmail.com"
        }
    ],
    "message": "success get all data"
}
```

## Login

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| POST   | /login        | 201 | JSON | access login|

POST data login structure:

```json
{
    "email": "user@gmail.com",
    "password": "123123"
}
```

## Logout

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| DELETE   | /logout     | 200 | JSON | delete token login|

DELETE data logout structure:

```json
{
   OK
}
```

## Schedule

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| POST   | /schedule        | 201 | JSON | Create new users |
| GET    | /schedule        | 200 | JSON | List data of users    |
| GET    | /schedule/userID        | 200 | JSON | List data of users    |
| DELETE    | /schedule/delete/scheduleID        | 200 | JSON | List data of users    |
| PUT    | /schedule/edit/scheduleID        | 200 | JSON | List data of users    |

POST data schedule body:

 - `scheduleID`: STRING / UUID
 - `title`: STRING
 - `description`: TEXT
 - `hour`: TIME
 - `userID`: STRING / UUID

POST data schedule structure:

```json
{
    "title": "lagi",
    "description": "ini adalah lagi",
    "hour": "12:31:30"
}
```

GET all data schedule structure:

```json
{
    "data": [
        {
            "scheduleID": "0017ac03-43dd-46d8-b8a2-b3b2c17ddd20",
            "title": "example title 1",
            "description": "example title 1",
            "hour": "12:31:30",
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
            "user": {
                "name": "user1",
                "email": "user@gmail.com",
                "phone": "081231312"
            }
        },
         {
            "scheduleID": "0017ac03-43dd-46d8-b8a2-b3b2c17ddd20",
            "title": "example title 2",
            "description": "example title 2",
            "hour": "12:31:30",
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
            "user": {
                "name": "user2",
                "email": "user@gmai2.com",
                "phone": "081231312"
            }
        },
    ],
    "message": "success get all schedules"
}
```

GET data schedule by user id structure:

```json
{
    "data": [
        {
            "scheduleID": "0017ac03-43dd-46d8-b8a2-b3b2c17ddd20",
            "title": "example title 1",
            "description": "example title 1",
            "hour": "12:31:30",
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee"
        },
        {
            "scheduleID": "4b9fd589-35a0-46f6-ab88-2ed35bf058e9",
            "title": "example title 2",
            "description": "example title 2",
            "hour": "12:31:30",
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee"
        },
    ],
    "message": "Successfully retrieved schedule data"
}
```

DELETE data schedule by schedule id structure:

```json
{
    "data": {
        "scheduleID": "4b9fd589-35a0-46f6-ab88-2ed35bf058e9",
        "title": "lagi",
        "description": "ini adalah lagi",
        "hour": "12:31:30",
        "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
        "createdAt": "2023-12-05T10:37:54.000Z",
    },
    "message": "delete data success"
}
```

PUT data schedule by schedule id structure:

```json
{
    "title": "edit titile 1",
    "description": "description edit 1",
    "hour": "12:00:00"
}
```

## CC

Host : 
```json
34.128.114.61
```
Password : 
```json
budakkorporat12
```

Connect SQL Instance:
```json
IP public (0.0.0.0/0)
sudo apt-get update
sudo apt-get install mysql-client
mysql -h ip_public_sql -u root -p 
create databse namadatabasenya
```

Server options:
 - `Databases`: dbtemantb
 - `port`: 8000
 - `host`: localhost
