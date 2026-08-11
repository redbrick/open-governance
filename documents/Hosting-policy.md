# Disclaimer and Hosting Standards for Redbrick Infrastructure

## Hosting Agreement Overview

When utilising the Redbrick infrastructure for hosting services, a designated Point of Contact (POC) must be established for all communications with Redbrick. This individual will be responsible for the ongoing maintenance of the hosted service.

## Submission Requirements

In order to initiate hosting, the following information must be provided to Redbrick:

1. **Dockerfile**: A complete and accurate Dockerfile.
2. **Build Artifacts**: A pre-built and published image.
3. **Service Dependencies**: A list of services upon which the application depends on.

It is imperative that this information remains current. Should there be any changes, the POC must notify Redbrick immediately. At a minimum, the contact details must include an email address of the individual or entity in charge.

## Liability Disclaimer

While Redbrick is able to host the service, it does not claim any responsibility for the security or stability of that service, nor does it guarantee any amount of uptime. 

Additionally, Redbrick **will not** host any services that are illegal or violate any applicable laws or regulations of Ireland or the European Union.

Redbrick is also not responsible for managing or safeguarding the secrets or credentials of users or third parties.

## Vulnerability Management

In the event that the service's source code is hosted on GitHub, it is a requirement that Dependabot alerts or a similar mechanism is activated to monitor for potential vulnerabilities. 

In the case that a vulnerability or weakness is identified, Redbrick reserves the right to enforce a deadline for remediation based on the following severity levels:

- **Medium**: Up to 3-4 weeks for resolution
- **High**: Up to 2 weeks for resolution
- **Critical**: Immediate suspension of service until the vulnerability is addressed and resolved

> Severity levels are determined by the Common Vulnerability Scoring System (CVSS) or official GitHub Dependabot alerts, unless the Redbrick Sysadmin team alters the assigned severity level based on a justified technical reason

Should these standards not be adhered to, Redbrick retains the right to terminate hosting services without further notice. A formal notification will be provided to the designated Point of Contact.

## Conclusion

By engaging Redbrick's hosting services, all parties acknowledge and accept these terms and conditions. Further clarification regarding our offerings and limitations can be provided upon request.