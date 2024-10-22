# Personal Expense Tracker API

## Setup and Run Instructions

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `node server.js` to start the server on port 3000.

## API Documentation

### POST /transactions
- **Request Body**: 
```json
{
    "type": "income/expense",
    "category": "string",
    "amount": number,
    "date": "YYYY-MM-DD",
    "description": "string"
},

# Response:
```json
{
    "id": 1
}

# GET /transactions
## Response: Array of transactions.

# GET /transactions/
## Response: Single transaction object.

# PUT /transactions/
## Request Body: Same as POST.

# Response:
```json
{
    "message": "Transaction updated"
}

# DELETE /transactions/
## Response:

```json
{
    "message": "Transaction deleted"
}

# GET /summary
## Response:

```json
[
    {
        "type": "income",
        "total": 1000
    },
    {
        "type": "expense",
        "total": 500
    }
]