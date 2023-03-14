Swagger UI: https://api.csgames2023.sandbox.croesusfin.cloud/swagger/index.html

There is one route for the API, /CroesusValidation. Two methods are supported:

# GET /CroesusValidation
The GET method will return the result of the last submissionthat was made by your team.

## URL Parameters
- TeamName: Your team name (you should have received this by email before the challenge starts)
- TeamPassword: Your team password (you should have received this by email before the challenge starts)

## Response
The response will be a JSON document containing the list of transactions submitted, as well as the final total value
of you investment.

# POST /CroesusValidation
The POST method allows you to submit à list of transactions for validation

## URL Parameters
- TeamName: Your team name (you should have received this by email before the challenge starts)
- TeamPassword: Your team password (you should have received this by email before the challenge starts)
- FinalValidationMode: The password to enable the final validation mode (see [FINAL_SIM.md](./FINAL_SIM.md))

## Request body
A JSON document containing the list of transactions that you want to submit. Here is an example:

    [
        {
            "date": "2023-01-03",
            "action": "BUY",
            "ticker": "F"
        },
        {
            "date": "2023-01-09",
            "action": "SELL",
            "ticker": "F"
        },
        {
            "date": "2023-01-10",
            "action": "BUY",
            "ticker": "GM"
        },
        {
            "date": "2023-01-12",
            "action": "SELL",
            "ticker": "GM"
        },
    ]

## Response
The response will be a JSON document containing the result message and the final total value
of you investment. Here are some examples:

## Successful response example
    {
      "Message": "success",
      "TotalValue": 1234567.89
    }
    
## Error response example

    {
      "Message": "Error: wrong trade action (use BUY or SELL) -> ACH",
      "TotalValue": null
    }
