
## Validation Error: Missing Email Address

**HTTP Status Code:** 400 Bad Request

**Error Code:** VALIDATION_ERROR

**Description:**

The API returns this error when a required email
address is missing from the request body.

**Example Error Response:**

```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "The email address is required.",
    "status": 400
  }
}
```

**Cause:**

The email field was omitted from the API request.

**Resolution:**

Include a valid email address in the request body.

**Corrected Request Example:**

```json
{
  "firstName": "Sandra",
  "lastName": "Johnson",
  "email": "Sandra.Johnson@SquareAngles.com",
  "department": "Finance"
}
```

**Expected Result:**

The API should process the request successfully
if all other validation requirements are satisfied.

