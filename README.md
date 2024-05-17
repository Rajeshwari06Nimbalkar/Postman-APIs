Postman Booking API 

# Description: 
A comprehensive tool for creating, organizing, and executing API tests, ensuring the reliability and functionality of the application.
JavaScript (Node.js): 
Leveraged for scripting within Postman tests, facilitating automation of validation and execution processes, enhancing efficiency and accuracy.
RESTful API: 
The API adheres to REST principles, enabling standardized communication and resource manipulation over HTTP, promoting interoperability and scalability.
Heroku: 
The API is deployed and hosted on the Heroku platform, providing cloud-based infrastructure with robust scalability and reliability, ensuring optimal performance and availability.
JSON (JavaScript Object Notation): 
Utilized as the data interchange format between the client (Postman) and the server (API), offering simplicity, readability, and flexibility in data representation.
## Running Tests

Execute each request in the collection and review the test results to ensure that the API endpoints behave as intended. Pay attention to the status codes, response bodies, and any error messages returned by the API.


## Features

- 1. Positive Endpoints
- **Get Booking IDs**: Retrieves a list of booking IDs from the API.
- **Create Booking**: Creates a new booking with the provided guest details.
- **Get Booking Details**: Retrieves details of a specific booking using its ID.
- **Token Generator**: Generates an authentication token for accessing protected endpoints.
- **Update Booking**: Updates an existing booking with new details.
- **Delete Booking**: Deletes a booking using its ID.

- 2. Negative Scenarios
- **Get Booking Details with Invalid ID**: Tests the API's response when attempting to retrieve details of a non-existent booking.
- **Create Booking with Invalid Characters**: Tests the API's handling of invalid characters in the request body.

These features cover both positive and negative scenarios to ensure thorough testing of the Booking API's functionality and error handling.
## Documentation

This section provides additional documentation and resources related to the Booking API testing project.

For detailed information about the endpoints, request parameters, and response formats of the Booking API, refer to the official API documentation:

[Booking API Documentation](https://restful-booker.herokuapp.com/apidoc/index.html)

### Postman Collection

The provided Postman collection (`Booking_API.postman_collection.json`) contains a set of requests for testing the Booking API. Import this collection into Postman or any other API testing tool that supports Postman collections to execute the tests.



## Environment Variables

To effectively run the tests in the provided Postman collection, you'll need to set up the following environment variables:

- **`{{fname}}`**: First name of the guest for creating a booking.
- **`{{lname}}`**: Last name of the guest for creating a booking.
- **`{{b_id}}`**: Booking ID. This variable is used to store the booking ID retrieved from the response of the "Create Booking" request. Subsequent requests, such as "Get Booking Details" and "Update Booking", depend on this variable to operate on the correct booking.
- **`{{b_token}}`**: Authentication token. This variable is used to store the authentication token retrieved from the response of the "Token Generator" request. It is required for authorization when performing actions like updating or deleting bookings.

Ensure that you set up these variables correctly in your testing environment. Depending on the tool you're using, you may configure these variables within Postman itself or through environment configurations in your testing framework.

## API Reference

This section provides an overview of the Booking API endpoints and their corresponding functionalities. For detailed information about request parameters, response formats, and authentication requirements, refer to the official API documentation linked below.

### Endpoints

1. **Get Booking IDs**
   - **Description**: Retrieves a list of booking IDs from the API.
   - **Method**: GET
   - **Endpoint**: `/booking`
   
2. **Create Booking**
   - **Description**: Creates a new booking with the provided guest details.
   - **Method**: POST
   - **Endpoint**: `/booking`
   
3. **Get Booking Details**
   - **Description**: Retrieves details of a specific booking using its ID.
   - **Method**: GET
   - **Endpoint**: `/booking/:id`
   
4. **Token Generator**
   - **Description**: Generates an authentication token for accessing protected endpoints.
   - **Method**: POST
   - **Endpoint**: `/auth`
   
5. **Update Booking**
   - **Description**: Updates an existing booking with new details.
   - **Method**: PUT
   - **Endpoint**: `/booking/:id`
   
6. **Delete Booking**
   - **Description**: Deletes a booking using its ID.
   - **Method**: DELETE
   - **Endpoint**: `/booking/:id`
   
### Authentication

- The "Token Generator" endpoint is used to generate an authentication token required for accessing protected endpoints.
- Once obtained, the token should be included in the request headers as an authorization token for endpoints that require authentication.

For more detailed information about each endpoint, including request and response examples, authentication requirements, and error handling, refer to the [Booking API Documentation](https://restful-booker.herokuapp.com/apidoc/index.html).


## Demo

Insert gif or link to demo

## Demo

To demonstrate how to use the Postman collection for testing the Booking API, follow these steps:

1. **Import the Collection**: Download the provided Postman collection (`Booking_API.postman_collection.json`) and import it into Postman.

2. **Set Up Environment**: Configure the necessary environment variables such as `{{fname}}`, `{{lname}}`, `{{b_id}}`, and `{{b_token}}`. Ensure that these variables are correctly populated with appropriate values.

3. **Execute Requests**:
   - Start by running the "Token Generator" request to obtain an authentication token.
   - Use the token to execute other requests like "Create Booking", "Update Booking", and "Delete Booking".
   - Verify the responses and test assertions to ensure that the API behaves as expected.

4. **Review Test Results**: Pay close attention to the test results in Postman. Ensure that all tests pass for each request, indicating that the API endpoints are functioning correctly.

5. **Explore Documentation**: Refer to the API documentation provided in the "Documentation" section for additional details about each endpoint and its expected behavior.

6. **Experiment and Learn**: Feel free to experiment with different scenarios, inputs, and configurations to deepen your understanding of how the Booking API works and how to effectively test it using the Postman collection.

By following these steps, you'll gain hands-on experience in using the Postman collection to interact with the Booking API and perform comprehensive testing.

## Tech Stack

**Client:** React, Redux, TailwindCSS

**Server:** Node, Express

## Demo

To demonstrate how to use the Postman collection for testing the Booking API, follow these steps:

1. **Import the Collection**: Download the provided Postman collection (`Booking_API.postman_collection.json`) and import it into Postman.

2. **Set Up Environment**: Configure the necessary environment variables such as `{{fname}}`, `{{lname}}`, `{{b_id}}`, and `{{b_token}}`. Ensure that these variables are correctly populated with appropriate values.

3. **Execute Requests**:
   - Start by running the "Token Generator" request to obtain an authentication token.
   - Use the token to execute other requests like "Create Booking", "Update Booking", and "Delete Booking".
   - Verify the responses and test assertions to ensure that the API behaves as expected.

4. **Review Test Results**: Pay close attention to the test results in Postman. Ensure that all tests pass for each request, indicating that the API endpoints are functioning correctly.

5. **Explore Documentation**: Refer to the API documentation provided in the "Documentation" section for additional details about each endpoint and its expected behavior.

6. **Experiment and Learn**: Feel free to experiment with different scenarios, inputs, and configurations to deepen your understanding of how the Booking API works and how to effectively test it using the Postman collection.

By following these steps, you'll gain hands-on experience in using the Postman collection to interact with the Booking API and perform comprehensive testing.


## Deployment

The Booking API is currently deployed and accessible at https://restful-booker.herokuapp.com. You can use this URL to interact with the API during testing.


## Contribution

Contributions are always welcome!

Contributions to improve this project are welcome! If you encounter any issues or have suggestions for enhancements, please open an issue or submit a pull request.


## Acknowledgements

 This project utilizes the Booking API hosted on Heroku (https://restful-booker.herokuapp.com). Special thanks to the developers and maintainers of the Booking API for providing this service.
## License

This project is licensed under the [MIT License](LICENSE). Feel free to modify and distribute it as needed.

## Feedback

Your feedback is valuable! If you have any questions, suggestions, or issues, please feel free to open an [issue](https://github.com/Rajeshwari06Nimbalkar/Postman-APIs/issues) 
or [pull request](https://github.com/Rajeshwari06Nimbalkar/Postman-APIs/pulls) on GitHub. We appreciate your contributions to improve this project.

