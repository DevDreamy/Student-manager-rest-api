# Student Manager Rest API
This REST API was built during **Basic to Advanced JavaScript and TypeScript Course 2021**

This API is beeing used for the [Student Manager](https://github.com/DevDreamy/Student-manager)

## Endpoints
| Method |                Desc               |    Endpoint    | Login Required? | 
| ------ | --------------------------------- | -------------- | --------------- |
|GET     |Show all registered students       |/students       | No              |
|GET     |Show one registered student        |/students/id    | No              |
|POST    |Register a new student             |/students       | Yes             |
|POST    |Upload a photo for a student       |/photos         | Yes             |
|POST    |Register a new user                |/users          | Yes             |
|POST    |Create an unique token for an user |/tokens         | No              |
|PUT     |Update a student information       |/students/id    | Yes             |
|PUT     |Update an user account             |/users/id       | Yes             |
|DELETE  |Delete a student                   |/students/id    | Yes             |

### Creating a new student using Postman

**DATABASE_URL/students**

_JSON Body_

```javascript
{
  "name": "Student Name",
  "lastname": "Student Lastname",
  "email": "studentemail@email.com",
  "age": "28",
  "weight": "80",
  "height": "1.68"
}
```

### Creating a new user using Postman
**DATABASE_URL/users**

_JSON Body_

```javascript
{
  "name": "Username",
  "password": "userpassword",
  "email": "user@email.com"
}
```

### Upload a new photo using Postman
**DATABASE_URL/photos**

_multipart/form-data_

```javascript
photo: filename.jpg
student_id: 1
```

## Available Scripts

### npm i

Install all the required packages.

### npm run dev

Run the API in development mode

### npm run build

Build the API for production

### npm run start

Run the API in production mode
