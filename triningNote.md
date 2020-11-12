# TLS
 * Transport Layer Security, or TLS, is a widely adopted security protocol designed to facilitate privacy and data security for communications over the Internet. A primary use case of TLS is encrypting the communication between web applications and servers, such as web browsers loading a website. TLS can also be used to encrypt other communications such as email, messaging, and voice over IP (VoIP). In this article we will focus on the role of TLS in web application security.

 * TLS was proposed by the `Internet Engineering Task Force (IETF)`, an international standards organization, and the first version of the protocol was published in 1999. The most recent version is TLS 1.3, which was published in 2018.

> ## What is the difference between TLS and SSL?
* TLS evolved from a previous encryption protocol called Secure Sockets Layer (SSL), which was developed by Netscape. TLS version 1.0 actually began development as SSL version 3.1, but the name of the protocol was changed before publication in order to indicate that it was no longer associated with `Netscape`. Because of this history, the terms TLS and SSL are sometimes used interchangeably.

> ## What is the difference between TLS and HTTPS?
* HTTPS is an implementation of TLS encryption on top of the HTTP protocol, which is used by all websites as well as some other web services. Any website that uses HTTPS is therefore employing TLS encryption.

> ## What does TLS do?
There are three main components to what the TLS protocol accomplishes: Encryption, Authentication, and Integrity.
* `Encryption`: hides the data being transferred from third parties.
* `Authentication`: ensures that the parties exchanging information are who they claim to be.
* `Integrity`: verifies that the data has not been forged or tampered with.
