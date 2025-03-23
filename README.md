# basic auth 
Step 1 Registration
curl --location 'http://localhost:8080/register' \
--header 'Content-Type: application/json' \
--header 'Cookie: JSESSIONID=D4E0CF72C1EFB703DB7D284FF5E551BB' \
--data '{
    "id":1,
    "userName":"rk",
    "password":"rk"
}'

Response:
{
    "id": 2,
    "userName": "rk2",
    "password": "$2a$10$V6ubNRf31T0y.GyMI.K7cuRVlrWhQKZwQ6WBynMhz2b871/eGtjuS"
}

Step 2 Login using username and password with basic auth
curl --location 'http://localhost:8080/login' \
--header 'Content-Type: application/json' \
--header 'Authorization: Basic cms6cms=' \
--header 'Cookie: JSESSIONID=D4E0CF72C1EFB703DB7D284FF5E551BB' \
--data '{
    "id":1,
    "userName":"rk",
    "password":"rk"
}'

response: 
{"id":1,"userName":"rk","password":"$2a$10$aUc/QR05dPSj4dn8wPP0QeqcBLZ0T7zODZNn/.zX9cZNqN7iV1/3S"}
