# Corkboard Project: Technical Design
draft 1

## Identity Subsystem
codename: ausweis
Subsystem serves the role of robust identity manager. Must support:
- providing a strong cryptiographic proof of identity. Identity could be pseudonymous
- linking user posts signed by different keys to a single identity
- revoking compromised keys

### User-owned identity
problem: must provide a way for user to persist presence across social networks, all of which are untrusted.
solution (ideas): 
- short-term: require a service running on user's desktop, which will work as a personal key server.
- use https://developer.mozilla.org/en-US/docs/Web/API/Web_Authentication_API to sign the content?..
- perhaps utilize some form of pgp?..

### Multiple browsers
problem: user could use multiple browsers, hence multiple keys. how to ensure that identities are linked?

### Hacked browsers
problem: user creds could become compromised. need to establish a process of blocking compromised identity and replace it with new

## Storage Subsystem
codename: tamagochi
objective: persistence layer for content; p2p service to exchange data; API for data retrieval; API for moderation and cleanup

problem: user may or may not store content stream locally. who's going to store it?
solution: user must enter into contract with one or more of social network providers. These are expected to store posted content,
but they also may delete it according to their policies. User may optionally use "local" network provider, which could be configured
to store everything

## User Interface
codename: bazinga
objective: provide generic local UI for network browsing, serve as a template for social network provider



