---
title: Office 365 仅限云身份标识
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- O365p_AddUsersWithDirSync
- O365M_AddUsersWithDirSync
- O365E_HRCSetupAADConnectAboutLM617031
- O365E_AddUsersWithDirSync
ms.service: o365-administration
localization_priority: Normal
ms.custom: Adm_O365
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOP150
- MOE150
- MBS150
ms.assetid: 01920974-9e6f-4331-a370-13aea4e82b3e
description: 介绍如何在 Office 365 订阅使用仅限云的标识时创建用户和组。
ms.openlocfilehash: 7a2aaf7705378da3cbd91b415f07d10b6e039293
ms.sourcegitcommit: 36e760407a1f4b18bc108134628ed9a8d3e35a8a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/17/2019
ms.locfileid: "34164607"
---
# <a name="office-365-cloud-only-identities"></a><span data-ttu-id="4c1db-103">Office 365 仅限云身份标识</span><span class="sxs-lookup"><span data-stu-id="4c1db-103">Office 365 cloud-only identities</span></span>

<span data-ttu-id="4c1db-104">对于仅限云的标识, 所有用户、组和联系人都存储在 Office 365 订阅的 Azure Active Directory (Azure AD) 租户中。</span><span class="sxs-lookup"><span data-stu-id="4c1db-104">With cloud-only identity, all your users, groups, and contacts are stored in the Azure Active Directory (Azure AD) tenant of your Office 365 subscription.</span></span> <span data-ttu-id="4c1db-105">下面是仅限云身份的基本组件。</span><span class="sxs-lookup"><span data-stu-id="4c1db-105">Here are the basic components of cloud-only identity.</span></span>
 
![](./media/about-office-365-identity/cloud-only-identity.png)

<span data-ttu-id="4c1db-106">可以通过多种方式对组织中的用户及其用户帐户进行分类。</span><span class="sxs-lookup"><span data-stu-id="4c1db-106">Users and their user accounts in organizations can be categorized in a number of ways.</span></span> <span data-ttu-id="4c1db-107">例如, 一些是员工, 且具有永久状态。</span><span class="sxs-lookup"><span data-stu-id="4c1db-107">For example, some are employees and have a permanent status.</span></span> <span data-ttu-id="4c1db-108">有些是具有临时状态的供应商、承包商或合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="4c1db-108">Some are vendors, contractors, or partners that have a temporary status.</span></span> <span data-ttu-id="4c1db-109">有些外部用户没有用户帐户, 但仍必须被授予对特定服务和资源的访问权限, 以支持交互和协作。</span><span class="sxs-lookup"><span data-stu-id="4c1db-109">Some are external users that have no user accounts but must still be granted access to specific services and resources to support interaction and collaboration.</span></span> <span data-ttu-id="4c1db-110">例如：</span><span class="sxs-lookup"><span data-stu-id="4c1db-110">For example:</span></span>

- <span data-ttu-id="4c1db-111">租户帐户表示组织中许可访问云服务的用户。</span><span class="sxs-lookup"><span data-stu-id="4c1db-111">Tenant accounts represent users within your organization that you license for cloud services</span></span>

- <span data-ttu-id="4c1db-112">企业到企业 (B2B) 帐户表示您的组织外部的用户, 您邀请参与协作的用户可以向您的组织中的用户类型进行分组。</span><span class="sxs-lookup"><span data-stu-id="4c1db-112">Business to Business (B2B) accounts represent users outside your organization that you invite to participate in collaboration Take stock of the types of users to your organization.</span></span> <span data-ttu-id="4c1db-113">分组是什么？</span><span class="sxs-lookup"><span data-stu-id="4c1db-113">What are the groupings?</span></span> <span data-ttu-id="4c1db-114">例如, 您可以将用户按高级功能或目标分组到您的组织。</span><span class="sxs-lookup"><span data-stu-id="4c1db-114">For example, you can group users by high-level function or purpose to your organization.</span></span>

<span data-ttu-id="4c1db-p104">此外，可以将某些云服务与组织外部没有任何用户帐户的用户共享，而且你还需要标识这些用户组。</span><span class="sxs-lookup"><span data-stu-id="4c1db-p104">Additionally, some cloud services can be shared with users outside your organization without any user accounts. You'll need to identify these groups of users as well.</span></span>

<span data-ttu-id="4c1db-117">您可以使用 Azure AD 中的组来实现多种目的, 从而简化云环境的管理。</span><span class="sxs-lookup"><span data-stu-id="4c1db-117">You can use groups in Azure AD for several purposes that simplify management of your cloud environment.</span></span> <span data-ttu-id="4c1db-118">例如, 使用 Azure AD 组, 您可以执行以下操作:</span><span class="sxs-lookup"><span data-stu-id="4c1db-118">For example, with Azure AD groups, you can:</span></span>

- <span data-ttu-id="4c1db-119">使用基于组的许可将 Office 365 的许可证在添加后立即自动分配给用户帐户。</span><span class="sxs-lookup"><span data-stu-id="4c1db-119">Use group-based licensing to assign licenses for Office 365 to your user accounts automatically as soon as they are added.</span></span>
- <span data-ttu-id="4c1db-120">根据用户帐户属性（如部门）将用户帐户动态添加到特定组。</span><span class="sxs-lookup"><span data-stu-id="4c1db-120">Add user accounts to specific groups dynamically based on user account attributes, such as department.</span></span>
- <span data-ttu-id="4c1db-121">自动预配软件即服务 (SaaS) 应用程序的用户，并通过多重身份验证和其他条件访问规则来保护对这些应用程序的访问。</span><span class="sxs-lookup"><span data-stu-id="4c1db-121">Automatically provision users for Software as a Service (SaaS) applications and to protect access to those applications with multi-factor authentication and other conditional access rules.</span></span>
- <span data-ttu-id="4c1db-122">为 SharePoint Online 团队网站设置权限和访问权限级别。</span><span class="sxs-lookup"><span data-stu-id="4c1db-122">Provision permissions and levels of access for SharePoint Online team sites.</span></span>

<span data-ttu-id="4c1db-123">您可以使用以下内容创建新***用户***:</span><span class="sxs-lookup"><span data-stu-id="4c1db-123">You can create new ***users*** with:</span></span>

- [<span data-ttu-id="4c1db-124">Microsoft 365 管理中心</span><span class="sxs-lookup"><span data-stu-id="4c1db-124">The Microsoft 365 admin center</span></span>](https://docs.microsoft.com/office365/admin/add-users/add-users)
- [<span data-ttu-id="4c1db-125">Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c1db-125">Office 365 PowerShell</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/create-user-accounts-with-office-365-powershell)

<span data-ttu-id="4c1db-126">您可以使用以下内容创建新***组***:</span><span class="sxs-lookup"><span data-stu-id="4c1db-126">You can create new ***groups*** with:</span></span>

- [<span data-ttu-id="4c1db-127">Microsoft 365 管理中心</span><span class="sxs-lookup"><span data-stu-id="4c1db-127">The Microsoft 365 admin center</span></span>](https://docs.microsoft.com/office365/admin/create-groups/create-groups)
- [<span data-ttu-id="4c1db-128">Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c1db-128">Office 365 PowerShell</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-groups-with-powershell)


## <a name="next-step-for-cloud-only-identities"></a><span data-ttu-id="4c1db-129">仅限云标识的下一步</span><span class="sxs-lookup"><span data-stu-id="4c1db-129">Next step for cloud-only identities</span></span>

[<span data-ttu-id="4c1db-130">向用户帐户分配许可证</span><span class="sxs-lookup"><span data-stu-id="4c1db-130">Assign licenses to user accounts</span></span>](assign-licenses-to-user-accounts.md)