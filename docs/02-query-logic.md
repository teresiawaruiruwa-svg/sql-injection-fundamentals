# Query logic: authentication, comments, and parentheses

## String boundaries
Applications may concatenate user-controlled values into quoted SQL strings. If the value is not bound as data, quote characters can affect SQL parsing. A syntax error is useful evidence but does not reveal the complete query by itself.

## Boolean logic
The practical material demonstrates how an always-true boolean expression can alter an authentication predicate when input is incorporated unsafely. The submitted report describes a successful authentication-context lab exercise. Public documentation omits flags and credential material.

## SQL comments
MySQL comment forms discussed include `-- ` (double dash followed by whitespace/control character) and `#`. A comment can cause trailing query text to be ignored, but it does not fix malformed syntax before the comment begins.

## Parenthesized contexts
The practical notes identify a backend expression that wrapped user input or a condition in parentheses. A query hypothesis that ignores this grouping can fail even when the general boolean logic is sound. Inspect responses, infer syntax context, adjust one structural assumption, and validate again in the lab. Do not generalize one successful test to all login forms.
