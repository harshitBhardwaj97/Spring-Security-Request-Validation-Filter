# Spring-Security-Request-Validation-Filter

This project provides a custom Spring Security filter for validating HTTP request headers. Specifically, it checks the
presence of a `Request-Id` header and returns a 400 status if the header is missing or invalid.

## Key Features

- Validates the `Request-Id` header in incoming HTTP requests.
- Responds with a `400 Bad Request` if the header is missing or invalid.

## Usage

Integrate this filter into your Spring Security filter chain to ensure that requests contain a valid `Request-Id`
header.

- **Valid Request (200 OK)**:  
  To test a valid request with the required `Request-Id` header, use the following curl command:
  ```bash
  curl -vH "Request-Id: 12345" http://localhost:8080/hello
    ```

- **Invalid Request (400 Bad Request)**:  
  To test an invalid request, either omit the Request-Id header or provide an empty value:
  ```bash
  curl -v http://localhost:8080/hello
  ```