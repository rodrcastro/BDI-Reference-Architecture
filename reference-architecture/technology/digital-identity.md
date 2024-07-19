# Digital Identity

## Summary&#x20;

This building block supports trust among participants by defining how digital identies play a role in BDI. In it's implementation, BDI aligns with iSHARE's implementation of digital identities, relying on eIDAS's trusted lists of qualified Trusted Service Providers as trust anchors.

## Purpose of the building block&#x20;

The purpose of this building block is to support the framework for trust among parties, by ensuring that parties can provide and receive a verified digital identity. This way all interactions within BDI (onboarding, offboarding, data exchange, service consumption, etc.) will take place between trusted parties.&#x20;

## Concepts&#x20;

The following concepts (from the BDI Glossary), all regarding legal entities, are particularly relevant in this building block:&#x20;

<table><thead><tr><th width="262">Concept</th><th>Meaning</th></tr></thead><tbody><tr><td>Business Partners</td><td><ul><li>Members of other BDI Associations than the root BDI Association</li></ul></td></tr><tr><td>Member</td><td><ul><li>Legal entity as member of a root BDI Association</li></ul></td></tr><tr><td>Outsider</td><td><ul><li>Member of a BDI Association other than the root</li></ul></td></tr><tr><td>Preferred Business Partners</td><td><ul><li>Outsiders</li><li>Those who have agreed to the specific terms and conditions of the local BDI Association, which maintains its own Business Partner Reputation Model</li></ul></td></tr><tr><td>Visitor</td><td><ul><li>Outsider with a better reputation score than a set minimum</li></ul></td></tr></tbody></table>

Besides legal entities, identifiers for natural persons are part of BDI, as natural persons have a role as representee of a legal entity (in the [representation-register.md](representation-register.md "mention") and in the [professional-qualification-register.md](professional-qualification-register.md "mention")).&#x20;

<figure><img src="../../.gitbook/assets/BDI Roles v01.png" alt=""><figcaption></figcaption></figure>

## Risks

An insufficient framework for digital identity, might lead to a lower level of trust among parties and will harm the overall trust in BDI.

## Interlinkages with other building blocks&#x20;

This building block describes the BDI principles for digital identity, whereas the building block on [verifiable-credentials.md](verifiable-credentials.md "mention") describes how Verifiable Credentials are applied to exchange proof of identity between parties.

## Core design decisions&#x20;

BDI uses iSHARE principles on identity management. In particular these principles are defined here:

* [Facilitate portable identity(s) for parties and humans](https://framework.ishare.eu/is/facilitate-portable-identity-s-for-parties-and-hum)
* [Identification by EORI](https://framework.ishare.eu/is/identification-by-eori)
* [The role of Identity Provider](https://framework.ishare.eu/is/functional-requirements-per-role#Functionalrequirementsperrole-IdentityProvider)
* [The acknowledgment of eIDAS](https://framework.ishare.eu/is/regulation-on-electronic-identification-and-trust-)

On the technical side the following pages are relevant:

* [The PKI standard](https://dev.ishare.eu/reference/standards.html#pki)
* [The specifications for the Identity Provider role](https://dev.ishare.eu/identity-provider/authorize.html)

BDI relies on the iSHARE governance to select eID Providers that are accepted.&#x20;

## Future topics&#x20;

The iSHARE framework on the topic of digital identification is subject to [RFC031](https://gitlab.com/ishare-foundation/cab/rfc/-/issues/11). This will impact the BDI as well.

## Further reading&#x20;

This building block has been drafted using the following sources, that provide opportunity for further reading:&#x20;

* [DSSC Blueprint building block “Identity and Attestation Management](https://dssc.eu/space/BVE/357075352/Identity+and+Attestation+Management)&#x20;
* [https://www.w3.org/TR/vc-data-model-2.0/](https://www.w3.org/TR/vc-data-model-2.0/)
* [iSHARE Framework documentation](https://framework.ishare.eu/), specifically on the topic of identities
* [iSHARE Developer Portal documentation](https://dev.ishare.eu/)
