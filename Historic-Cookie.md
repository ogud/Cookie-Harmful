% Title = "DNS Cookie Harmful" 
% abbrev = "cookie-harmful"
% category = "standards"
% docName = "draft-ogud-dns-cookie-harmful-00"
% ipr= "trust200902"
% area = "Operations"
% workgroup = ""
% keyword = ["dns", "privacy"]
% updates="7873" 
% date = 2018-07-18T00:00:00Z
%
% [[author]]
% initials="O."
% surname="Gudmundsson"
% fullname="Olafur Gudmundsson"
% #role="editor"
% organization = "CloudFlare"
%   [author.address]
%   email = "olafur+ietf@cloudflare.com"
%   [author.address.postal]
%   street = ""
%

# Abstract

RFC7873 introduced a lightweigth intregity mechanism to DNS queries. 
This has been experimented with on the internet. The results from the
experiment have been that the cookies are not worth it.  
This document moves RFC7873 to historic. 

{mainmatter}

# Introduction

DNS Cookies[@RFC7873] is an attempt to add more integrity to DNS
transactions over UDP. RFC7873 says in introduction: 
This document describes DNS Cookies, a lightweight DNS transaction
   security mechanism specified as an OPT [RFC6891] option.  The
   DNS Cookie mechanism provides limited protection to DNS servers and
   clients against a variety of increasingly common abuses by off-path
   attackers.  It is compatible with, and can be used in conjunction
   with, other DNS transaction forgery resistance measures such as
   those
   in [RFC5452].  (Since DNS Cookies are only returned to the IP
   address
   from which they were originally received, they cannot be used to
   generally track Internet users.)

   The protection provided by DNS Cookies is similar to that provided
   by
   using TCP for DNS transactions.  Bypassing the weak protection
   provided by using TCP requires, among other things, that an
   off-path
   attacker guess the 32-bit TCP sequence number in use.  Bypassing
   the
   weak protection provided by DNS Cookies requires such an attacker
   to
   guess a 64-bit pseudorandom "cookie" quantity.  Where DNS Cookies
   are
   not available but TCP is, falling back to using TCP is reasonable.

Implementaion experience has shown that cookes have not lived upto
these goals, in particular anycast support is hard to implement
between different implementations. To addres these defect as well as
other ones in RFC7873 a update draft has been proposed to the dnsop working group, 


## Terminology
The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", 
"SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [@RFC2119].


# Cookies to Historic 

This document changes the status of RFC7873 to Historic 

## Reasons 
All the goals that Cookies promte can be addressed with other
mechanisms, like DNS over TCP, DNS over TLS and DNS over HTTPS. As
those are the transport mechanishms of the future the efforts of
implementors should be focused on those. 


# Security considerations 
Removal of DNS Cookies will reduce the complexity of DNS
components. 

# IANA considerations 

{backmatter}

# Acknowledgements 
This document is generated using the mmark tool that Miek Gieben has developed.


