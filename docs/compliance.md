# NHS DSP Toolkit and UK GDPR Compliance

## 1. NHS Data Security and Protection Toolkit

The NHS Data Security and Protection Toolkit (DSPT) is an online self-assessment framework for organisations that access NHS patient data and systems. Organisations use it to assess their controls, identify gaps, and provide evidence of their data-security practices.

### Data security principles

- Make staff responsibilities clear and provide regular information-governance and security training.
- Use personal and confidential data only for an authorised purpose, and handle it lawfully and confidentially.
- Identify systems and services that store or process sensitive data, and maintain ownership and risk information for them.
- Maintain policies and procedures for data protection, records management, security incidents, and business continuity.
- Assess suppliers and processors that handle data, and define security responsibilities in appropriate agreements.

### Access control

- Give each user a unique account and grant only the access needed for their role and duties.
- Use strong authentication, including multi-factor authentication where supported, especially for remote or privileged access.
- Approve access before it is granted, review permissions regularly, and promptly change or revoke access when roles change or access is no longer needed.
- Separate privileged administration from routine user activity and protect administrative credentials.
- Keep appropriate audit records of access to sensitive systems and review alerts or unusual activity.

### Data protection measures

- Collect and retain only the information needed for a defined purpose; apply retention schedules and securely dispose of data when no longer required.
- Protect data in transit and at rest with appropriate encryption and key management.
- Use pseudonymised or synthetic information for development and testing wherever possible; never store real patient data or secrets in this repository.
- Protect backups, test recovery procedures, and ensure backup retention is consistent with data-retention requirements.
- Maintain a documented process to identify, contain, assess, record, and escalate security incidents and suspected data breaches.
- Keep systems supported and patched, and monitor for vulnerabilities and security events.

DSPT requirements and evidence depend on the organisation and services in scope. The controls above are planning guidance; the organisation should complete the applicable DSPT assessment and retain evidence rather than treating this summary as proof of compliance.

## 2. UK GDPR and personal data

Personal data is information that identifies, or can be used to identify, a living person. Health information is special-category personal data and requires additional protection. An organisation processing it must identify a lawful basis under Article 6 of the UK GDPR and a separate applicable condition under Article 9, and document why those choices apply.

The organisation responsible for deciding why and how data is processed (the controller) should:

- Explain the purpose, lawful basis, data categories, recipients, retention period, and individual rights in a clear privacy notice.
- Collect only data necessary for a specified purpose, keep it accurate, and retain it only as long as needed or legally required.
- Identify processors and ensure appropriate written arrangements and safeguards are in place.
- Assess risks before introducing new or high-risk processing, and involve the organisation's data protection officer or privacy lead where applicable.

### Consent

Consent is one possible lawful basis, not a default requirement for every use of personal data. It must be freely given, specific, informed, and indicated by a clear affirmative action. Where consent is the basis, the organisation should record what the person agreed to, when and how they agreed, and make withdrawal straightforward. Withdrawal applies to future processing relying on that consent; it does not automatically make earlier processing unlawful.

For health data, consent alone does not satisfy the additional Article 9 requirement. The controller must establish both the Article 6 lawful basis and an applicable Article 9 condition. The appropriate basis depends on the purpose and context; it should be assessed with qualified privacy or legal guidance, especially where there is a power imbalance or the person may not be able to refuse freely.

### Access and deletion requests

- **Access:** A person can request access to their personal data and supplementary information about its use. The controller should verify identity proportionately, locate relevant records, check for information that must be withheld or protected (including other people's data), and provide a clear response through a secure channel.
- **Deletion:** A person can request erasure, but the right is not absolute. The controller must assess whether an exception applies, for example where retaining information is necessary to meet a legal obligation or for another permitted purpose. Healthcare records may be subject to retention requirements, so a request should be assessed rather than automatically accepted or refused.
- **Handling requests:** Provide a usable contact route, record the request and decision, involve the privacy lead when needed, and respond within the applicable statutory timeframe. If a request cannot be fully met, explain why and describe any available next steps.

Other individual rights may also apply, including rectification, restriction, portability, and objection, depending on the circumstances and lawful basis.

## 3. Secure data handling

Controls should be selected for the actual system and risk. Relevant measures include:

- Restrict access to authorised people using unique accounts, least-privilege permissions, strong authentication, and periodic access reviews.
- Encrypt personal data in transit and at rest, and protect encryption keys and credentials separately from application code.
- Use pseudonymised or synthetic data for development and testing wherever possible. Do not commit patient data, credentials, or secrets to the repository.
- Avoid putting unnecessary personal or health information in logs. Protect audit records from unauthorised access or alteration, and monitor access and security events.
- Set documented retention and secure deletion rules for active systems, exports, and backups; protect backups and test recovery.
- Maintain a process for suspected personal-data breaches, including containment, assessment, documentation, and required notifications.

## 4. Application to HealthTechGov

The repository describes intended safeguards and does not currently demonstrate a live service processing patient data. Before any such processing, the project should define its data flows, purposes, controller/processor responsibilities, lawful bases, Article 9 condition, retention schedule, access-request process, and security controls. Those controls must then be implemented and verified in the target environment.

## 5. Conclusion

Applying UK GDPR principles and DSP Toolkit guidance helps protect personal information and build trust. Compliance depends on the facts of each processing activity and on effective, evidenced controls; this document is a planning guide, not legal advice or proof of compliance.

## References

- [NHS Data Security and Protection Toolkit](https://www.dsptoolkit.nhs.uk/)
- [Information Commissioner's Office (ICO): UK GDPR guidance and resources](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/)
- [UK GDPR, Regulation (EU) 2016/679](https://www.legislation.gov.uk/eur/2016/679/contents)
