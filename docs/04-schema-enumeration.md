# Schema enumeration with INFORMATION_SCHEMA

MySQL exposes database metadata through `INFORMATION_SCHEMA`. The practical work used a hierarchy to understand database, table, and column structure.

| View | Information |
|---|---|
| `SCHEMATA` | Database/schema names |
| `TABLES` | Tables and views |
| `COLUMNS` | Column names, types, and table association |

Example metadata queries in a local training database:

```sql
SELECT schema_name FROM information_schema.schemata;
SELECT table_name FROM information_schema.tables WHERE table_schema = 'sample_db';
SELECT column_name, data_type FROM information_schema.columns
WHERE table_schema = 'sample_db' AND table_name = 'users';
```

The supplied report records discovery of schemas, a users table, and authentication-related fields. It also records retrieving a lab password hash; the actual hash and schema-specific secrets are omitted. Metadata access is normal database behavior; the security issue is allowing untrusted input to control arbitrary queries. Parameterized statements and least privilege reduce risk.
