# Configuring the EZ Proxy Stanza for digitaltheatreplus.com

> **Database Stanzas**
> Every resource that library users access remotely using EZproxy must be configured in EZproxy’s config.txt file. This file contains a listing of the e-resources that the library subscribes to with instructions for EZproxy about what resources within those websites users are allowed to access. The instructions are called directives, and when combined, these directives form database stanzas. When library users attempt to access an e-resource, after they have been authenticated, EZproxy reads the institution’s list of e-resources and directives in the config.txt file and determines whether or not the e-resource the user is trying to access is available to them, and either grants access (by rewriting the URL into a proxied URL) or denies access.
[help.oclc.org](https://help.oclc.org/Library_Management/EZproxy/EZproxy_for_content_providers)

```text
Title Digital Theatre Plus
HTTPHeader -request -process Accept-Encoding
URL https://www.digitaltheatreplus.com/
Domain digitaltheatreplus.com
Host www.digitaltheatreplus.com
Host https://www.digitaltheatreplus.com
HJ digitaltheatreplus.com
HJ www.digitaltheatreplus.com
HJ https://digitaltheatreplus.com
HJ https://www.digitaltheatreplus.com
DJ digitaltheatreplus.com
```
