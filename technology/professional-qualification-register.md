# Professional Qualification Register

## Summary

Work in progress.

## Purpose of the building block

Work in progress.

## Concepts

[**Personal qualifications**](https://www.lawinsider.com/dictionary/personal-qualifications) means criteria related to an individual's personal background, including completion of an approved educational program, satisfactory performance on an examination, work experience, criminal history, moral standing and completion of continuing education.

Personal qualifications are issued by competent organizations to natural person. Examples include universities (education courses), former employers (work experience), governments (VOG statements, driving license), and terminals  & chemical plants (safety badge).

Employers can request the proof of personal qualifications from natural persons when they apply for a job. Periodic proofs by the employer could be performed to validate that the employees are still qualified.

When an employee interacts - representing his employer - with another organization  then this organization could have specific requirements towards the personal qualification of the employee. The legal contract between the organization and the employer would typically list the required personal qualification. However, in specific situations the organization has a need to check the required personal qualifications itself. Examples include the physical access to a site for which a safety training is required.

## Implementation Considerations&#x20;

The traditional paper based approach is to collect and store a physical file of the professional qualifications and to present the applicable qualifications when required. This is a cumbersome process and sensitive to fraud.

A modern approach is to collect the qualifications in an mobile app or a secure card. On request the employee can share the qualifications. Examples include the Vakpaspoort and the XS-ID of Secure Logistics.

The drawback of the app approach is that the different implementations are not interoperable. For example the protocols for retrieving the qualifications from the sources are not standardized. Also the protocols for presenting the qualifications are not standardized.&#x20;

The (open) European Wallet is an enticing prospect because it will standardize both the retrieving and the presentment of the qualifications as verifiable credentials in the personal wallet of the employee. These credentials can on request be presented towards the employee or other organizations when requested.&#x20;

A suggested alternative within the BDI is to store the professional qualifications in a register hosted by the employer. The employer could provide access to these qualifications to other organizations. This has however some heavy drawbacks:

* the personal qualifications are personal data and most likely privacy sensitive. Sharing this data with other organizations is from a legal perspective not trivial.
* It requires strong authorizations by the employer to ensure that the data is only accessible by the organizations which have a clear need to access the data. This translates into process costs for managing the checks and balances.
* It introduces a risk to be non-compliant with the GDPR
* It introduces a security risk (honey pot for hackers)

Therefore this alternative is not considered to be recommended by BDI.

## Interlinkages with other building blocks

## Elements and their key functions

## Core design decisions

## Future topics

## Further reading
