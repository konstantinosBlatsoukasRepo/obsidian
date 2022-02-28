session management purpose:

session management is intended to allow the application to track a unique instance of a user within the application.


session token per request
for re-authenticating the user
is used for all authorization activities


HTTP strict transport security (TLS)


session tracking mechanisms:

- url rewritting (session id is included in the url)
- basic authentication 
(never be used in a web app, you send username and password in every request)
- cookies

the session id must changes


[[OWASP top 10]]
