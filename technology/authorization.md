---
description: >-
  This document is prepared for
  https://topsectorlogistiek.atlassian.net/browse/DEA-110.
---

# Authorization

{% hint style="warning" %}
The content of this page is to be replaced with the new version in [authorization-and-trust-assessment.md](authorization-and-trust-assessment.md "mention")
{% endhint %}

## Summary&#x20;

## Purpose of the building block&#x20;

## Concepts&#x20;

The following concepts (from the BDI Glossary) are particularly relevant in this building block:&#x20;

<table><thead><tr><th width="207">Concept</th><th>Meaning</th></tr></thead><tbody><tr><td>Data Owner </td><td><ul><li>Has control over data and access to data,   </li><li>Controls decisions on Data Sovereignty and Trust Sovereignty  </li><li>Controls authorisation policies, representation rules, professional qualification verification of staff and contactors    </li><li>Controls subscription to the Event Pub/Sub Service, and publishing of events to subscribers  </li><li>Controls discovery and endpoints  </li><li>Controls roles assumed by entity </li></ul></td></tr><tr><td>Data Consumer </td><td><ul><li>Requests access to data and/or Representation Register and/or Professional Qualification Register of the Data Owner  </li><li>Controls discovery and endpoints  </li><li>Requests subscription to Event Pub/Sub Service of the Data Owner, receives and evaluates events  </li></ul></td></tr><tr><td>Data Service Provider </td><td><ul><li>A Service Provider that acts under supervision and on behalf of the Data Owner </li></ul></td></tr></tbody></table>

## Risks&#x20;

## Interlinkages with other building blocks&#x20;

This building block has links to:&#x20;

* [Business Partner Reputation model](business-partner-reputation-model.md)&#x20;
* [Zero Trust check](zero-trust-check.md)
* [Association Register ](association-register.md)
* [Data licenses ](data-licenses.md)

## Elements and their key functions&#x20;

A Data Owner must decide which Data Consumer can access the data of the Data Owner at a Data Service Provider. To determine whether or not the Data Consumer is trusted and can be provided with an authorisation, the Data Owner will follow the logic:&#x20;

1. Do I trust the party on the basis of membership of an Association, one of it’s parent Associations or the root BDI Network?&#x20;
2. Do I require additional trust based on the reputation of the Member as provided by the Reputation Model?&#x20;

This building block describes how step 1 can be performed and facilitated by the BDI Framework specifications. Step 2 is part of the building block “Business Partner Reputation model”.&#x20;

This building block also defines the concept and shape of authorisations when used as authorisation evidence in data transactions.&#x20;

## Core design decisions&#x20;

### Authorisations&#x20;

In terms of the technical specifications for Authorisations, the BDI Framework builds on the iSHARE Trust Framework. The iSHARE Trust Framework uses the term “delegations” for the concept that in BDI is called Authorisations.&#x20;

* The framework defines [the role of an Authorisation Registry](https://framework.ishare.eu/is/framework-and-roles)&#x20;
* Entitled Parties are enabled in exercising data sovereignty by providing delegations (as described in the [generic use cases](https://framework.ishare.eu/is/use-cases)) to parties to use their data&#x20;
* [Licenses](https://framework.ishare.eu/is/licenses) further specify to legal boundaries of the data usages&#x20;
* The [structure of delegation](https://framework.ishare.eu/is/structure-of-delegation-evidence) evidence is defined in the framework and technical requirements for Authorisations and on the [iSHARE Developer Portal](https://dev.ishare.eu/).&#x20;

All mentioned iSHARE requirements must be considered as BDI requirements.&#x20;

### Trust processing&#x20;

To determine whether or not a party can be trusted on the basis of membership of an Association, one of its parent Associations or the root BDI Network, the following steps can be followed:&#x20;

1. Retrieve party information from an Association Registry (by invoking the /parties/{party\_id} endpoint. The retrieved party information contains a list of association of which the party is a member of.&#x20;
2. If this membership information is not enough to establish trust, proceed retrieving all associations and traverse the tree of associations until trust can be established.&#x20;

If this does not lead to trust, then use the second method mentioned above (trust based on reputation model).&#x20;

{% hint style="info" %}
As defined on [https://dev.ishare.eu/satellite/dataspaces.html](https://dev.ishare.eu/satellite/dataspaces.html), a dataspace must contain the field “tags”. This field must contain the parent dataspace in the following form:

`parent:<id_of_parent_dataspace>`

Traversing the parents of BDI associations (dataspaces) will always eventually lead to the discovery of the BDI Root Association (dataspace), which has the ID: EU.DS.BDI.NL.ROOT.
{% endhint %}

### Future topics

For improved discoverability of the parents of a BDI Association, the BDI Association Register could be improved by returning this information for every party lookup directly as part of the party information.

### Further reading

This building block has been drafted using the following sources, that provide opportunity for further reading:

* [DSSC Blueprint building block “Participation Management”](https://dssc.eu/space/BVE/357074624/Participation+Management)
* [iSHARE Framework documentation](https://framework.ishare.eu)
* [iSHARE Developer Portal documentation](https://dev.ishare.eu)
* [iSHARE Dataspace Template, section Access & usage policies and enforcement](https://template.ishare.eu/data-sovereignty-and-trust/access-and-usage-policies-and-enforcement)

