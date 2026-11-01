# Secure coding and database remediation

## Parameterized queries
Use prepared statements so SQL syntax and user values are transmitted separately. Do not build SQL by concatenating untrusted input.

```php
$stmt = $pdo->prepare('SELECT id, username FROM users WHERE username = :username');
$stmt->execute(['username' => $username]);
$user = $stmt->fetch();
```

## Input validation
Validate values against expected business meaning and type. Validation is additional protection, not a replacement for parameterized queries.

## Least privilege
- Do not use database root accounts for application traffic.
- Grant only permissions required by the application.
- Restrict file-related privileges and review grants regularly.
- Separate read/write roles where appropriate.

Configure `secure_file_priv` deliberately. Restrict database process filesystem permissions and prevent writes to web-executable directories. Do not expose raw SQL errors, paths, credentials, or stack traces. Monitor repeated syntax errors, unusual metadata queries, unexpected file operations, and suspicious file creation.

Parameterized queries address the injection root cause; least privilege and filesystem restrictions reduce risk if another weakness is present.
