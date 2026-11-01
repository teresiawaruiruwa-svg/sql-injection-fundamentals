# Overview

This repository records practical SQL injection learning from HTB Academy's SQL Injection Fundamentals module. Its emphasis is understanding how applications construct SQL and how untrusted input can alter intended query syntax or logic.

## Workflow
1. Map routes, HTTP methods, parameters, and normal application behavior.
2. Establish a baseline request and response.
3. Test whether user-controlled input reaches a database query.
4. Infer quoting, parentheses, and data-type context from observable behavior.
5. Validate one hypothesis at a time.
6. In UNION contexts, determine result-column count and compatible types.
7. Identify which returned values are rendered by the application.
8. Record impact conditions and separate observations from inference.
9. Translate the learning into defensive recommendations.

## Evidence labels
- **Observed:** directly visible in captured evidence.
- **Reported:** stated in the submitted completion report.
- **Inferred:** supported interpretation, not directly proven.
- **Not verified:** source material does not establish the claim.

All activity relates to authorized training-lab work. Never publish credentials, hashes, flags, tokens, or private target information.
