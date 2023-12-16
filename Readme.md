# TemanTB-API

## URL
url structure:
```json
https://temantb-api.et.r.appspot.com/
```

## Users

POST data users body:

 - `userID`: STRING / UUID
 - `name`: STRING
 - `email`: STRING
 - `phone`: STRING
 - `password`: STRING
 - `refresh_token`: TEXT

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| POST   | /users        | 201 | JSON | Create new users |

   
POST data users structure:

```json
{
    "name": "user1",
    "email": "user@gmail.com",
    "phone": "0812312312",
    "password": "123123",
    "confPassword": "123123"
}
```

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| GET    | /users        | 200 | JSON | List data of users    |

GET data users Response:

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
</br>
</br>
</br>
</br>

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
Response Login :
```json
{
    "loginResult": {
        "userId": "84a2a107-dc18-4606-a2b5-a529a06995d8",
        "name": "chandra halim",
        "token": <token>
    }
}
```

</br>
</br>
</br>
</br>

## Logout

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| DELETE   | /logout     | 200 | JSON | delete token login|

## Authorization:
 - `Bearer`: token

DELETE data logout Response:

```json
{
   OK
}
```
</br>
</br>
</br>
</br>

## Schedule

POST data schedule body:

 - `scheduleID`: STRING / UUID
 - `medicineName`: STRING
 - `description`: STRING
 - `hour`: STRING
 - `userID`: STRING / UUID

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| POST   | /schedule        | 201 | JSON | Create new users |

## Authorization:
 - `Bearer`: token

POST data schedule structure:

```json
{
    "medicineName": "nama obat",
    "description": "keterangan",
    "hour": "12:31:30"
}
```

</br>
</br>


| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| GET    | /schedule        | 200 | JSON | List data of users    |

## Authorization:
 - `Bearer`: token

GET data schedule id structure :

```json
{
    "data": [
        {
            "scheduleID": "example user id 1",
            "title": "example title 1",
            "description": "example title 1",
            "hour": "12:31:30",
            "userID": "example user id 1",
            "user": {
                "name": "user1",
                "email": "user1@gmail.com",
                "phone": "081231312"
            }
        },
         {
            "scheduleID": "example user id 2",
            "medicineName": "example medicineName 2",
            "description": "example title 2",
            "hour": "12:31:30",
            "userID": "example user id 2",
            "user": {
                "name": "user2",
                "email": "user2@gmai2.com",
                "phone": "081231312"
            }
        },
    ],
    "message": "success get all schedules"
}
```

</br>
</br>

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| GET    | /schedule/scheduleID        | 200 | JSON | List data of users    |

## Authorization:
 - `Bearer`: token

```json
{
    "data": [
        {
            "scheduleID": "cca5263f-778c-4010-bdab-b0aaw1eb1aed",
            "medicineName": "nama obat",
            "description": "deskripsi obat",
            "hour": "12:31:30",
            "userID": "84502107-303d-4f2b-8dd6-2e78517bd8a6",
            "createdAt": "2023-12-16T18:08:01.000Z",
            "updatedAt": "2023-12-16T18:08:01.000Z",
            "userUserID": null
        }
    ],
    "message": "success get schedule"
}
}
```

</br>
</br>

GET all data schedule response :

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| GET    | /schedule/userID        | 200 | JSON | List data of users    |

## Authorization:
 - `Bearer`: token

GET data schedule by user id response:


```json
{
    "data": [
        {
            "scheduleID": "0017ac03-43dd-46d8-b8a2-b3b2c17ddd20",
            "medicineName": "example medicineName 1",
            "description": "example description 1",
            "hour": "12:31:30",
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
            "user": {
                "name": "user",
                "email": "user@gmail.com",
                "phone": "081231312"
            }
        },
         {
            "scheduleID": "0017ac03-43dd-46d8-b8a2-b3b2c17ddd20",
            "title": "example medicineName 2",
            "description": "example description 2",
            "hour": "12:31:30",
            "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
            "user": {
                "name": "user",
                "email": "user@gmail.com",
                "phone": "081231312"
            }
        },
    ],
    "message": "success get all schedules"
}
```

</br>
</br>


| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| PUT    | /schedule/edit/scheduleID        | 201 | JSON | List data of users    |

## Authorization:
 - `Bearer`: token


PUT data schedule by schedule id structure:

```json
{
    "medicineName": "edit medicineName 1",
    "description": "description edit 1",
    "hour": "12:00:00"
}
```

</br>
</br>

| Method | Path          | Response Code | Body | Description         |
| ------ |---------------| ------------- | ---- |---------------------|
| DELETE    | /schedule/delete/scheduleID        | 200 | JSON | List data of users    |

## Authorization:
 - `Bearer`: token

DELETE data schedule by schedule id structure:

```json
{
    "data": {
        "scheduleID": "4b9fd589-35a0-46f6-ab88-2ed35bf058e9",
        "medicineName": "lagi",
        "description": "ini adalah lagi",
        "hour": "12:31:30",
        "userID": "19ccdba0-8654-4f34-b4d3-40f1eea3eeee",
        "createdAt": "2023-12-05T10:37:54.000Z",
    },
    "message": "delete data success"
}
```

</br>
</br>
</br>
</br>

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
create database namadatabasenya
```

Server options:
 - `Databases`: dbtemantb
 - `port`: 8000
 - `host`: localhost
