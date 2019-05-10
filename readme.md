# QUARKUS JWT examples

## building

```
mvn compile quarkus:dev
```
[read the Quarkus JWT guide](https://quarkus.io/guides/jwt-guide)

## generating a JWT token
```
mvn exec:java -Dexec.mainClass=org.acme.jwt.GenerateToken -Dexec.classpathScope=test
```

## do a baerer token CURL
```
curl -H "Authorization: Bearer eyJraWQiOiJcL3ByaXZhdGVLZXkucGVtIiwidHlwIjoiSldUIiwiYWxnIjoiUlMyNTYifQ.eyJzdWIiOiJqZG9lLXVzaW5nLWp3dC1yYmFjIiwiYXVkIjoidXNpbmctand0LXJiYWMiLCJ1cG4iOiJqZG9lQHF1YXJrdXMuaW8iLCJiaXJ0aGRhdGUiOiIyMDAxLTA3LTEzIiwiYXV0aF90aW1lIjoxNTUxNjUyMDkxLCJpc3MiOiJodHRwczpcL1wvcXVhcmt1cy5pb1wvdXNpbmctand0LXJiYWMiLCJyb2xlTWFwcGluZ3MiOnsiZ3JvdXAyIjoiR3JvdXAyTWFwcGVkUm9sZSIsImdyb3VwMSI6Ikdyb3VwMU1hcHBlZFJvbGUifSwiZ3JvdXBzIjpbIkVjaG9lciIsIlRlc3RlciIsIlN1YnNjcmliZXIiLCJncm91cDIiXSwicHJlZmVycmVkX3VzZXJuYW1lIjoiamRvZSIsImV4cCI6MTU1MTY1MjM5MSwiaWF0IjoxNTUxNjUyMDkxLCJqdGkiOiJhLTEyMyJ9.aPA4Rlc4kw7n_OZZRRk25xZydJy_J_3BRR8ryYLyHTO1o68_aNWWQCgpnAuOW64svPhPnLYYnQzK-l2vHX34B64JySyBD4y_vRObGmdwH_SEufBAWZV7mkG3Y4mTKT3_4EWNu4VH92IhdnkGI4GJB6yHAEzlQI6EdSOa4Nq8Gp4uPGqHsUZTJrA3uIW0TbNshFBm47-oVM3ZUrBz57JKtr0e9jv0HjPQWyvbzx1HuxZd6eA8ow8xzvooKXFxoSFCMnxotd3wagvYQ9ysBa89bgzL-lhjWtusuMFDUVYwFqADE7oOSOD4Vtclgq8svznBQ-YpfTHfb9QEcofMlpyjNA" http://127.0.0.1:8080/secured/roles-allowed; echo
```

## now go for the winners
```
curl -H "Authorization: Bearer YOUR_TOKEN" http://localhost:8080/secured/winners; echo
```

@@ go for the second winners
```
curl -H "Authorization: Bearer YOUR_TOKEN" http://localhost:8080/secured/winners2; echo
```
