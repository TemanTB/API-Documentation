# TemanTB-API

<h2>
 Endpoint
</h2>
 <a href="https://apitemantb-5vmozaariq-ts.a.run.app">https://apitemantb-5vmozaariq-ts.a.run.app</a>

 <br>
 <br>

<h2>Register</h2>

- **Register User**
- **URL**: `/users`
- **Method**: `POST`
- **Request Type Data Body** : <br>
        1. name : `STRING` <br>
        2. email : `STRING` <br>
        3. phone : `STRING` <br>
        4. password : `STRING` <br>
        5. confPassword : `STRING` <br>
- **Request Dummy Data Body** : <br>
```json
{
        "name": "input name",
        "email": "input email",
        "phone": "input phone",
        "password": "input paswword",
        "ConfPassword": "input same paswword"
}
```
- **Response** : <br>
```json
{
    "data": {
        "userId": "60213eb1-e637-4102-bcae-f3f50a871725",
        "name": "user",
        "email": "user@gmail.com",
        "phone": "08123123123",
        "password": "paswword",
        "updatedAt": "autodate",
        "createdAt": "autodate"
    },
    "message": "success register data"
}
```

<br>
<br>

<h2>GET All User</h2>

- **Login User**
- **URL**: `/users`
- **Method**: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** :
```json
{
    "loginResult": {
        "userId": "result of user id",
        "email": "result of email"
        "token": <token>
    }
}
```

<br>
<br>

<h2>Login</h2>

- **Login User**
- **URL**: `/login`
- **Method**: `POST`
- **Request Type Data Body**: <br>
        1. email : `STRING` <br>
        2. password : `STRING` <br>
- **Request Dummy Data Body** : <br>
```json
{
        "name": "input name",
        "password": "input paswword",
}
```
- **Response** : <br>
```json
{
    "loginResult": {
        "userId": "result of user id",
        "email": "result of email"
        "token": <token>
    }
}
```

<br>
<br>

<h2>Logout</h2>

- **Logout User**
- URL: `/logout`
- Method: `DELETE`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- Response : <br>
```json
{
    OK
}
```

<br>
<br>

<h2>GET All Schedule</h2>

- **GET Schedule All User id & Schedule id**
- URL: `/schedule`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- Response : <br>
```json
{
    "data": [
        {
            "scheduleId": "schedule user Id 1",
            "medicineName": "medicine name user 1",
            "description": "description user 1",
            "hour": "time user 1",
            "userId": "user id 1",
            "user": {
                "name": "name 1",
                "email": "email 1",
                "phone": "phone 1"
            }
        },
         {
            "scheduleId": "schedule user Id 2",
            "medicineName": "medicine name user 2",
            "description": "description user 2",
            "hour": "time user 2",
            "userId": "user id 2",
            "user": {
                "name": "name 2",
                "email": "email 2",
                "phone": "phone 2"
            }
        }
}
```

<br>
<br>

<h2>POST Data Schedule</h2>

- **POST Data Schedule**
- URL: `/schedule`
- Method: `POST`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Request Body** : <br>
        1. medicineName : `STRING` <br>
        2. description : `STRING` <br>
        3. hour : `STRING` <br>
- **Request Dummy Data Body** : <br>
```json
{
        "medicineName": "input medicine name",
        "description": "input description",
        "hour": "input hour"
}
```
- **Response** : <br>
```json
{
    "data": {
        "scheduleId": "schedule id user they success created",
        "medicineName": "medicine name user they success create",
        "description": "description user they success create",
        "hour": "hours user they success create",
        "userId": "user id they success create",
        "updatedAt": "date & time",
        "createdAt": "date & time"
    },
    "message": "Success, schedule added"
}
```

<br>
<br>

<h2>GET Data Schedule By User ID</h2>

- **GET Data Schedule By User ID**
- URL: `/schedule/:userId`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- Response : <br>
```json
{
    "data": {
        "scheduleId": "schedule id user they success created",
        "medicineName": "medicine name user they success create",
        "description": "description user they success create",
        "hour": "hours user they success create",
        "userId": "user id they success create",
        "updatedAt": "date & time",
        "createdAt": "date & time"
    },
    "Successfully retrieved schedule data"
}
```

<br>
<br>

<h2>GET Data Schedule By Schedule ID</h2>

- **GET Data Schedule By Schedule ID**
- URL: `/getschedule/:scheduleId`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- Response : <br>
```json
{
    "data": [
        {
            "scheduleId": "schedule id user they success created",
            "medicineName": "medicine name user they success create",
            "description": "description user they success create",
            "hour": "hours user they success create",
            "userId": "user id they success create",
            "updatedAt": "date & time",
            "createdAt": "date & time"
            "userUserId": null
        }
    ],
    "message": "success get schedule"
}
```

<br>
<br>

<h2>DELETE Data Schedule By Schedule ID</h2>

- **DELETE Data Schedule By Schedule ID**
- URL: `/schedule/:scheduleId`
- Method: `DELETE`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- Response : <br>
```json
{
   OK
}
```

<br>
<br>

<h2>EDIT Data Schedule By Schedule ID</h2>

- **EDIT Data Schedule By Schedule ID**
- URL: `/schedule/:scheduleId`
- Method: `PUT`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Request Body** : <br>
        1. medicineName : `STRING` <br>
        2. description : `STRING` <br>
        3. hour : `STRING` <br>
- **Request Dummy Data Body** : <br>
```json
{
        "medicineName": "edit medicine name",
        "description": "edit description",
        "hour": "edit hour"
}
```
- **Response** : <br>
```json
{
    "data": {
        "scheduleId": "schedule 1",
        "medicineName": "edit titile 1",
        "description": "description edit 1",
        "hour": "12:00:00",
        "userId": "user id 1",
        "createdAt": "date & time",
        "updatedAt": "date & time",
        "userUserId": null
    },
    "message": "update data success"
}
```

<br>
<br>

<h2>GET All Health users By users Id & Health Id</h2>

- **GET All Data Health**
- URL: `/health`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** : <br>
```json
{
    "data": [
        {
            "healthId": "healthId user 1",
            "weeks": 3,
            "date": "2023-12-19T00:00:00.000Z",
            "nextDate": "2024-01-02T00:00:00.000Z",
            "point": 4,
            "alert": "Please put your health back on 2024-01-02",
            "description": "saya sehat",
            "average": "Membaik",
            "images": "https://storage.googleapis.com/temantb-api.appspot.com/up.png",
            "time": "2023-12-19T22:37:28.000Z",
            "userId": "user id 1",
            "userUserId": null
        },{
            "healthId": "healthId user 2",
            "weeks": 3,
            "date": "2023-12-19T00:00:00.000Z",
            "nextDate": "2024-01-02T00:00:00.000Z",
            "point": 4,
            "alert": "Please put your health back on 2024-01-02",
            "description": "saya sehat",
            "average": "Membaik",
            "images": "https://storage.googleapis.com/temantb-api.appspot.com/up.png",
            "time": "2023-12-19T22:37:28.000Z",
            "userId": "user id 2",
            "userUserId": null
        }
}
```

<br>
<br>

<h2>GET Data Health users By users Id</h2>

- **GET All Data Health**
- URL: `/health/:userId`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** : <br>
```json
{
    "data": [
        {
            "healthId": "healthId user 1",
            "weeks": 3,
            "date": "2023-12-19T00:00:00.000Z",
            "nextDate": "2024-01-02T00:00:00.000Z",
            "point": 4,
            "alert": "Please put your health back on 2024-01-02",
            "description": "saya sehat",
            "average": "Membaik",
            "images": "https://storage.googleapis.com/temantb-api.appspot.com/up.png",
            "time": "2023-12-19T22:37:28.000Z",
            "userId": "user id 1",
            "userUserId": null
        },{
            "healthId": "healthId user 2",
            "weeks": 3,
            "date": "2023-12-19T00:00:00.000Z",
            "nextDate": "2024-01-02T00:00:00.000Z",
            "point": 4,
            "alert": "Please put your health back on 2024-01-02",
            "description": "saya sehat",
            "average": "Membaik",
            "images": "https://storage.googleapis.com/temantb-api.appspot.com/up.png",
            "time": "2023-12-19T22:37:28.000Z",
            "userId": "user id 1",
            "userUserId": null
        }
}
```

<br>
<br>

<h2>GET Data Health users By Health Id</h2>

- **GET Data Detail Health**
- URL: `/healthid/:healthId`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** : <br>
```json
{
    "data": [
        {
            "healthId": "healthId user 1",
            "weeks": 3,
            "date": "2023-12-19T00:00:00.000Z",
            "nextDate": "2024-01-02T00:00:00.000Z",
            "point": 4,
            "alert": "Please put your health back on 2024-01-02",
            "description": "saya sehat",
            "average": "Membaik",
            "images": "https://storage.googleapis.com/temantb-api.appspot.com/up.png",
            "time": "2023-12-19T22:37:28.000Z",
            "userId": "user id 1",
            "userUserId": null
        }
}
```

<br>
<br>

<h2>DELETE Data Health users By Health Id</h2>

- **DELETE Data Health**
- URL: `/health/:healthId`
- Method: `DELETE`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** : <br>
```json
{
    OK
}
```

<br>
<br>

<h2>GET Point Health users By users Id</h2>

- **GET Point User Data Health By User Id**
- URL: `/point/:userId`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** : <br>
```json
{
    "data": [
        {
            "date": "2023-12-19",
            "point": 5
        },
        {
            "date": "2023-12-19",
            "point": 6
        },
}
```

<br>
<br>

<h2>GET Alert Health users By users Id</h2>

- **GET Alert User Data Health By User Id**
- URL: `/alert/:userId`
- Method: `GET`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Response** : <br>
```json
{
    "data": {
        "alert": "Please put your health back on 2024-01-02"
    },
    "message": "success get meesage next date"
}
```

<br>
<br>

<h2>POST Data Health</h2>

- **POST Data Health**
- URL: `https://apiml-5vmozaariq-ts.a.run.app/health`
- Method: `POST`
- **Headers**: <br>
          1. `Authorization`: Bearer `<token>`
- **Request Body** : <br>
        1. description : `STRING` <br>
- **Request Dummy Data Body** : <br>
```json
{
        "description": "input user health",
}
```
- **Response** : <br>
```json
{
    "data": {
        "current_point": 3,
        "description": "saya sehat",
        "ml_predict": 0
    },
    "message": "Data inserted successfully",
    "status": {
        "code": 201,
        "message": "success post data"
    }
}
```

<br>
<br>






