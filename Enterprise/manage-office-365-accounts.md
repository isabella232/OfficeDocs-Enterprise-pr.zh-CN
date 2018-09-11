---
title: 用于管理 Office 365 帐户的工具
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 5/3/2018
ms.audience: Admin
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.custom: Adm_O365
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: 98ca5b3f-f720-4d8e-91be-fe656548a25a
description: '了解哪些工具用于管理 Office 365 用户，以及如何您可以使用什么取决于您如何管理用户标识。 '
ms.openlocfilehash: 24a7dd72603b881ea0810d0712900bc78dc34a81
ms.sourcegitcommit: 69d60723e611f3c973a6d6779722aa9da77f647f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2018
ms.locfileid: "22539543"
---
# <a name="tools-to-manage-office-365-accounts"></a><span data-ttu-id="cf07a-103">用于管理 Office 365 帐户的工具</span><span class="sxs-lookup"><span data-stu-id="cf07a-103">Tools to manage Office 365 accounts</span></span>

<span data-ttu-id="cf07a-p101">您可以管理 Office 365 用户几种不同方法，具体取决于您的配置。您可以管理 Office 365 管理中心中，Windows PowerShell 中，您的本地目录中，或在 Azure Active Directory 管理门户中的用户。只要您购买 Office 365 时，可以使用管理中心和 Windows PowerShell，管理帐户。管理云身份时在组织中的每个人都适用于 Office 365 具有单独的用户 ID 和密码。如果您希望与您的内部部署基础结构集成并让用户帐户与 Office 365 同步，您可以使用 Azure Active Directory 连接提供标识的同步和 （可选） 提供密码同步或完整单一登录功能。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p101">You can manage Office 365 users in several different ways, depending on your configuration. You can manage users in the Office 365 admin center, Windows PowerShell, your on-premises directory, or in Azure Active Directory admin portal . As soon as you purchase Office 365, the admin center and Windows PowerShell can be used to manage accounts. When managing cloud identities every person in your organization has a separate user ID and password for Office 365. If you want to integrate with your on-premises infrastructure and have user accounts synchronized with Office 365, you can use Azure Active Directory Connect to provide synchronization of identities and optionally provide password synchronization, or full single sign-on functionality.</span></span>
  
## <a name="plan-for-where-and-how-you-will-manage-your-user-accounts"></a><span data-ttu-id="cf07a-109">规划在何处以及如何管理用户帐户</span><span class="sxs-lookup"><span data-stu-id="cf07a-109">Plan for where and how you will manage your user accounts</span></span>

<span data-ttu-id="cf07a-p102">位置和方式可以管理您的用户帐户取决于您想要使用的 Office 365 的标识模型。两个总体模型是云身份验证和联合身份验证。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p102">Where and how you can manage your user accounts depends on the identity model you want to use for your Office 365. The two overall models are cloud authentication and federated authentication.</span></span>
  
### <a name="cloud-authentication"></a><span data-ttu-id="cf07a-112">云身份验证</span><span class="sxs-lookup"><span data-stu-id="cf07a-112">Cloud authentication</span></span>

- <span data-ttu-id="cf07a-113">[云身份验证](about-office-365-identity.md#cloud-authentication)-创建和管理 Office 365 管理中心中的用户，您也可以使用 Windows PowerShell 或 Azure Active Directory 管理您的用户。</span><span class="sxs-lookup"><span data-stu-id="cf07a-113">[Cloud authentication](about-office-365-identity.md#cloud-authentication) - create and manage users in the Office 365 admin center, you can also use Windows PowerShell, or Azure Active Directory to manage your users.</span></span> 
    
- <span data-ttu-id="cf07a-p103">[与无缝单一登录的密码哈希同步](about-office-365-identity.md)-启用内部部署目录对象在 Azure AD 身份验证的最简单方式。使用密码哈希同步 (PHS)，您可以将您的本地 Active Directory 用户帐户对象与 Office 365 同步和管理用户内部部署。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p103">[Password hash sync with seamless single sign-on](about-office-365-identity.md) - The simplest way to enable authentication for on-premises directory objects in Azure AD. With password hash sync (PHS), you synchronize your on-premises Active Directory user account objects with Office 365 and manage your users on-premises.</span></span> 
    
- <span data-ttu-id="cf07a-116">[传递身份验证与无缝单一登录](about-office-365-identity.md)-提供用于 Azure AD 身份验证服务使用一个或多个本地服务器上运行的软件代理程序验证直接与用户简单密码验证您内部部署 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="cf07a-116">[Pass-through authentication with seamless single sign-on](about-office-365-identity.md) - Provides a simple password validation for Azure AD authentication services using a software agent running on one or more on-premises servers to validate the users directly with your on-premises Active Directory.</span></span> 
    
### <a name="federated-authentication"></a><span data-ttu-id="cf07a-117">联合身份验证</span><span class="sxs-lookup"><span data-stu-id="cf07a-117">Federated authentication</span></span>

- <span data-ttu-id="cf07a-118">[联合身份验证选项](about-office-365-identity.md#federated-authentication-options)-主要用于身份验证要求更复杂的大型企业组织的内部部署目录对象与 Office 365 同步和用户帐户是本地托管。</span><span class="sxs-lookup"><span data-stu-id="cf07a-118">[Federated authentication options](about-office-365-identity.md#federated-authentication-options) - Primarily for large enterprise organizations with more complex authentication requirements, on-premises directory objects are synchronized with Office 365 and users accounts are managed on-premises.</span></span> 
    
- <span data-ttu-id="cf07a-119">[第三方身份验证和标识提供程序](about-office-365-identity.md)的内部部署目录对象可能同步到 Office 365 和云资源访问主要第三方身份提供程序 (IdP) 进行管理。</span><span class="sxs-lookup"><span data-stu-id="cf07a-119">[Third-party authentication and identity providers](about-office-365-identity.md) - On-premises directory objects may be synchronized to Office 365 and cloud resource access is primarily managed by a third-party identity provider (IdP).</span></span> 
    
## <a name="managing-accounts"></a><span data-ttu-id="cf07a-120">管理帐户</span><span class="sxs-lookup"><span data-stu-id="cf07a-120">Managing Accounts</span></span>

<span data-ttu-id="cf07a-121">决定您的组织将创建和管理帐户的方式时, 考虑以下事项：</span><span class="sxs-lookup"><span data-stu-id="cf07a-121">When deciding which way your organization will create and manage accounts, consider the following:</span></span>
  
- <span data-ttu-id="cf07a-122">需要连接 Office 365 和内部部署目录之间标识您的本地环境中的服务器上安装目录同步软件。</span><span class="sxs-lookup"><span data-stu-id="cf07a-122">The directory synchronization software needs to be installed on servers within your on-premises environment to connect the identities between Office 365 and your on-premises directory.</span></span>
    
- <span data-ttu-id="cf07a-p104">任何目录同步选项，包括 SSO 选项要求您的本地目录属性符合标准。在您的目录中使用哪些属性和哪些清理 （如果有） 所需的详细说明如何[准备通过目录同步到 Office 365 设置用户](prepare-for-directory-synchronization.md)所述。有关如何使用 IdFix 自动化目录清理的说明，请参阅[安装和运行 Office 365 IdFix 工具](install-and-run-idfix.md)。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p104">Any directory synchronization option, including SSO options, requires your on-premises directory attributes meet standards. The specifics of what attributes are used in your directory and what cleanup (if any) is needed are described in [Prepare to provision users through directory synchronization to Office 365](prepare-for-directory-synchronization.md). See [Install and run the Office 365 IdFix tool](install-and-run-idfix.md) for instruction on how to use IdFix to automate directory cleanup.</span></span> 
    
- <span data-ttu-id="cf07a-126">规划如何要创建 Office 365 帐户。</span><span class="sxs-lookup"><span data-stu-id="cf07a-126">Plan how you are going to create Office 365 accounts.</span></span>
    
    <span data-ttu-id="cf07a-127">下表列出了不同的帐户管理工具。</span><span class="sxs-lookup"><span data-stu-id="cf07a-127">The following table lists the different account management tools.</span></span>
    
|<span data-ttu-id="cf07a-128">**选项**</span><span class="sxs-lookup"><span data-stu-id="cf07a-128">**Option**</span></span>|<span data-ttu-id="cf07a-129">**备注**</span><span class="sxs-lookup"><span data-stu-id="cf07a-129">**Notes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf07a-130">Office 365 管理中心</span><span class="sxs-lookup"><span data-stu-id="cf07a-130">Office 365 admin center</span></span>  <br/> |[<span data-ttu-id="cf07a-131">将用户添加单独或批量到 Office 365-管理帮助</span><span class="sxs-lookup"><span data-stu-id="cf07a-131">Add users individually or in bulk to Office 365 - Admin Help</span></span>](https://support.office.com/article/1970f7d6-03b5-442f-b385-5880b9c256ec) <br/>  <span data-ttu-id="cf07a-132">提供简单的 web 界面来添加和更改用户帐户。</span><span class="sxs-lookup"><span data-stu-id="cf07a-132">Provides a simple web interface to add and change user accounts.</span></span>  <br/>  <span data-ttu-id="cf07a-133">不能用来更改用户，如果启用了目录同步 （可以设置位置和许可证分配）。</span><span class="sxs-lookup"><span data-stu-id="cf07a-133">Can't be used to change users if directory synchronization is enabled (location and license assignment can be set).</span></span>  <br/>  <span data-ttu-id="cf07a-134">不能与 SSO 选项一起使用。</span><span class="sxs-lookup"><span data-stu-id="cf07a-134">Can't be used with SSO options.</span></span>  <br/> |
|<span data-ttu-id="cf07a-135">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cf07a-135">Windows PowerShell</span></span>  <br/> |[<span data-ttu-id="cf07a-136">使用 Windows PowerShell 管理 Office 365</span><span class="sxs-lookup"><span data-stu-id="cf07a-136">Manage Office 365 with Windows PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=698471) <br/>  <span data-ttu-id="cf07a-137">可以使用 Windows PowerShell 脚本批量用户中添加用户。</span><span class="sxs-lookup"><span data-stu-id="cf07a-137">Allows you to add users in bulk users by using a Windows PowerShell script.</span></span>  <br/>  <span data-ttu-id="cf07a-138">可用于位置和许可证分配到帐户，而不考虑如何创建帐户。</span><span class="sxs-lookup"><span data-stu-id="cf07a-138">Can be used to assign location and licenses to accounts, regardless of how the accounts are created.</span></span>  <br/> |
|<span data-ttu-id="cf07a-139">批量导入</span><span class="sxs-lookup"><span data-stu-id="cf07a-139">Bulk import</span></span>  <br/> |[<span data-ttu-id="cf07a-140">同时向 Office 365 添加多个用户 - 管理员帮助</span><span class="sxs-lookup"><span data-stu-id="cf07a-140">Add several users at the same time to Office 365 - Admin Help</span></span>](add-several-users-at-the-same-time.md) <br/>  <span data-ttu-id="cf07a-141">允许您导入 CSV 文件的用户组添加到 Office 365。</span><span class="sxs-lookup"><span data-stu-id="cf07a-141">Allows you to import a CSV file to add a group of users to Office 365.</span></span>  <br/>  <span data-ttu-id="cf07a-142">不能与 SSO 选项一起使用。</span><span class="sxs-lookup"><span data-stu-id="cf07a-142">Can't be used with SSO options.</span></span>  <br/> |
|<span data-ttu-id="cf07a-143">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cf07a-143">Azure Active Directory</span></span>  <br/> |<span data-ttu-id="cf07a-p105">使用 Office 365 订阅获取免费版本的 Azure Active Directory。您可以执行类似自助服务密码重置的云用户和自定义的登录和访问面板的页面使用的免费版本的功能。若要获得增强的功能，您可以升级到的基本版本，或者 premium edition。有关受支持的功能的列表，请参阅[Azure Active Directory 版本](https://go.microsoft.com/fwlink/p/?LinkId=698465)。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p105">You get a free edition of Azure Active Directory with your Office 365 subscription. You can perform functions like self-service password reset for cloud users, and customization of the Sign-in and Access Panel pages by using the free edition. To get enhanced functionality, you can upgrade to either the basic edition, or the premium edition. See [Azure Active Directory editions](https://go.microsoft.com/fwlink/p/?LinkId=698465) for the list of supported features.  </span></span><br/> |
|<span data-ttu-id="cf07a-148">目录同步</span><span class="sxs-lookup"><span data-stu-id="cf07a-148">Directory synchronization</span></span>  <br/> |[<span data-ttu-id="cf07a-149">将与 Azure Active Directory 集成的本地标识</span><span class="sxs-lookup"><span data-stu-id="cf07a-149">Integrating your on-premises identities with Azure Active Directory</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=624168) <br/>  <span data-ttu-id="cf07a-150">使用或不密码同步的目录同步，使用[使用 express 设置 Azure AD 连接](https://go.microsoft.com/fwlink/p/?LinkID=698537)。</span><span class="sxs-lookup"><span data-stu-id="cf07a-150">For directory synchronization with or without password synchronization, use [Azure AD Connect with express settings](https://go.microsoft.com/fwlink/p/?LinkID=698537).</span></span>  <br/>  <span data-ttu-id="cf07a-151">对于多个林和 SSO 选项，使用[自定义安装的 Azure AD 连接](https://go.microsoft.com/fwlink/p/?LinkId=698430)。</span><span class="sxs-lookup"><span data-stu-id="cf07a-151">For multiple forests and SSO options, use [Custom Installation of Azure AD Connect](https://go.microsoft.com/fwlink/p/?LinkId=698430).</span></span>  <br/>  <span data-ttu-id="cf07a-152">提供启用 SSO 所需的基础结构。</span><span class="sxs-lookup"><span data-stu-id="cf07a-152">Provides the infrastructure that's necessary to enable SSO.</span></span>  <br/>  <span data-ttu-id="cf07a-153">所需的许多混合方案：</span><span class="sxs-lookup"><span data-stu-id="cf07a-153">Required for many hybrid scenarios:</span></span>  <br/>  <span data-ttu-id="cf07a-154">暂存迁移</span><span class="sxs-lookup"><span data-stu-id="cf07a-154">Staged migration</span></span>  <br/>  <span data-ttu-id="cf07a-155">混合 Exchange</span><span class="sxs-lookup"><span data-stu-id="cf07a-155">Hybrid Exchange</span></span>  <br/>  <span data-ttu-id="cf07a-156">从内部部署目录同步安全组和已启用邮件组。</span><span class="sxs-lookup"><span data-stu-id="cf07a-156">Synchronizes security and mail-enabled groups from your on-premises directory.</span></span>  <br/> |
   
- <span data-ttu-id="cf07a-p106">无论您打算如何添加到 Office 365 的用户帐户，您需要管理多个帐户功能，如分配许可证，指定位置，等等。这些功能可以管理长期从 Office 365 管理中心，或者您还可以[创建与 Office 365 PowerShell 中的用户帐户](https://go.microsoft.com/fwlink/p/?LinkId=717083)。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p106">Regardless of how you intend to add the user accounts to Office 365, you need to manage several account features, such as assigning licenses, specifying location, and so on. These features can be managed long-term from the Office 365 admin center or you can also [create user accounts with Office 365 PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=717083).</span></span>
    
    <span data-ttu-id="cf07a-p107">如果您选择添加和管理您通过 Office 365 管理中心内的所有用户，您将指定的位置，并作为创建的 Office 365 帐户同时分配许可证。因此，不多规划，则需要。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p107">If you choose to add and manage all your users through the Office 365 admin center, you will specify the location and assign licenses at the same time as creating the Office 365 account. As a result, not much planning is required.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="cf07a-p108">Office 365 中创建帐户没有将许可证分配 (to SharePoint Online，例如) 意味着帐户所有者可以查看 Office 365 门户但不是能访问任何内贵公司的订阅的服务。位置和许可证分配后，该帐户将被复制到的服务或您为其分配的服务。用户可以登录到其帐户，并使用分配给它们的服务。</span><span class="sxs-lookup"><span data-stu-id="cf07a-p108">Creating accounts in Office 365 without assigning a license (to SharePoint Online, for example) means that the account owner can view the Office 365 portal but can't access any of the services within your company's subscription. After you assign a location and the license, the account is replicated to the service or services that you assigned. The user can sign in to their account and use the services that you assigned to them.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="cf07a-164">后续步骤</span><span class="sxs-lookup"><span data-stu-id="cf07a-164">Next steps</span></span>

[<span data-ttu-id="cf07a-165">Office 365 与内部部署环境的集成</span><span class="sxs-lookup"><span data-stu-id="cf07a-165">Office 365 integration with on-premises environments</span></span>](office-365-integration.md)
  
## <a name="see-also"></a><span data-ttu-id="cf07a-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf07a-166">See Also</span></span>

[<span data-ttu-id="cf07a-167">管理 Office 365 中的用户帐户</span><span class="sxs-lookup"><span data-stu-id="cf07a-167">Manage user accounts in Office 365</span></span>](https://support.office.com/article/3204162b-0b6c-4838-8a11-394b9bfd31de.aspx)
  
