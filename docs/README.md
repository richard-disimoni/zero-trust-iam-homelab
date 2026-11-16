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

