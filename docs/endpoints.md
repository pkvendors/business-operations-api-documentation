
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

