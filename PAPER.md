# Introduction to JWT
Place holder

# Known Vulnerabilities
Place holder

# Potential Vulnerabilities
Place holder

# Solutions
Place holder

# Proper Usage of JWT
We recommand to use JWT for one-time authentication between multiple entities in service. One of example is SDK services. In case of SDK services, SDK provider needs to verify the client is authenticated user of service which is using SDK service. Then, client get a signed claim from its service and bring it to SDK provider. If the cryptographic proof, signature, is valid, SDK provider can trust the client and allow to use functions. JWT can be used for this signed claim to prove authentication of client between multiple services.

Another example is stateless micro-service architecture. With the rise of cloud services, many companies are using an Infrastructure as a Service (IaaS), such as Amazon Web Service or Google Cloud Platform and build many small statless components on top of it. For example, if you run stateless file server in your service, authentication server can issue a short-period ticket to download file for authenticated user. Since it has short expiration and is used only once, JWT can be used without weakness that we mentioned above.

# Conclusion

Many examples in web is suggesting use JWT to manage persistent session between server and client. However, it's even worse compared to traditional cookie based session management. As stated in RFC proposal, proper usage of JWT is claiming someone is authenticated from another service in cryptographic reliable way. SDK service or stateless micro service arhitecture is one of example of this kind of usage.