# Professional Qualification Register

## Summary

Work in progress.

## Purpose of the building block

The purpose of the building block is to specify the interface and structure for storing and validating professional qualifications to allow automated recognition by the BDI participants so they can be used as proof of competency conditions to improve the statement of compliance and granting (data or physical) access.

## Concepts

[**Personal qualifications**](https://www.lawinsider.com/dictionary/personal-qualifications) means criteria related to an individual's background, including completion of an approved educational program, satisfactory performance on an examination, work experience, testimonials and completion of continuing education.

Personal qualifications are issued by competent organizations to natural person. Examples include universities (education courses), former employers (work experience), governments (VOG statements, driving license), and terminals  & chemical plants (health and safety courses).

Employers can request proof of personal qualifications from natural persons when they apply for a job. Periodic the employer could check the validity that the employee are still qualified before being assigned to task that require this qualification. This would equally apply to staff that are associated with a legal entity. The natural person should associate their professional qualification for reuse by an employer or client.&#x20;

From here on we refer to 'staff' which is a more general, simply referring to someone part of a team which could be employee or contractor.&#x20;

When staff interacts - representing his employer or client - with another organization then this organization could have specific requirements towards the personal qualification of the employee or staff. The legal contract between the organizations would typically list the required personal qualification (explicit requirment). However, in specific situations the organization has a need to check the required personal qualifications itself (implicit expectation of compliance to common requirments). Examples include the physical access to a site for which a safety training is required.

## Implementation Considerations&#x20;

The traditional paper based approach is to collect and store a physical file of the professional qualifications and to present the applicable qualifications when required. This is a cumbersome process and sensitive to fraud as many copies are kept at multiple sources of which varying levels of controls are applied to validate authenticity and validity of the evidence.

A modern approach is to collect the qualifications in an mobile app or a secure card. On request the employee can share the qualifications. Examples include the [Vakpaspoort of the Centraal Register Techniek](https://centraalregistertechniek.nl/app-vakpaspoort-techniek) and the [XS-ID of Secure Logistics](https://www.secure-logistics.nl/en/xs-key/).

The drawback of the app approach is that the different implementations are not interoperable. For example the protocols for retrieving the qualifications from the sources are not standardized. Also the protocols for presenting the qualifications are not standardized.&#x20;

The (open) European Wallet is an enticing prospect because it will standardize both the retrieving and the presentment of the qualifications as verifiable credentials in the personal wallet of the employee. These credentials can on request be presented towards the employee or other organizations when requested.&#x20;

A suggested alternative within the BDI is to store the professional qualifications in a register (can be with an association). The association could provide access to these qualifications to requesting other organizations. The following it to be considered:

* the personal qualifications are personal data and most likely privacy sensitive. Sharing this data with other organizations is limited to its purpose meaning that anything else not trivial is to be masked.
* It requires clear authorization conditions to be provided to the association to ensure that the data is only made available to the organizations that can present clear evidence of the need need to access the data.

## Interlinkages with other building blocks

## Elements and their key functions

## Core design decisions

## Future topics

## Further reading
