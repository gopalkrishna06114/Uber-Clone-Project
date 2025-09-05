# User Registration Endpoint Documentation

## Endpoint

`POST /users/register`

## Description

Registers a new user in the system. Validates the input data, checks for existing users, hashes the password, creates the user, and returns an authentication token.

---

## Request Body

Send a JSON object with the following structure:

```json
{
  "fullname": {
    "firstname": "John",
    "lastname": "Doe"
  },
  "email": "john.doe@example.com",
  "password": "yourpassword"
}
```

### Field Requirements

- `fullname.firstname`: **string**, required, minimum 3 characters
- `fullname.lastname`: **string**, optional, minimum 3 characters if provided
- `email`: **string**, required, must be a valid email address, minimum 5 characters
- `password`: **string**, required, minimum 6 characters

---

## Responses

### Success

- **Status Code:** `201 Created`
- **Body:**
  ```json
  {
    "token": "<JWT_TOKEN>",
    "user": {
      "_id": "...",
      "fullname": {
        "firstname": "...",
        "lastname": "..."
      },
      "email": "...",
      // other user fields
    }
  }
  ```

### Validation Error

- **Status Code:** `400 Bad Request`
- **Body:**
  ```json
  {
    "errors": [
      {
        "msg": "Error message",
        "param": "field",
        "location": "body"
      }
    ]
  }
  ```

### User Already Exists

- **Status Code:** `400 Bad Request`
- **Body:**
  ```json
  {
    "message": "User already exist"
  }
  ```

---

## Example Request

```bash
curl -X POST http://localhost:3000/users/register \
  -H "Content-Type: application/json" \
  -d '{
    "fullname": { "firstname": "Jane", "lastname": "Smith" },
    "email": "jane.smith@example.com",
    "password": "securepassword"
  }'
```

---

## Notes

- All fields are required except `fullname.lastname`.
- Passwords are securely hashed before storing.
- On success, a JWT token is returned