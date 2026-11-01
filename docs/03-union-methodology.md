# UNION methodology

SQL `UNION` combines result sets. Both SELECT statements must return the same number of columns, and corresponding columns must have compatible types. `UNION` removes duplicate rows; `UNION ALL` retains duplicates.

The source report describes a staged approach: establish normal behavior, determine the original query's column count, create a compatible result shape, identify output positions rendered by the application, and validate with a low-impact expression. The notes refer to ORDER BY-based column discovery and test UNION values.

A database may return columns that the application does not render. A value appearing in the page confirms that the corresponding position is observable; a value not appearing does not prove that the database did not evaluate it. The report records using MySQL/MariaDB `USER()` in a printable result position. Sensitive lab output is generalized.

When troubleshooting, check whether the parameter reaches the query, whether input is quoted or parenthesized, column count, type compatibility, and rendered output. Label backend SQL structure as a hypothesis unless the source query itself is available.
