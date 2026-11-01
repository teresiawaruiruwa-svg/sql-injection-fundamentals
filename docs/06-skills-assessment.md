# Black-box skills assessment

The final practical assessment involved an unfamiliar lab web application. The report describes mapping the application, identifying the relevant input, analysing query context, enumerating database information, identifying the web root, and completing the lab objective. Target addresses, flags, hashes, credentials, and sensitive account values are omitted.

The notes describe reviewing login and registration routes, request methods and parameters, redirects, headers, and response behavior. Some state information was communicated through HTTP redirect headers rather than response bodies, making header inspection important.

Not every promising parameter was injectable. Some inputs appeared transformed or cast before query processing, and an initially suspected login flow was not the effective injection point. The report describes identifying a search parameter and inferring a parenthesized backend expression; earlier attempts failed because query structure was not fully accounted for.

The assessment progression included column count, visible output positions, metadata enumeration, server configuration review to identify the web root, and database file-operation impact. Distinguish direct observations from report conclusions; do not invent commands or claim execution where the source does not show it.
