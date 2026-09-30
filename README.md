# Postman API Tests. 

The project demonstrates practical API testing techniques including positive and negative scenarios, response validation, boundary testing, and test data handling.

## What I'm Practicing

* REST API testing
* HTTP methods and status codes
* Request and response validation
* JSON response validation
* Positive and negative testing
* Boundary value testing
* Input validation
* Response time checks
* Environment variables
* Request chaining
* Basic Postman test scripting
* Organizing API tests into collections

## Test Coverage

The collection includes scenarios covering:

* GET requests
* POST requests
* PUT requests
* DELETE requests
* Successful responses
* Invalid input
* Non-existing resources
* Required fields
* Boundary values
* Response body validation
* Response data types
* Response headers
* Response time

## Example Test

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

const data = pm.response.json();

pm.test("Response contains user ID", function () {
    pm.expect(data).to.have.property("id");
});

pm.test("User ID is a number", function () {
    pm.expect(data.id).to.be.a("number");
});
```

## Project Structure

```text
postman-api-tests/
├── README.md
├── collections/
│   └── api-tests.postman_collection.json
├── environments/
│   └── test.postman_environment.json
└── test-cases.md
```

## Tools

* Postman
* JavaScript
* REST API
* JSON
* Git / GitHub

## Running the Tests

1. Install Postman.
2. Import the collection from the `collections` folder.
3. Import the environment from the `environments` folder, if applicable.
4. Select the required environment.
5. Open the collection.
6. Run the collection using the Collection Runner.

## Goals

This project is part of my ongoing QA learning and portfolio development.

The focus is on applying manual QA knowledge to API testing and gradually developing practical test automation skills using Postman and JavaScript.
