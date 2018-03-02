<!-- Answers to the Short Answer Essay Questions go here -->
1. Describe Middleware, Sessions (as we know them in express), bcrypt and JWT.

Middleware is a function that takes place/is given control during the execution of asynchronous functions and resolve before the resolution of the asynchronous function.
Sessions are a part of sessions middleware in express that is stored on sessionID, server-side. It allows for data to persist through multiple functions.
bcrypt is a middleware that deals with secure data, usually passwords, by hashing plain text into encrypted, randomized hashes and deals with checking/validating of the hashes as well.
JWTs, JSON Web Tokens, is a way of dealing with security, it's a 3-piece, hashed string separated by '.' that is generated upon logging in and generally has an expiration, it's stored client-side. It is then validated by the server as being a token that was granted access to data and deals with it accordingly.

2. What does bcrypt do in order to prevent attacks?

It hashes all sensitive material (first), allowing no storage of plain text. It then is gated by a hash function which has a built in Bcrypt cost that can be changed to limit how many hashes can be generated per millisecond/second. This prevents rainbow tables due to the sheer amount of time it would take to generate all the basic letters/words, usually many years in total. 

3. What are the three parts of the JSON Web Token

Header: Type of algorithm used to encrypt the token and the type of token

Payload: The claims to make using the token

Signature: Uses the encoded header, encoded payload, and the secret and uses the algorithm specified by the header to create a unique signature that verifies the client sending the JWT
