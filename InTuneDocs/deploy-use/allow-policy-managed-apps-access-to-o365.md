---
# required metadata

title: App based conditional access to 0365 | Microsoft Docs
description: Understand the concepts of how MAM CA can help with controlling what apps have access to O365 services.
keywords:
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 10/25/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: bd6bee60-5e39-42c8-a2e9-f5865ac3573f

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: chrisgre
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Allow only mobile apps that support Intune MAM policies to access Office 365 services
[Intune mobile app management (MAM) policies](protect-apps-and-data-with-microsoft-intune.md) help protect your company data on devices that are enrolled for management in Intune. You can also use MAM policies on **employee owned devices that are not enrolled for management in Intune**.  In this case, even though you don't manage the device, you still need to make sure that your company data and resources is protected. Using conditional access for MAM (MAM CA), you can create a policy that allows only mobile apps that support Intune MAM policies to access O365 services like Exchange Online.

For example, by only allowing the **Microsoft Outlook app** to access Exchange Online, you can **block the built-in mail apps on iOS and Android**, which don't have the data protection from Intune MAM policies to get email from **Exchange Online**.

The diagram below illustrates the flow used by MAM CA policies to determine when to allow or block access:
![Diagram that shows the various criteria included to determine whether to allow or block access ](../media/mam-ca-decision-flow_simple.png).

Description of the abbreviations used in the diagrams:
* **CP**: Company Portal app
* **AA**: Azure Authenticator app
* **AAD**: Azure Active Directory
* **EAS**: Exchange Active Sync

## Prerequisites
**Before** you can configure MAM CA policy you must have an **Enterprise Mobility + Security or an Azure Active Directory premium subscription**, and the users must be licensed for EMS or Azure AD. For more details, see the [Enterprise Mobility pricing page](https://www.microsoft.com/en-us/cloud-platform/enterprise-mobility-pricing) or the [Azure Active Directory pricing page](https://azure.microsoft.com/en-us/pricing/details/active-directory/).


## Supported apps
**Exchange Online**:
**Microsoft Outlook** for Android and iOS.

To learn about the user experience with an app that has MAM CA policies, see [What to expect when using an app with MAM CA](use-apps-with-mam-ca.md).


## Next steps
[Create an Exchange Online Policy for MAM apps](mam-ca-for-exchange-online.md)

[Block apps that do not have modern authentication](block-apps-with-no-modern-authentication.md)

### See also

[Protect app data with MAM policies](protect-app-data-using-mobile-app-management-policies-with-microsoft-intune.md)
