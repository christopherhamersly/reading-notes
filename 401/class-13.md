# Bearer Authorization

  - Header
    - The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA
  - Payload
    - The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.
      - Registered claims: These are a set of predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims. Some of them are: iss (issuer), exp (expiration time), sub (subject), aud (audience), and others.
      - Public claims: These can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.
      - Private claims: These are the custom claims created to share information between parties that agree on using them and are neither registered or public claims.
      - 
  - What is the JSON Web Token structure?
    - In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

      1. Header
      1. Payload
      1. Signature
      - Therefore, a JWT typically looks like the following.

        - xxxxx.yyyyy.zzzzz

  - Following a signin attempt, either using Basic Authentication (where your username and password are transmitted to a server) or OAuth (where there is a cumbersome handshaking/authorization process), your service is able to make a boolean decision as to the success of the attempt.
  - Assuming the signin was successful, we can assert that it would be both more efficient and secure if the server “just knew” that the client making subsequent requests was allowed to do so.
  - Rather than continually sending username+password over the internet, or undergoing the long OAuth process, we are able to use a secondary authentication method called “Bearer Token”
  - Bearer Tokens are sent to the user/client after the initial signin process has completed.
  - Clients must make every subsequent request to the server with that token, in the header
    - Authorization: Bearer encoded.jsonwebtoken.here
  - The server opens the token, does the re-authentication, and then grants or denies access
  - In express servers, this can be done in middleware, in conjunction with a user mode
  - JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transmitting information between parties (servers, clients, etc) as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.
  - When should you use JSON Web Tokens?
    - Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.
    - Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload.
