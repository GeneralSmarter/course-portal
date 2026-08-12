<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-12T12:00:38.388284+12:00 -->
# ENEL301-26S2 weekly summary

## Coverage

- Week: 2026-W33, from 2026-08-10T00:00:00+12:00 to 2026-08-12T11:58:40.039233+12:00.
- Source covered: Lecture 9 summary, focused on data privacy and data ethics in engineering practice.
- Main areas: engineering responsibility for data, privacy and security, data breaches, confidentiality and NDAs, New Zealand privacy law, GDPR, Māori data sovereignty, and ethical frameworks.
- No mathematical equations were presented.

## Main concepts

- Engineers are data custodians because they design and operate systems that collect, process, store, transfer, and secure personal information.
- Data privacy concerns how personal information is collected, stored, accessed, used, corrected, transferred, and disclosed.
- Data ethics evaluates the fairness, transparency, consequences, and accountability of data practices.
- Privacy and security support stakeholder trust and an organisation’s social licence to operate.
- Personal-data benefits, such as efficiency, personalisation, prediction, and improved services, must be balanced against risks to privacy, security, fairness, justice, transparency, and autonomy.
- The Qantas and Optus examples showed that data breaches can cause identity theft, fraud, scams, reputational damage, regulatory penalties, litigation, and substantial financial losses.
- APIs must enforce authentication and authorisation. Sequential record identifiers must not allow unauthorised access to other users’ data.
- An NDA defines confidential information, permitted uses and disclosures, protection requirements, duration, and consequences of breach. Access to information does not automatically grant permission to copy, reuse, or disclose it.
- Confidentiality obligations may arise from professional codes even where no NDA exists.
- The New Zealand Privacy Act 2020 was discussed in relation to collection purpose, notification, security, access, correction, retention, disclosure, offshore transfers, and breach reporting.
- The GDPR may apply to a New Zealand company that has an EU establishment, offers goods or services to people in the EU, or monitors their behaviour.
- Māori data sovereignty emphasises self-determination, authority, consultation, participation, protection, and meaningful control over data concerning Māori communities.
- Engineers should avoid harmful deficit framing and consider whether data interpretation reinforces stereotypes.
- Virtue ethics, consequentialism, deontology, and professional codes provide different but complementary ways to assess data-related decisions.

## Equations and worked patterns

- No equations were presented.
- Worked engineering pattern from the Optus example:
  - Identify the data and system boundary.
  - Check authentication and authorisation.
  - Test whether identifiers allow record enumeration.
  - Restrict access to the requesting user’s authorised objects.
  - Consider consequences beyond the immediate technical failure.
- Worked privacy-assessment pattern for a data-collecting application:
  - What data is collected?
  - Why is it collected?
  - What secondary uses are possible?
  - What uses are disclosed to users?
  - Who can access it?
  - How long is it retained?
  - Can it be disclosed to law enforcement?
  - Can users access, correct, or contest decisions based on it?
- Worked international-compliance pattern from the Circularn scenario:
  - Identify the location and nature of users.
  - Review privacy notices and consent.
  - Check collection, retention, access, security, and transfer practices.
  - Determine whether EU users are being offered services or monitored.
  - Assess whether geo-blocking is appropriate, while recognising that it may not eliminate legal risk.

## Warnings and deadlines

- No deadlines were identified in the source.
- The lecture summary is not an authoritative statement of the Privacy Act 2020, Australian privacy law, GDPR, contract law, Engineering New Zealand’s code, or Treaty-related legislation.
- The exact wording and scope of the 13 New Zealand privacy principles were not provided and should be checked against the Act and Office of the Privacy Commissioner guidance.
- The lecture’s breach-reporting discussion was high-level; thresholds and procedures require verification from current official guidance.
- Optus breach figures, financial amounts, legal outcomes, and customer numbers were lecture claims and should be checked before formal citation.
- The Google data-erasure case was not clearly identified.
- The reference to the Data and Statistics Act contained an unclear year and requires verification.
- Whether a permitted disclosure can be made anonymously was unresolved.
- The Circularn scenario was hypothetical, and the legal consequences of VPN use, geo-blocking, and GDPR jurisdiction are fact-specific.

## Recall questions

1. Why can engineers be responsible for privacy even when they do not directly collect personal information?
2. What is the relationship between data privacy, data security, stakeholder trust, and social licence to operate?
3. Why was the Optus API failure serious from an authentication, authorisation, and record-enumeration perspective?
4. What issues should a student check before signing an NDA for an industry project?
5. What is a permitted disclosure, and what types of circumstances may allow or require one?
6. What access and correction rights were associated with the New Zealand Privacy Act 2020 in the lecture?
7. Under what circumstances might the GDPR apply to a New Zealand company?
8. What does Māori data sovereignty require engineers to consider?
9. What is deficit framing, and why should it be limited when processing Māori data?
10. How might virtue ethics, consequentialism, and deontology assess the same data-collection proposal differently?

## Practice priorities

- Be able to explain why engineers are data custodians and identify privacy responsibilities across a system lifecycle.
- Practise analysing APIs for authentication, authorisation, object-level access control, and record enumeration vulnerabilities.
- Compare the benefits and harms of collecting personal data, including effects on privacy, fairness, autonomy, and trust.
- Review NDA structure: confidential information, duration, permitted disclosure, pre-existing knowledge, independently developed work, and breach consequences.
- Build a privacy review checklist covering purpose, consent, access, correction, retention, disclosure, security, and offshore transfer.
- Distinguish legal compliance from broader ethical acceptability.
- Apply partnership, participation, and protection to engineering decisions involving Māori data.
- Use the Circularn scenario to practise identifying when international privacy obligations may arise.
- Treat all legal figures, thresholds, statutes, and case details from the lecture as items requiring authoritative verification before formal use.

## Missing or incomplete

- No missing or incomplete lectures were identified for this weekly period.
- Within the Lecture 9 source, the exact statutory wording of the New Zealand privacy principles, the Google data-erasure case, the year of the Data and Statistics Act reference, and the anonymous-disclosure question were unresolved or incomplete.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `20d31f929923b584471a213de023e941bad5d24c6095933d728b7c7d2501da23`; transcript `25a39067d19f7182ec497a65581d4e8d34d70f77fce684ddf449ace360312f68`; summary path `[local source path redacted]`
