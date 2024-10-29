
Author : Karikalan Peramaiyan

This task has been done using the following environment versions

OS		: Ubuntu 18.04
Java	: 17.0.9
Spring Boot: 3.3.5
MySQL	: 8.0.18

Provided instructions are followed except request parameters validation.

Just run the maven builder
./mvnw spring-boot:run

Results
-------

1. karikalan@localhost:~$ curl http://localhost:8080/actuator/health | json_pp
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    15    0    15    0     0    394      0 --:--:-- --:--:-- --:--:--   394
{
   "status" : "UP"
}

2. karikalan@localhost:~$ curl http://localhost:8080/actuator | json_pp
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   243    0   243    0     0   8678      0 --:--:-- --:--:-- --:--:--  8678
{
   "_links" : {
      "self" : {
         "href" : "http://localhost:8080/actuator",
         "templated" : false
      },
      "health" : {
         "templated" : false,
         "href" : "http://localhost:8080/actuator/health"
      },
      "health-path" : {
         "href" : "http://localhost:8080/actuator/health/{*path}",
         "templated" : true
      }
   }
}

Tested using firefox browser
3. http://localhost:8080/next-tracking-number?customer_name=kalan&customer_id=de619854-b59b-425e-9db4-943979e1bd49&origin_country_id=MY&destination_country_id=ID&weight=1.123&created_at=2024-10-29T06:59:37.801+00:00&customer_slug=kalan


trackingNumber	"C6NQD3128D75NDO5"
createdAt	"2024-10-29T1:33:17+05:30"
_links
self	{…}
href	"http://localhost:8080/next-tracking-number?origin_country_id=MY&destination_country_id=ID&weight=1.123&created_at=2024-10-29T06%3A59%3A37.801%2000%3A00&customer_id=de619854-b59b-425e-9db4-943979e1bd49&customer_name=kalan&customer_slug=kalan"
