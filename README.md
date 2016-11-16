# Google Calendar API Using Spring Boot and Spring OAuth2 Client

## Credentials
credentials are entered in the src/main/resources application*.properties files
application-dev.properties is not checked in and must be generated for local
development, see below

```
server.port=3500
spring.devtools.restart.enabled=true
spring.devtools.livereload.enabled=true

 
google.client.client-id=zzzzzzzzzz
google.client.client-secret=zzzzzzz
google.client.access-token-uri=https://www.googleapis.com/oauth2/v3/token
google.client.user-authorization-uri=https://accounts.google.com/o/oauth2/auth
google.client.client-authentication-scheme=query
google.client.scope=profile,email,https://www.googleapis.com/auth/calendar
google.resource.user-info-uri=https://www.googleapis.com/oauth2/v2/userinfo
google.resource.prefer-token-info=false
```

In production the client-id and the client-secret will come in via system
properties provided by heroku, along with server.port=$PORT