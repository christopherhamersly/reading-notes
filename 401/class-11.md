# Authentication 

## User Modeling
  - Modern web applications need to model sensitive information about their users. When a users provides an applications with sensitive information, they are trusting that it will not be leaked are misused. This means that it is a developers responsibility to store that information responsibly. 
    - Some information, like emails, user names, and addresses can be stored in plain text, as long as the database is password protected and/or behind a firewall.

  - User models that have sensitive data that should NEVER be sent to client applications. 

  - Cryptography is the science which studies methods for encoding messages so that they can be read only by a person who knows the secret information required for decoding, called the key; it includes cryptanalysis, the science of decoding encrypted messages without possessing the proper key, and has several other branches.

  - A Cryptographic Hash Algorithm takes a piece of data and produces a hash that is deliberately difficult to reverse. 

  - In a User model, a hash password can be stored when the user signs up. When the user needs to login, they can resend their password and the server can hash the login password using the same hash algorithm.

  - A Cryptographic Cypher Algorithm takes a piece of data and a key and produces encrypted data. Later the encrypted data can be reversed into the original data by decrypting it using the same key.

  - Basic Authorization is a common method used to send a username and password in an HTTP request

  - The BA mechanism provides no confidentiality protection for the transmitted credentials. They are merely encoded with Base64 in transit, but not encrypted or hashed in any way. Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.

  - Server side
    - When the server wants the user agent to authenticate itself towards the server, the server must respond appropriately to unauthenticated requests.

  - Client side
    - When the user agent wants to send authentication credentials to the server, it may use the Authorization field.

  - URL encoding
    - A client may avoid a login prompt when accessing a basic access authentication by prepending username:password@ to the hostname in the URL. For example, the following would access the page index.html at the web site www.example.com with the secure HTTPS protocol and provide the username Aladdin and the password OpenSesame credentials via basic authorization:

  - JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

  - Here are some scenarios where JSON Web Tokens are useful:

    - Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

    - Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.



