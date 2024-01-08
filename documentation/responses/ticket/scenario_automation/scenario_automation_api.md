# Scenario Automation API's

- [Scenario Automation API's](#scenario-automation-apis)
  - [Get Scenario Automations](#get-scenario-automations)
  - [Execute Scenario](#execute-scenario)


## Get Scenario Automations

```
Method - GET
Path - /api/_/scenario_automations
```

| Request |                                           Response                                            |   Notes |
| ------- | :-------------------------------------------------------------------------------------------: | ------: |
| -       | [Body](../../../../response/ticket/scenario_automation/get_scenario_automations/success.json) | Success |


## Execute Scenario

```
Method - PUT
Path - /api/_/tickets/execute_scenario
body - {
    "scenario_id": 27000168500,
    "ids": [
        52
    ]
}
```

| Request |  Response  |   Notes |
| ------- | :--------: | ------: |
| -       | No Content | Success |