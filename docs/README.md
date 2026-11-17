\# Zero Trust IAM Homelab Documentation



\## Purpose



This lab documents my hands-on implementation of identity and access management concepts in a Microsoft cloud environment.



The lab is designed to explore Zero Trust principles through practical identity-focused configuration and testing.



\## Identity and Access Configuration



\### Security Group



Created the cloud-based security group SG-IAM-Lab-Users with assigned membership to provide a controlled grouping for homelab user identities.



\### Test User Identity



Created Lab User 01 as a standard member identity and assigned the account to SG-IAM-Lab-Users. No administrative role was assigned, keeping the test identity separate from the privileged administrative account.



\### Verification



Verified that Lab User 01 appears as an assigned member of SG-IAM-Lab-Users in Microsoft Entra ID after provisioning.



\### Baseline Security



Verified that Microsoft Entra Security Defaults are enabled for the tenant, providing baseline identity protections while the homelab uses the Microsoft Entra ID Free tier.



\### Authentication Test



Completed an interactive sign-in as Lab User 01, registered Microsoft Authenticator when prompted, and verified the successful multifactor authentication event in Microsoft Entra sign-in logs. The event showed that the MFA requirement was satisfied by an existing claim in the authentication token.



\### Application Access



Added the Microsoft Entra SAML Toolkit enterprise application and directly assigned Lab User 01 with application access. Group-based application assignment was unavailable under the Microsoft Entra ID Free tier, so direct user assignment was used. Verified the assignment from the user perspective by confirming the application appeared in the Lab User 01 My Apps portal.



\### SAML Single Sign-On



Configured and validated SAML 2.0 single sign-on between Microsoft Entra ID and the Microsoft Entra SAML Toolkit. Configured the Identity Provider and Service Provider relationship using the Entity ID, SP-initiated sign-on URL, Assertion Consumer Service (ACS) URL, Microsoft Entra login and logout endpoints, and the SAML signing certificate. Created a matching service-provider test identity and successfully validated SP-initiated SSO as Lab User 01 without re-entering the application's local credentials.

