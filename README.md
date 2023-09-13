# VDP
## Verified Document Protocol

With the rise of AI, deepfakes and other imitation of official organizations and people is a bigger problem than ever before. There is no established protocol for verifying whether a piece of media came from the source it claims besides, pergaps, hashing the media and checking against checsums on the organization's website. This is too cumbersome, inconviniant, and confusing, especially for a non-technical user. 

This protocol aims to ammend this problem, by creating an accepted set of rules for verifying if a piece of media came from an organization. 

## Technical
Before publishing, the organization's public key location and the domain the organization wants to show as verified is added to the metadata of the media. The media is then signed by the organization's private key. 

When a user downloads and displays or otherwise interacts with the media, the client reads the location of the public key from the metadata, and fetches it. The client then verifies the media with the public key. If the signatute is correct and the key came from a domain owned by the domain listed in the metadata as the one the organization wants to show, it's shown as verified in the client

In the future, it might be possible to leverage SSL certificates to authenticate the domain and organization name a media comes from