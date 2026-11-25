
# API Endpoints

## 1. Retrieve All Employees

**Endpoint:** `/employees`

**HTTP Method:** GET

**Description:**

Retrieves a list of all employee records
stored in the BOMS application.

**Base URL:**

`https://api.boms-demo.com/v1`

**Complete Request URL:**

`https://api.boms-demo.com/v1/employees`

**Authentication:** Required

**Request Parameters:**

| Parameter | Type | Required | Description |
|---|---|---|---|
| department | String | No | Filters employees by department |
| status | String | No | Filters by employment status |

**Example Request:**

```http
GET /v1/employees HTTP/1.1
Host: api.boms-demo.com
Authorization: Bearer YOUR_ACCESS_TOKEN
Content-Type: application/json
```

**Example Response: 200 OK**

```json
{
  "employees": [
    {
      "employeeId": 101,
      "firstName": "John",
      "lastName": "Smith",
      "department": "Finance",
      "status": "Active"
    }
  ]
}
```

**Response Field Definitions:**

| Field | Type | Description |
|---|---|---|
| employeeId | Integer | Unique employee identifier |
| firstName | String | Employee's first name |
| lastName | String | Employee's last name |
| department | String | Employee's department |
| status | String | Employment status |



---

## 2. Create a New Employee

**Endpoint:** `/employees`

**HTTP Method:** POST

**Description:**

Creates a new employee record in the BOMS application.

**Authentication:** Required

**Request Body:**

| Field | Type | Required | Description |
|---|---|---|---|
| firstName | String | Yes | Employee's first name |
| lastName | String | Yes | Employee's last name |
| email | String | Yes | Employee's email address |
| department | String | Yes | Assigned department |

**Example Request:**

```http
POST /v1/employees HTTP/1.1
Host: api.boms-demo.com
Authorization: Bearer YOUR_ACCESS_TOKEN
Content-Type: application/json
```

**JSON Request Body:**

```json
{
  "firstName": "Robert",
  "lastName": "Brown",
  "email": "robert@example.com",
  "department": "Information Technology"
}
```

**Example Response: 201 Created**

```json
{
  "employeeId": 103,
  "firstName": "Robert",
  "lastName": "Brown",
  "email": "robert@example.com",
  "department": "Information Technology",
  "status": "Active"
}
```


---

## 3. Retrieve an Individual Employee

**Endpoint:** `/employees/{employeeId}`

**HTTP Method:** GET

**Description:**

Retrieves an individual employee record using
the employee's unique identification number.

**Authentication:** Required

**Path Parameters:**

| Parameter | Type | Required | Description |
|---|---|---|---|
| employeeId | Integer | Yes | Unique employee identifier |

**Example Request:**

```http
GET /v1/employees/103 HTTP/1.1
Host: api.boms-demo.com
Authorization: Bearer YOUR_ACCESS_TOKEN
```

**Example Response: 200 OK**

```json
{
  "employeeId": 103,
  "firstName": "Robert",
  "lastName": "Brown",
  "email": "robert@example.com",
  "department": "Information Technology",
  "status": "Active"
}
```


---

## 4. Update an Employee

**Endpoint:** `/employees/{employeeId}`

**HTTP Method:** PUT

**Description:**

Replaces an existing employee record using
the employee's unique identification number.

**Authentication:** Required

**Path Parameters:**

| Parameter | Type | Required | Description |
|---|---|---|---|
| employeeId | Integer | Yes | Employee record to update |

**Example Request:**

```http
PUT /v1/employees/103 HTTP/1.1
Host: api.boms-demo.com
Authorization: Bearer YOUR_ACCESS_TOKEN
Content-Type: application/json
```

**JSON Request Body:**

```json
{
  "firstName": "Robert",
  "lastName": "Brown",
  "email": "robert@example.com",
  "department": "Operations"
}
```

**Example Response: 200 OK**

```json
{
  "employeeId": 103,
  "firstName": "Robert",
  "lastName": "Brown",
  "email": "robert@example.com",
  "department": "Operations",
  "status": "Active"
}
```
