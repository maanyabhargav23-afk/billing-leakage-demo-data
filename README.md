# Billing Leakage Demo Data

**Demo only:** These are fictional records, not real customer or billing data.

For this example, potential leakage is calculated as expected amount minus billed amount, if expected is higher.

```json
{
  "demoOnly": true,
  "records": [
    {
      "reconciliationId": "DEMO-RA-001",
      "currency": "INR",
      "expectedAmount": 1200.00,
      "billedAmount": 1200.00,
      "items": [
        { "item": "Demo data pack", "expected": 800.00, "billed": 800.00 },
        { "item": "Demo voice usage", "expected": 400.00, "billed": 400.00 }
      ],
      "expectedDemoResult": {
        "result": "NO_GAP_FOUND",
        "potentialLeakage": 0.00
      }
    },
    {
      "reconciliationId": "DEMO-RA-002",
      "currency": "INR",
      "expectedAmount": 1500.00,
      "billedAmount": 1250.00,
      "items": [
        { "item": "Demo data pack", "expected": 1000.00, "billed": 1000.00 },
        { "item": "Demo roaming usage", "expected": 500.00, "billed": 250.00 }
      ],
      "expectedDemoResult": {
        "result": "POTENTIAL_LEAKAGE",
        "potentialLeakage": 250.00
      }
    }
  ]
}
```
