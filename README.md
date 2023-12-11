
# Express Authentication Boilerplate

Welcome to the Express Authentication Boilerplate! This boilerplate provides a foundation for implementing user authentication using Express.js, encryption for passwords, JSON Web Tokens (JWT), and Nodemailer for email functionality.

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`SERVER_PORT`
`NODEMAILER_EMAIL`
`NODEMAILER_PASSWORD`
`MONGO_URI`


## Features

### Signup: 
Implements user registration with encrypted password storage.

### Login: 
Matches the entered password with the stored hash and issues a JWT upon successful login.

### Nodemailer: 
Uses Nodemailer to send emails, facilitating functionalities such as account verification and password reset.

## Further Assistance
For more details and explanations, refer to the tutorial videos on [YouTube]( www.youtube.com/@usamausman-dev). If you have any questions or encounter issues, feel free to reach out by commenting on the videos or contacting the developer.

## Notes
Ensure that you have a MongoDB instance set up and replace the `MONGO_URI` in the `.env` file with the correct connection string.

For security reasons, keep your `.env` file confidential and do not share it publicly.


## API Reference


#### Signup User

```http
  POST /api/signup
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `username` | `string` | **Required**. Your Username |
| `gender` | `string` | **Required**. Your Gender|
| `email` | `string` | **Required**. Your Email |
| `password` | `string` | **Required**. Your Password|

#### Login User

```http
  POST /api/login
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Your Email |
| `password` | `string` | **Required**. Your Password|


#### NewsLetter Subscription

```http
  POST /api/newsletter
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Your Email |




#### Get All User

```http
  GET /api/all-users
```

returns All Users



#### Get User By ID

```http
  GET /api/user-by-id/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of user to fetch |





#### Get User By Email

```http
  GET /api/user-by-email
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `email`      | `string` | **Required**. Email of item to fetch |

#### Update User Profile

```http
  PUT /api/update-profile
```


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Your Email |
| `username` | `string` | Your Updated Username |
| `profile_pic` | `string` |Your Updated Profile Picture |
| `gender` | `string` | Your Updated Gender |

#### DELETE USER

```http
  DELETE /api/delete-user
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Your Email |



