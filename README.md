#  Ask Apiko API


## Start

Make sure that you have last version of [Node js](https://nodejs.org/en//) and [npm](https://www.npmjs.com/). Thеn run

> !!! add .env file with `PORT` `MONGODB_URI` and `SECRET_TOKEN` variables for example 
 ```
MONGODB_URI = mongodb://localhost:27017/spark-horizon-api
PORT = 3001
SECRET_TOKEN = W3 Hav3 th3 kn0w h0w

 ```
 and then:
```
npm i && npm run dev

```

### Lint

```
npm run lint
```

## API docs
### Auth

__POST__ `/api/v1/auth/sign-in` - **Sign In**
```
@params
       email {string}
       password {string}
 ```

 __POST__ `/api/v1/auth/sign-up` - **Sign Un**
```
 @params
       email {string}
       password {string}
```
 __POST__ /api/v1/auth/sign-out - **Sign Out**
```
 @header
        Authorization: Bearer {token}
```

__PUT__ `/api/v1/auth/change-password` - **Change Password**
```
 @header
       Authorization: Bearer {token}
 @params
       newPassword {string}
       password {string}
```



### User

__PUT__ `/api/v1/users/my` - **Update** User details
```
 @header
        Authorization: Bearer {token}
 @params
       email {string}
```