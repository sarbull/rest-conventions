# rest-conventions

# GET /api/elements
## Request
```json
GET /api/elements HTTP/1.1
```
## Response
```json
[
  {
    "id": 1,
    "name": "Oxygen",
    "atomicNumber": 8
  },
  {
    "id": 2,
    "name": "Carbon",
    "atomicNumber": 6
  }
]
```

# POST /api/elements
## Request
```json
{
  "name": "HELIUM",
  "atomicNumber": 2
}
```
## Response
```json
{
  "id": 3,
  "name": "HELIUM",
  "atomicNumber": 2
}
```

# GET /api/elements/:id
## Request
```json
GET /api/elements/3 HTTP/1.1
```
## Response
```json
{
  "id": 3,
  "name": "HELIUM"
  "atomicNumber": 2
}
```

# PATCH /api/elements/:id
## Request
```json
{
  "atomicNumber": 20
}
```
## Response
```json
{
  "id": 3,
  "name": "Helium"
  "atomicNumber": 20
}
```

# PUT /api/elements/:id
## Request
```json
{
  "name": "Helium"
  "atomicNumber": 2
}
```
## Response
```json
{
  "id": 3,
  "name": "Helium"
  "atomicNumber": 2
}
```

# DELETE /api/elements/:id
## Request
```json
DELETE /api/elements/3 HTTP/1.1
```
## Response
```json
HTTP/1.1 204 NO CONTENT
```

# POST /api/elements/:id/actions
## Request
```json
{
  "type": "RAISE_CONCENTRATION",
  "payload": {
    "percentage": 20
  }
}
```
## Response
```
HTTP/1.1 200 OK
```
