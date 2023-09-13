# VDP
## Verified Document Protocol

With the rise of AI, deepfakes and other imitation of official organizations and people is a bigger problem than ever before. There is no established protocol for verifying whether a piece of media came from the source it claims besides, pergaps, hashing the media and checking against checsums on the organization's website. This is too cumbersome, inconviniant, and confusing, especially for a non-technical user. 

This protocol aims to ammend this problem, by creating an accepted set of rules for verifying if a piece of media came from an organization. 

## Technical
Before publishing, the organization's public key location and the domain the organization wants to show as verified is added to the metadata of the media. The media is then signed by the organization's private key. 

When a user downloads and displays or otherwise interacts with the media, the client reads the location of the public key from the metadata, and fetches it. The client then verifies the media with the public key. If the signatute is correct and the key came from a domain owned by the domain listed in the metadata as the one the organization wants to show, it's shown as verified in the client


A media could have a malicious domain in the metadata. Could this be dangerous?

A platform which is like a blog. It has to have tools for the user to make blog posts. 

When the user uploads a picture or document, it fetches the private key from enterprise key management, and signs it.

When the website signs the document, it signs something like "keyaddress:key.example.com/publickey.pgp, domaintoshow:example.com" into the metadata, so the signed message is where the key comes from. 

Also needs a viewer or tool which views/renders the document. It fetches the key from the specified address, checks if it is valid and says something like "This document was published by domaintoshow" (as long as domaintoshow is a domain belonging to the domain the key is on (eg. key.example.com belongs to example.com))

