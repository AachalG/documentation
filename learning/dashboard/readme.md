## This directory is the placeholder for all Dashboard and frontend related learnings

### Please use this directory to raise PRs for the learning issues created.
## Authentication methods :

- Authentication is the process of verifying an identity. For example, you can prove your identity by showing an ID card or driver's license. Similarly, RESTful service clients must prove their identity to the server to establish trust.

- RESTful API has three common authentication methods:

### HTTP authentication
HTTP defines some authentication schemes that you can use directly when you are implementing REST API. The following are two of these schemes:

#### Basic authentication :

In basic authentication, the client sends the user name and password in the request header. It encodes them with base64, which is an encoding technique that converts the pair into a set of 64 characters for safe transmission.

![](https://assets.website-files.com/5ff66329429d880392f6cba2/61e7b5289894978b8941d1a0_basic%20authentication%20Preview.jpg)

#### Bearer authentication :

The term bearer authentication refers to the process of giving access control to the token bearer. The bearer token is typically an encrypted string of characters that the server generates in response to a login request. The client sends the token in the request headers to access resources.

### API keys
API keys are another option for REST API authentication. In this approach, the server assigns a unique generated value to a first-time client. Whenever the client tries to access resources, it uses the unique API key to verify itself. API keys are less secure because the client has to transmit the key, which makes it vulnerable to network theft.

### OAuth
OAuth combines passwords and tokens for highly secure login access to any system. The server first requests a password and then asks for an additional token to complete the authorization process. It can check the token at any time and also over time with a specific scope and longevity.

## Server Response :

- server response means a client sends a message in form of a HTTP Request and the server responds in the form of an HTTP Response. This technique is termed as Messaging.

- REST principles require the server response to contain the following main components:

### Status line
- The status line contains a three-digit status code that communicates request success or failure. For instance, 2XX codes indicate success, but 4XX and 5XX codes indicate errors. 3XX codes indicate URL redirection.

#### The following are some common status codes:
  * 200: Generic success response
  * 201: POST method success response
  * 400: Incorrect request that the server cannot process
  * 404: Resource not found

  ### Message body
- The response body contains the resource representation. The server selects an appropriate representation format based on what the request headers contain. 
- Clients can request information in XML or JSON formats, which define how the data is written in plain text. For example, if the client requests the name and age of a person named John, the server returns a JSON representation as follows:

    '{"name":"John", "age":30}'

### Headers
- The response also contains headers or metadata about the response.

- They give more context about the response and include information such as the server, encoding, date, and content type.
