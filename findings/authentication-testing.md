# Authentication Testing

## Objective

Evaluate authentication behavior and input handling
within a locally controlled OWASP Juice Shop environment.

## Methodology

Used Burp Suite Repeater to modify authentication
requests and compare HTTP response codes.

## Findings

- Invalid credentials returned HTTP 401 Unauthorized.
- Malformed input produced unexpected server errors.
- Boolean input testing returned HTTP 500.
- Empty email and password fields were tested separately.
- Valid credentials returned HTTP 200 OK.

## Assessment

Unexpected server errors indicate potential weaknesses
in input validation and exception handling.

SQL injection and authentication bypass were not confirmed.

## Recommendations

- Implement server-side input validation.
- Use parameterized database queries.
- Return consistent authentication error responses.
- Avoid exposing internal application errors.
