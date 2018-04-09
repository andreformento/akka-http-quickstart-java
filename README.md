# akka-http-quickstart-java

### Requirements
- Java
- Sbt

### Run

- On OSX or Linux systems, enter `./sbt`
- On Windows systems, enter `sbt.bat`.

At the sbt prompt, enter `run`. Access on http://localhost:8080


- Add some users

```bash
curl -H "Content-type: application/json" \
     -X POST \
     -d '{"name": "MrX", "age": 31, "countryOfResidence": "Canada"}' \
     http://localhost:8080/users

curl -H "Content-type: application/json" \
     -X POST \
     -d '{"name": "Anonymous", "age": 55, "countryOfResidence": "Iceland"}' \
     http://localhost:8080/users

curl -H "Content-type: application/json" \
     -X POST \
     -d '{"name": "Bill", "age": 67, "countryOfResidence": "USA"}' \
     http://localhost:8080/users
```

- And then show users

```bash
curl http://localhost:8080/users
```

- To retrieve a specific user

```bash
curl http://localhost:8080/users/Bill
```

- Now `delete` Bill

```bash
curl -X DELETE http://localhost:8080/users/Bill
```

## References
- https://github.com/andreformento/akka-http-quickstart-java
