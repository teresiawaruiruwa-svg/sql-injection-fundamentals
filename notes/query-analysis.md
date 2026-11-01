# Query analysis worksheet

| Field | Record |
|---|---|
| Lab section | |
| Application route | |
| HTTP method | |
| Parameter | |
| Baseline input/response | |
| Test input (sanitized) | |
| Observed response/error | |
| Likely quoting context | |
| Parentheses present? | |
| Query hypothesis | |
| Supporting evidence | |
| Alternative explanations | |
| Follow-up validation | |
| Screenshot reference | |

**Observation:** a malformed input produced a database syntax error. **Hypothesis:** the application may concatenate the value into SQL. **Not established:** exact source query, privileges, or whether other parameters are injectable.
