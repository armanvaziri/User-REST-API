# REST API for user data

## Usage 

All responses will have the form 

```json
{
	"data": {
		"name": "name of the user",
		"age": "age of the user",
		"occupation": "occupation of the user"
	},
	"message": "Description of what happened"
}
```

Subsequent response definitions will only detail the expected value of the 'data field'

### List all users 

***Definition***

'GET /users'

**Response**

- '200 OK' on success

```json
[
	{
        "name": "Arman",
        "age": 20,
        "occupation": "Student"
    },
    {
        "name": "Matt",
        "age": 30,
        "occupation": "Teacher"
    }
]
```

### Adding a new user 

**Definition**

'POST /user/name'

**ARGUMENTS**

- `"name":string` a globally unique identifier for the user's name
- `"age":int` the user's age
- `"occupation":string` the user's current occupation 

**RESPONSE**

- `201 Created`	on success

```json
{
    "name": "Arman",
    "age": 20,
    "occupation": "Student"
}
```

## Lookup user details 

'GET /user/<name>'

**Response**

- '404 Not Found' if the user does not exist
- '200 OK' on success

```json
{
    "name": "Arman",
    "age": 20,
    "occupation": "Student"
}
```





## Instructions for use with Postman applications

### navigate to directory where data.py is located
### run "python app.py"
### open postman
### enter given http
