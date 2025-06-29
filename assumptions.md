# Assumptions Made

- Timestamps are all handled in IST.
- Pattern 1 is only triggered after merchant's total transactions exceed 50,000.
- CustomerImportance weights are averaged per customer across transaction types.
- Fraud field is ignored as per instruction.
- Pattern outputs are written to S3 in batches of 50.
- Each detection includes only applicable fields; others are left empty.
