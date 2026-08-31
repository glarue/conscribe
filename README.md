# Conscribe

A local-first, end-to-end-encrypted shared shopping list for a household. No
accounts, no ads, no server that holds your data.

Your lists live on your devices. When they sync they go directly between your
devices over the local network where possible, and through a relay that cannot
read them when your devices are apart. There is no sign-up, and nobody running
Conscribe has a list of who uses it, because no such list is created.

- [Privacy policy](https://glarue.github.io/conscribe/privacy-policy.html)

## What is public here

This repository is the project's public face: the privacy policy, and links to
the components that are open.

The app itself is not open source. The parts that carry the security claims are
being published separately, because those are the ones worth checking rather
than taking on trust:

- **The relay** — the mailbox service that passes encrypted messages between
  devices. Its entire claim is that it can read nothing, and it is small enough
  to read in an evening. Self-hosting it is the intended answer for anyone who
  would rather not use the default one. *(not yet published)*
- **The cryptography core** — MLS (RFC 9420) for group state and Noise for
  device pairing, composed from audited implementations. The project's rule is
  that it never hand-rolls cryptography; publishing this is what makes that
  checkable rather than merely asserted. *(not yet published)*

Publishing these is not a claim that they have been audited. Nobody has audited
them. It means the claims made about them can be checked, and cannot quietly
change later.
