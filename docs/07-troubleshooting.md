# Troubleshooting and lessons

## Failure patterns
- **Quoting assumptions:** establish the actual quoting context from evidence.
- **Parenthesis mismatch:** comment markers do not repair syntax already malformed before the comment.
- **Column count or type mismatch:** UNION results require matching counts and compatible types; reconfirm for each endpoint.
- **Wrong parameter:** an input may be ignored, validated, cast, or safely bound; map requests first.
- **Missing response headers:** redirects and Location headers may communicate application state.
- **Default-path assumptions:** the source report describes Nginx with a non-standard web root; inspect configuration.

## Diagnostic checklist
- [ ] Confirm authorized lab instance.
- [ ] Capture a normal baseline request.
- [ ] Record method, path, parameters, status, headers, and body.
- [ ] Infer quote and parenthesis context from evidence.
- [ ] Change one variable per test.
- [ ] Reconfirm column count and compatible types.
- [ ] Identify rendered output positions.
- [ ] Separate observation from query hypothesis.
- [ ] Redact secrets before publication.

Progress depended on replacing assumptions with testable hypotheses and preserving response evidence.
