# Keycloak Service

*DO NOT USE THIS IN PRODUCTION. DO NOT USE ANY KEYS ASSOCIATED WITH THIS IF YOU DON'T WANT EVERYONE TO HAVE FULL ACCESS.*
*THIS IS A TESTING REPOSITORY ONLY*

## Setting up

* ran `docker run -p 8080:8080 -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=admin quay.io/keycloak/keycloak:11.0.2`
* admin login at http://localhost:8080/auth/admin
* created a realm called realm
* created user with password password
* tested user login at http://localhost:8080/auth/realms/realm/account
* created client with id client and root url https://www.keycloak.org/app/
* tested at https://www.keycloak.org/app/ (changine realm and client ids)


## Token
The token given was
```
{"access_token":"eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJFY3FxcC0zSVM5bkNvTHgxRndUaXoxdC1KY0tQOWkwRGVYbXY5WXJSODE0In0.eyJleHAiOjE2MDEzMDE5ODQsImlhdCI6MTYwMTMwMTY4NCwiYXV0aF90aW1lIjoxNjAxMzAxNjg0LCJqdGkiOiJjODM4ODU2MC1mMmYxLTQ0ZTktYWJhOC1iZmE5ZWFmNWNiNDkiLCJpc3MiOiJodHRwOi8vbG9jYWxob3N0OjgwODAvYXV0aC9yZWFsbXMvcmVhbG0iLCJhdWQiOiJhY2NvdW50Iiwic3ViIjoiNzJjMmE1ZDUtNGYwOS00Y2Q3LWJkZjUtMGZlMjlhMTM2NWQzIiwidHlwIjoiQmVhcmVyIiwiYXpwIjoiY2xpZW50Iiwibm9uY2UiOiI3YzdkNzM5NC02MzJjLTRjNWItOTU3MC1iOThlOTVmNDg5OGEiLCJzZXNzaW9uX3N0YXRlIjoiMjhjODE1MDYtZjhlYy00NGM3LTkzMDgtNDc3NjQyODAyZDA1IiwiYWNyIjoiMSIsImFsbG93ZWQtb3JpZ2lucyI6WyJodHRwczovL3d3dy5rZXljbG9hay5vcmciXSwicmVhbG1fYWNjZXNzIjp7InJvbGVzIjpbIm9mZmxpbmVfYWNjZXNzIiwidW1hX2F1dGhvcml6YXRpb24iXX0sInJlc291cmNlX2FjY2VzcyI6eyJhY2NvdW50Ijp7InJvbGVzIjpbIm1hbmFnZS1hY2NvdW50IiwibWFuYWdlLWFjY291bnQtbGlua3MiLCJ2aWV3LXByb2ZpbGUiXX19LCJzY29wZSI6Im9wZW5pZCBlbWFpbCBwcm9maWxlIiwiZW1haWxfdmVyaWZpZWQiOmZhbHNlLCJuYW1lIjoiVXNlciBOQSIsInByZWZlcnJlZF91c2VybmFtZSI6InVzZXIiLCJnaXZlbl9uYW1lIjoiVXNlciIsImZhbWlseV9uYW1lIjoiTkEiLCJlbWFpbCI6InVzZXJAcmJpcm0udXMifQ.fimxh71bqRieh4wUw5aYZ9R0i7Bu0tHzdQGUGvYskiDZa6eAZGjWW16_4Qpx9MDrp_05eeZtyXJ-76D_chqNr2k7uzqT7BPoANHVZXAL4GL-L4Vmf7fhNcclYOWj-tsizRi6oDfYvDxySN2EOTSvMliIhGHhGf0MpK9DNWxHwlKY5SuTqW-J38H3pPsomF8lA5YJW099BvA3yspQYbWnJcQ8Ac7rW6Z-cIRaSPlILDcX2talwjBEs0rFYomGRc2YfqpQQvRxnkVFLO5aNza3W_XB0DWa0g9pA5Dubq-vjd8tg5EJTVCiCjttYtwpztWedvgx3SrK7z6zUxfuePiqWA","expires_in":300,"refresh_expires_in":1800,"refresh_token":"eyJhbGciOiJIUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICIzM2EzMTljYS1hZTY2LTQ3M2UtYmM4Yy03ZDBlOWVmMWY3YWEifQ.eyJleHAiOjE2MDEzMDM0ODQsImlhdCI6MTYwMTMwMTY4NCwianRpIjoiYTRiNjA2YTYtOTA1ZC00MTY1LWIwNTEtZTU4MzYyMGZkNGFlIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL2F1dGgvcmVhbG1zL3JlYWxtIiwiYXVkIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL2F1dGgvcmVhbG1zL3JlYWxtIiwic3ViIjoiNzJjMmE1ZDUtNGYwOS00Y2Q3LWJkZjUtMGZlMjlhMTM2NWQzIiwidHlwIjoiUmVmcmVzaCIsImF6cCI6ImNsaWVudCIsIm5vbmNlIjoiN2M3ZDczOTQtNjMyYy00YzViLTk1NzAtYjk4ZTk1ZjQ4OThhIiwic2Vzc2lvbl9zdGF0ZSI6IjI4YzgxNTA2LWY4ZWMtNDRjNy05MzA4LTQ3NzY0MjgwMmQwNSIsInNjb3BlIjoib3BlbmlkIGVtYWlsIHByb2ZpbGUifQ.tca-YKI73nRAwy_ICxKwZjyLTCWBqj_qtlTFC9UQN90","token_type":"bearer","id_token":"eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJFY3FxcC0zSVM5bkNvTHgxRndUaXoxdC1KY0tQOWkwRGVYbXY5WXJSODE0In0.eyJleHAiOjE2MDEzMDE5ODQsImlhdCI6MTYwMTMwMTY4NCwiYXV0aF90aW1lIjoxNjAxMzAxNjg0LCJqdGkiOiIwZmNmOWNkMS02OTUwLTQzNDUtYmVmYS1kMTcxZTQ1YjJhZjciLCJpc3MiOiJodHRwOi8vbG9jYWxob3N0OjgwODAvYXV0aC9yZWFsbXMvcmVhbG0iLCJhdWQiOiJjbGllbnQiLCJzdWIiOiI3MmMyYTVkNS00ZjA5LTRjZDctYmRmNS0wZmUyOWExMzY1ZDMiLCJ0eXAiOiJJRCIsImF6cCI6ImNsaWVudCIsIm5vbmNlIjoiN2M3ZDczOTQtNjMyYy00YzViLTk1NzAtYjk4ZTk1ZjQ4OThhIiwic2Vzc2lvbl9zdGF0ZSI6IjI4YzgxNTA2LWY4ZWMtNDRjNy05MzA4LTQ3NzY0MjgwMmQwNSIsImF0X2hhc2giOiI2eUtRelU3S3BHLVVJQ2JJZ1lKSDlBIiwiYWNyIjoiMSIsImVtYWlsX3ZlcmlmaWVkIjpmYWxzZSwibmFtZSI6IlVzZXIgTkEiLCJwcmVmZXJyZWRfdXNlcm5hbWUiOiJ1c2VyIiwiZ2l2ZW5fbmFtZSI6IlVzZXIiLCJmYW1pbHlfbmFtZSI6Ik5BIiwiZW1haWwiOiJ1c2VyQHJiaXJtLnVzIn0.NeU8IayN8Y3Fkt9R-V7-MuDR77yD083r0lKZ1NbuVe_IhA8pY1FQ5eROMQISeFU0l82gOdnuW6KO8g5uLSKkax1x6NYR0bTYbPl8cnI0fcXYDbyDKTyAfaY01Gt6q_fbDdbcVyuaxV2snw7BovFaKku5_1ttByP8h44zuS_DftTh9DNKh3wKflKpcEc-VJ1j4VW69pYAK7jQ9738b5wOY6qiqyTvjqvN6982IsIxVFY2PLsq2WDvfJzWsfQT0PYNn9Yxi_WraWEK2wT4695S2cX5TLMtWJRGPzBXXqF92tl80FcddyhNsivE4G_TEi5jC2P40UU7a2lR0ycvKU9pZQ","not-before-policy":0,"session_state":"28c81506-f8ec-44c7-9308-477642802d05","scope":"openid email profile"}
```

Contains application info:
```json
{
  "exp": 1601301984,
  "iat": 1601301684,
  "auth_time": 1601301684,
  "jti": "c8388560-f2f1-44e9-aba8-bfa9eaf5cb49",
  "iss": "http://localhost:8080/auth/realms/realm",
  "aud": "account",
  "sub": "72c2a5d5-4f09-4cd7-bdf5-0fe29a1365d3",
  "typ": "Bearer",
  "azp": "client",
  "nonce": "7c7d7394-632c-4c5b-9570-b98e95f4898a",
  "session_state": "28c81506-f8ec-44c7-9308-477642802d05",
  "acr": "1",
  "allowed-origins": [
    "https://www.keycloak.org"
  ],
  "realm_access": {
    "roles": [
      "offline_access",
      "uma_authorization"
    ]
  },
  "resource_access": {
    "account": {
      "roles": [
        "manage-account",
        "manage-account-links",
        "view-profile"
      ]
    }
  },
  "scope": "openid email profile",
  "email_verified": false,
  "name": "User NA",
  "preferred_username": "user",
  "given_name": "User",
  "family_name": "NA",
  "email": "user@rbirm.us"
}
```
