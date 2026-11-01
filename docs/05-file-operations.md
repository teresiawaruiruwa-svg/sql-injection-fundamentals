# Database file operations: LOAD_FILE and INTO OUTFILE

## LOAD_FILE()
MySQL `LOAD_FILE()` can read a server-side file when database and operating-system permissions and configuration allow it. The report describes inspecting application source and identifying a configuration include; the exercise demonstrated potential exposure of application configuration and a database credential. Secret-bearing output is omitted. Success depends on server permissions, database privileges, path validity, configuration, and whether the application returns the value.

## secure_file_priv
The practical work examined MySQL's `secure_file_priv`, which constrains certain server-side import/export operations. Interpret its value alongside database grants and operating-system permissions. An empty value is not a security control.

## INTO OUTFILE
MySQL `SELECT ... INTO OUTFILE` writes query output to a server-side file when account, server settings, and operating-system permissions allow it. The HTB report describes a controlled demonstration in which permissive file access and a web-accessible directory illustrated impact. No deployable web shell, credential, target address, or flag is included.

The escalation depended on multiple conditions: unsafe SQL construction, excessive database file privileges, database process write access, a web-accessible destination, and server-side script execution. SQL injection alone does not automatically provide operating-system command execution.

The report notes that the skills assessment used Nginx and a non-standard web root. Assuming the default web root was incorrect; inspecting configuration identified the actual path. Verify the environment rather than relying on defaults.
