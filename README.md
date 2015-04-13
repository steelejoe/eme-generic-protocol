# eme-generic-protocol
Strawman proposal for a generic license request/response protocol for use by Key Systems using the Encrypted Media Extensions API. 

At the October 2014 W3C TPAC meeting we had some brief discussion about the need for a common request/response protocol, roughly parallel to the Common PSSH Format that is supported by the EME spec today. There was some agreement that such a protocol would be useful but no proposals have come to light yet (as far as I know). I believe this would be a useful tool in addressing some of the concerns raised:
[Perspectives on Encrypted Media Extensions](http://www.w3.org/blog/2013/05/perspectives-on-encrypted-medi) 
[Bug 20944 - EME should do more to encourage/ensure CDM-level interop](https://www.w3.org/Bugs/Public/show_bug.cgi?id=20944)
[Bug 27055 - Surfacing license to the user](https://www.w3.org/Bugs/Public/show_bug.cgi?id=27055)

This project contains descriptions of the request and response data formats. The initial versions are ASN.1, but can and should be translated into JSON, XML, and any other syntax folks feel is useful. We should pick a single syntax for the final proposal though, because supporting multiple would be problematic due to the digital signatures required.

This is NOT intended to capture all the various rules and policies supported by all DRMs today. It is intended to reflect only those features which are suppported today are are likely to b supported in the near future by the Encryted Media Extensions spec. 

Supporting this protocol for the User Agent would mean that Key Systems would produce requests and consume responses in the proposed formats. Supporting this request on the server side would mean that a service is available which will consume requests and produce responses. In either case new support must be added, since this is a new protocol (although it should map fairly well to all existing DRM provider protocols). 
