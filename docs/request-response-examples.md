Request

POST /v1/employees HTTP/1.1
Host: api.boms-demo.com
Authorization: Bearer YOUR_ACCESS_TOKEN
Content-Type: application/json

JSON request body

{
  "firstName": "Lisa",
  "lastName": "Williams",
  "email": "lisa@example.com",
  "department": "Finance"
}

JSON response

{
  "employeeId": 104,
  "firstName": "Lisa",
  "lastName": "Williams",
  "email": "lisa@example.com",
  "department": "Finance",
  "status": "Active"
}
