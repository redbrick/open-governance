# Disclaimer and Hosting Standards for Redbrick Infrastructure

## Hosting Agreement Overview

When you host a project on Redbrick, a designated Point of Contact (PoC) must be established for all communications with Redbrick. This individual will be responsible for maintaining the project.
## Submission Requirements

Before we start hosting your project you need to:
1. Set up a mirror of your code to Redbrick Git.
2. Upload a Docker image to our container registry.
3. Keep track of dependencies and security vulnerabilities (e.g. Use Dependabot on GitHub).
4. Provide an up to date and well documented list of any requirements (resource utilisation, open ports etc.)

This information **must** stay up-to-date. If there are any changes, the PoC must notify Redbrick immediately. At a minimum, the contact details must include an email address of the individual or group responsible for maintaining the project.

While you do not need to primarily manage your project using our Git hosting services, we require that you **mirror** your repository to Redbrick Git and upload your Docker image to our container registry. We **cannot** accept GitHub credentials under any circumstances.
## Disclaimer

While we will do our best to host your project, we **do not** claim any responsibility for the security or stability of your project, nor do we guarantee any amount of uptime. 
We **will not** claim responsibility for the safety or security of any secrets in your project.
We reserve the right to **refuse or cease hosting** of your project for any reason, at any time.

Redbrick **will not** host any services that are illegal or violate any applicable laws or regulations of the Republic of Ireland or the European Union.
## Vulnerability Management

You should take steps to ensure that you are always on top of vulnerabilities found in any of the dependencies of your project (e.g. Dependabot on GitHub).

In the event a vulnerability or weakness is identified, you are required address the issue in a timely manner as follows:
- **Medium**: Up to 1 month for resolution
- **High**: Up to 1 week for resolution
- **Critical**: Immediate suspension of service until the vulnerability is addressed and resolved

> Severity levels are determined by the Common Vulnerability Scoring System (CVSS) or official GitHub Dependabot alerts, unless the Redbrick Systems Administrators alter the assigned severity level based on a justified technical reason.

Should these standards not be adhered to, Redbrick reserves the right to terminate hosting services immediately. A formal notification will be provided to the designated Point of Contact.
## Conclusion

By engaging with Redbrick's hosting services, all parties acknowledge and accept these terms and conditions. Further clarification regarding our offerings and limitations can be provided upon request.