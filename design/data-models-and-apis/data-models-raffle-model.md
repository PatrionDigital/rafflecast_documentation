---
description: Describes Data Schema for a raffle
---

# Data Models - Raffle Model

## Table Schema

<table><thead><tr><th data-type="number">CID</th><th>NAME</th><th>TYPE</th><th>PKEY</th></tr></thead><tbody><tr><td>0</td><td>id</td><td>UUID</td><td>T</td></tr><tr><td>1</td><td>creator</td><td>INT</td><td>F</td></tr><tr><td>2</td><td>title</td><td>VARCHAR(255) </td><td>F</td></tr><tr><td>3</td><td>description</td><td>TEXT</td><td>F</td></tr><tr><td>4</td><td>phase</td><td>VARCHAR(50) </td><td>F</td></tr><tr><td>5</td><td>startDate</td><td>TIMESTAMP</td><td>F</td></tr><tr><td>6</td><td>createdAt</td><td>TIMESTAMP</td><td>F</td></tr><tr><td>7</td><td>updatedAt</td><td>TIMESTAMP</td><td>F</td></tr><tr><td>8</td><td>challengePeriod</td><td>TIMESTAMP</td><td>F</td></tr></tbody></table>

{% hint style="warning" %}
endDate, startTime and endTime will need to be added to the table schema
{% endhint %}

### Raffle Phase

Raffles can be in one of three phases:

* **Active:**
  * Raffle is open for participants to submit entries
  * Backend processes incoming entries and validates them.
* **Settled:**
  * Entry period has Ended. Backend selects winner(s)
  * Challenge period begins (if applicable). During this period:
    * Winners can be disputed
    * Backend may handle re-selected based on valid challenges.&#x20;
* **Finalized**
  * Raffle is confirmed as complete.
  * No further changes allowed. Backed handles prize distribution to confirmed winners.

```mermaid
// Raffle State Diagram
stateDiagram-v2
    [*] --> Active: Raffle is open for participation
    Active --> Settled: Entry period ends and winners are selected
    Settled --> Active: Re-opened due to a challenge (optional)
    Settled --> Finalized: Challenge period ends or winners are confirmed
    Finalized --> [*]: Raffle is completed
```







