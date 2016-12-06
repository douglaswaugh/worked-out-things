Work out what the location HTTP header does
===

Provides a URI to reference to a specific resource required by some responses.

For example by 201 (Created) responses, where the location header should contain the URI for the newly created resource.  Also, the 3xx (Redirection) responses also use the location header to tell the client where the resource requested has moved to.

Move information can be found in [section 7.1.2][1] of the [Hypertext Transfer Protocol (HTTP/1.1)][2] specification.

[1]: https://tools.ietf.org/html/rfc7231#section-7.1.2 "Hypertext Transfer Protocol (HTTP/1.1) RFC 7231, section 7.1.2 Location"
[2]: https://tools.ietf.org/html/rfc7231 "Hypertext Transfer Protocol (HTTP/1.1) RFC 7231"