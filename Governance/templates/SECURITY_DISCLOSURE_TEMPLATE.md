# Security Disclosure: [Short, non-exploitable title]

Copy this template into the repository's private GitHub security advisory
(**Security > Report a vulnerability**) and complete each section. Never paste a
completed copy into a public issue, pull request, discussion, or chat. Follow the
[Vulnerability Disclosure Process](../processes/VULN_DISCLOSURE.md) and the
[Security Policy](../SECURITY_POLICY.md); where this template and those documents
differ, those documents govern.

Fields marked _(maintainer)_ are completed by the case owner during triage, not by
the reporter.

## Report Details

- **Report date:** [YYYY-MM-DD]
- **Advisory or case ID:** _(maintainer)_ [GHSA ID or private security record ID]
- **Case owner:** _(maintainer)_ [Named maintainer from the
  [Security Response Team](../SECURITY_RESPONSE_TEAM.md)]
- **Acknowledged:** _(maintainer)_ [YYYY-MM-DD HH:MM UTC]

## Vulnerability Description

- **Summary:** [One or two sentences describing the weakness without a working
  exploit]
- **Vulnerability class:** [For example: authentication bypass, insecure storage,
  deep-link injection, SSL-pinning bypass, data exposure; add a CWE ID if known]
- **Affected component:** [Screen, module, API, build or release pipeline step, or
  documented integration]
- **Attack vector:** [Remote, adjacent network, local app, or supply chain]
- **Preconditions:** [User interaction, privileges, configuration, or device state
  required]

### Reproduction Steps

1. [Starting state, account type, and device or emulator used]
2. [Action taken]
3. [Observed result that demonstrates the issue]

- **Proof of concept:** [Attach privately, or describe; minimize real user data]
- **Expected secure behavior:** [What should happen instead]

## Affected Versions

Cite what a user can see in the app's settings screen. See
[Supported Versions](../SECURITY_POLICY.md#supported-versions) for which release
lines receive fixes.

| Field | Value |
|---|---|
| App version name | [For example: `1.16.4`] |
| Platform and build number | [iOS `buildNumber` / Android `versionCode`] |
| OS and device | [For example: Android 14, Pixel 8; iOS 18, iPhone 15] |
| Install source | [App Store, Google Play, TestFlight, EAS build, or local build] |
| First known affected version | [Version, or "Unknown"] |
| Confirmed unaffected versions | [Versions, or "Unknown"] |
| Fixed in | _(maintainer)_ [Version and build, once released] |

## Impact

- **What an attacker gains:** [Data, access, or capability obtained]
- **Who is affected:** [All users, specific roles, a platform, or a configuration]
- **Data involved:** [Personal data, learner or children's data, credentials,
  payment data, or none]
- **Known exploitation:** [None known, suspected, or confirmed, with evidence]
- **Workaround or mitigation:** [Steps users can take now, and whether they are in
  a released build]
- **Reporter-suggested severity:** [Critical, High, Medium, or Low]
- **Confirmed severity:** _(maintainer)_ [Level and rationale under the
  [Security Severity Rubric](../SECURITY_SEVERITY_RUBRIC.md)]

## Reporter Contact

- **Name or handle:** [As you want it to appear, or "Anonymous"]
- **Preferred private contact:** [GitHub advisory thread by default; any other
  channel only after a maintainer confirms it is private]
- **Timezone and availability:** [For example: UTC+1, weekdays]
- **Research collaborators:** [Names of anyone else with knowledge of the issue, or
  "None"]
- **Credit preference:** [Credit by name/handle with link, credit anonymously, or
  no credit]

Contact never moves to a public thread. Requests for anonymity limit access to
those on the embargo list.

## Embargo and Coordinated Disclosure

The [Embargo Policy](../policies/EMBARGO.md) governs this section. The default
embargo is 90 calendar days from confirmation as a credible issue.

- **Reporter's disclosure deadline:** [YYYY-MM-DD, or "Follow the project default"]
- **Planned external disclosure:** [Conference talk, blog post, CVE request, or none]
- **Embargo start:** _(maintainer)_ [YYYY-MM-DD, confirmation date]
- **Next embargo review:** _(maintainer)_ [YYYY-MM-DD]
- **Remediation target:** _(maintainer)_ [Date per the
  [Vulnerability Remediation SLA Policy](../policies/VULN_SLA.md)]
- **Expected advisory date:** _(maintainer)_ [No later than 14 calendar days after
  the fix is available, unless an early-disclosure exception applies]
- **Embargo list:** _(maintainer)_ [Roles and organizations granted access; kept to
  the minimum necessary]
- **Extension or early disclosure:** _(maintainer)_ [Reason, approver, and
  reporter consent, or "Not applicable"]

## Reporter Acknowledgements

- [ ] I have not disclosed this issue publicly or to anyone outside the
  collaborators listed above.
- [ ] I did not access, modify, or retain data that is not mine beyond what was
  needed to demonstrate the issue.
- [ ] I will keep details confidential until the embargo is lifted or a disclosure
  date is agreed.

## Maintainer Checklist

- [ ] Acknowledged within the [Security Severity Rubric](../SECURITY_SEVERITY_RUBRIC.md)
  target and private channel confirmed
- [ ] Initial triage update sent within seven calendar days
- [ ] Severity, affected versions, and embargo dates recorded in the private
  security record
- [ ] Fix released and update path available for affected users
- [ ] Advisory published with affected versions, fixed versions, mitigations, and
  credit
- [ ] Embargo list notified before publication

- **Status:** _(maintainer)_ [Reported, Triaged, Fixing, Fixed, Disclosed, or
  Declined]
- **Last updated:** [YYYY-MM-DD]

## Related Documents

- [`../processes/VULN_DISCLOSURE.md`](../processes/VULN_DISCLOSURE.md)
- [`../SECURITY_POLICY.md`](../SECURITY_POLICY.md)
- [`../SECURITY_SEVERITY_RUBRIC.md`](../SECURITY_SEVERITY_RUBRIC.md)
- [`../SECURITY_RESPONSE_TEAM.md`](../SECURITY_RESPONSE_TEAM.md)
- [`../policies/EMBARGO.md`](../policies/EMBARGO.md)
- [`../policies/VULN_SLA.md`](../policies/VULN_SLA.md)
