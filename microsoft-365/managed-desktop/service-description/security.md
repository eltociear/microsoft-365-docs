---
title: Security in Microsoft Managed Desktop 
description:  
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.date: 09/24/2018
---

# Security in Microsoft Managed Desktop

<!--Security, also Onboarding doc: data handling/store, privileged account access -->

Microsoft Managed Desktop uses several Microsoft technologies to help secure managed devices and data. Specifically: 


- [Device security](#device-security) – security and protection on Microsoft Managed Desktop devices
- [Identity and Access Management](#identity-and-access-management) – managing secure use of devices through Azure Active Directory identity services
- [Network security](#network-security) – VPN information and Microsoft Managed Desktop recommended solution and settings
- [Information security](#information-security) – optional available services to further protect sensitive information 




## Device security

Microsoft Managed Desktop ensures all managed devices are secured and protected, and detects threats as early as possible using the following services:

Service | Description
--- | ---
Antivirus |	Microsoft Defender AV is installed and configured<br>Microsoft Defender AV definitions are up to date
Full Volume Encryption |	Windows BitLocker is the volume encryption solution for Microsoft Managed Desktop devices.<br><br>Once an organization is onboarded into the service, devices will be encrypted using Windows BitLocker with built-in Trust Platform Module (TPM) to prevent unauthorized access to local data when the device is in sleep mode, or off. 
Monitoring |	Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) is used for security threat monitoring across all Microsoft Managed Desktop devices. Microsoft Defender ATP allows enterprise customers to detect, investigate, and respond to advanced threats in their corporate network. For more information, see [Microsoft Defender Advanced Threat Protection.](https://docs.microsoft.com/windows/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) 
Operating system updates |	Microsoft Managed Desktop devices are always secured with the latest security updates.
Secure Device Configuration |	Microsoft Managed Desktop implements the Microsoft Security Baseline. For more information, see [Windows security baselines.](https://docs.microsoft.com/windows/security/threat-protection/windows-security-baselines)



## Identity and access management

Identity and access management protects corporate assets and business-critical data. Microsoft Managed Desktop configures devices to ensure secure use with Azure Active Directory (Azure AD) managed identities. It is the customer's responsibility to maintain accurate information in their Azure AD tenant. 

Service | Description
--- | ---
Biometric Authentication |	Windows Hello allows users to login using their face or a PIN, making passwords harder to forget or steal. Customers are responsible for implementing the necessary pre-requisites for their on-premises Active Directory for use of this service in a hybrid configuration. For more information, see [Windows Hello.](https://docs.microsoft.com/windows-hardware/design/device-experiences/windows-hello) 
Standard user permission |	To protect the system and make it more secure, the user will be assigned Standard User Permissions. This is assigned as part of the Windows Autopilot out-of-box experience.



## Network security

Customers are responsible for network security. 

Service | Description
--- | ---
VPN | Customers own their VPN infrastructure, to ensure limited corporate resources can be exposed outside the intranet.<br><br>Minimum requirement: Microsoft Managed Desktop requires a Windows 10 compatible and supported VPN solution. If your organization needs a VPN solution, it needs to support Windows 10 and be packaged and deployable through Intune. Contact your software publisher for more information.<br><br>Recommendation:<br>- Microsoft recommends a modern VPN solution that could be easily deployed through Intune to push VPN profiles. This provides an always-on, seamless, reliable, and secure way to access corporate network. For more information, see [[VPN settings in Intune]](https://docs.microsoft.com/intune/vpn-settings-configure).<br>- Thick VPN clients, or legacy VPN clients, are not recommended by Microsoft while using Microsoft Managed Desktop as it can impact the end-user environment.<br>- Microsoft recommends that the outgoing web traffic goes directly to Internet without going through the VPN to avoid any performance issues.<br>- Ideally, Microsoft recommends the use of Azure Active Directory App Proxy instead of a VPN.


## Information security

Customers may configure these optional services to help protect corporate high-value assets. 

Service | Description
--- | ---
Data recovery  | Information stored in key folders on the device is backed up to OneDrive for Business. Microsoft Managed Desktop is not responsible for data that isn’t synchronized with OneDrive for Business. 
Windows Information Protection |	For companies that require high levels of information security, we recommend [Windows Information Protection](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/protect-enterprise-data-using-wip) and [Azure Information Protection.](https://www.microsoft.com/cloud-platform/azure-information-protection). 

