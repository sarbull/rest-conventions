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
    "name": "Oxygen"
  },
  {
    "id": 2,
    "name": "Carbon"
  }
]
```

# GET /api/elements/:id
## Request
```json
GET /api/elements/1 HTTP/1.1
```
## Response
```json
{
  "id": 1,
  "name": "Oxygen"
}
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
