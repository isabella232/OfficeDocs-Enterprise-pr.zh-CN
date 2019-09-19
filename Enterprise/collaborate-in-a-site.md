---
title: 在网站中与来宾协作
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: sharepoint-online
localization_priority: Normal
description: 了解如何在 SharePoint 网站中与来宾进行协作。
ms.openlocfilehash: 4b68b50fec4322f12c24969bdd71e7d9c0fda245
ms.sourcegitcommit: d388c76d25ca67f240db97f7bfc90f0991b0e7f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2019
ms.locfileid: "37017310"
---
# <a name="collaborate-with-guests-in-a-site"></a><span data-ttu-id="518f1-103">在网站中与来宾协作</span><span class="sxs-lookup"><span data-stu-id="518f1-103">Collaborate with guests in a site</span></span>

<span data-ttu-id="518f1-104">如果需要在文档、数据和列表之间与来宾进行协作，则可以使用 SharePoint 网站。</span><span class="sxs-lookup"><span data-stu-id="518f1-104">If you need to collaborate with guests across documents, data, and lists, you can use a SharePoint site.</span></span> <span data-ttu-id="518f1-105">新式 SharePoint 网站连接到可管理网站成员身份的 Office 365 组，并提供其他协作工具（如共享邮箱和日历）。</span><span class="sxs-lookup"><span data-stu-id="518f1-105">Modern SharePoint sites are connected to Office 365 Groups which can manage the site membership and provide additional collaboration tools such as a shared mailbox and calendar.</span></span>

<span data-ttu-id="518f1-106">在本文中，我们将逐步完成为与来宾协作设置 SharePoint 网站所必需的 Microsoft 365 配置步骤。</span><span class="sxs-lookup"><span data-stu-id="518f1-106">In this article, we'll walk through the Microsoft 365 configuration steps necessary to set up a SharePoint site for collaboration with guests.</span></span>

## <a name="azure-organizational-relationships-settings"></a><span data-ttu-id="518f1-107">Azure 组织关系设置</span><span class="sxs-lookup"><span data-stu-id="518f1-107">Azure Organizational relationships settings</span></span>

<span data-ttu-id="518f1-108">Microsoft 365 中的共享受 Azure Active Directory 中的组织关系设置的最高级别的管辖。</span><span class="sxs-lookup"><span data-stu-id="518f1-108">Sharing in Microsoft 365 is governed at its highest level by the organizational relationships settings in Azure Active Directory.</span></span> <span data-ttu-id="518f1-109">如果在 Azure AD 中禁用或限制来宾共享，这将替代您在 Microsoft 365 中配置的任何共享设置。</span><span class="sxs-lookup"><span data-stu-id="518f1-109">If guest sharing is disabled or restricted in Azure AD, this will override any sharing settings that you configure in Microsoft 365.</span></span>

<span data-ttu-id="518f1-110">检查组织关系设置以确保不会阻止与来宾共享。</span><span class="sxs-lookup"><span data-stu-id="518f1-110">Check the organizational relationships settings to ensure that sharing with guests is not blocked.</span></span>

![Azure Active Directory 组织关系设置页面的屏幕截图](media/azure-ad-organizational-relationships-settings.png)

<span data-ttu-id="518f1-112">设置组织关系设置</span><span class="sxs-lookup"><span data-stu-id="518f1-112">To set organizational relationship settings</span></span>

1. <span data-ttu-id="518f1-113">登录到 Microsoft Azure [https://portal.azure.com](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="518f1-113">Log in to Microsoft Azure at [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="518f1-114">在左侧导航中，单击 " **Azure Active Directory**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-114">In the left navigation, click **Azure Active Directory**.</span></span>
3. <span data-ttu-id="518f1-115">在 "**概述**" 窗格中，单击 "**组织关系**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-115">In the **Overview** pane, click **Organizational relationships**.</span></span>
4. <span data-ttu-id="518f1-116">在 "**组织关系**" 窗格中，单击 "**设置**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-116">In the **Organizational relationships** pane, click **Settings**.</span></span>
5. <span data-ttu-id="518f1-117">确保**来宾邀请者角色中的管理员和用户可以邀请**和**成员**都可以邀请都设置为 **"是"**。</span><span class="sxs-lookup"><span data-stu-id="518f1-117">Ensure that **Admins and users in the guest inviter role can invite** and **Members can invite** are both set to **Yes**.</span></span>
6. <span data-ttu-id="518f1-118">如果进行了更改，请单击 "**保存**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-118">If you made changes, click **Save**.</span></span>

<span data-ttu-id="518f1-119">请注意 "**协作限制**" 部分中的设置。</span><span class="sxs-lookup"><span data-stu-id="518f1-119">Note the settings in the **Collaboration restrictions** section.</span></span> <span data-ttu-id="518f1-120">确保不会阻止您要与之进行协作的来宾域。</span><span class="sxs-lookup"><span data-stu-id="518f1-120">Make sure that the domains of the guests that you want to collaborate with aren't blocked.</span></span>

## <a name="office-365-groups-guest-settings"></a><span data-ttu-id="518f1-121">Office 365 组来宾设置</span><span class="sxs-lookup"><span data-stu-id="518f1-121">Office 365 Groups guest settings</span></span>

<span data-ttu-id="518f1-122">新式 SharePoint 网站使用 Office 365 组来控制网站访问。</span><span class="sxs-lookup"><span data-stu-id="518f1-122">Modern SharePoint sites use Office 365 Groups to control site access.</span></span> <span data-ttu-id="518f1-123">必须打开 Office 365 组来宾设置，才能使 SharePoint 网站中的来宾访问能够正常工作。</span><span class="sxs-lookup"><span data-stu-id="518f1-123">The Office 365 Groups guest settings must be turned on in order for guest access in SharePoint sites to work.</span></span>

![Microsoft 365 管理中心中的 Office 365 组来宾设置的屏幕截图](media/office-365-groups-guest-settings.png)

<span data-ttu-id="518f1-125">设置 Office 365 组来宾设置</span><span class="sxs-lookup"><span data-stu-id="518f1-125">To set Office 365 Groups guest settings</span></span>

1. <span data-ttu-id="518f1-126">在 Microsoft 365 管理中心的左侧导航栏中，展开 "**设置**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-126">In the Microsoft 365 admin center, in the left navigation, expand **Settings**.</span></span>
2. <span data-ttu-id="518f1-127">单击 "**服务" & 外接程序**。</span><span class="sxs-lookup"><span data-stu-id="518f1-127">Click **Services & add-ins**.</span></span>
3. <span data-ttu-id="518f1-128">在列表中，单击 " **Office 365 组**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-128">In the list, click **Office 365 Groups**.</span></span>
4. <span data-ttu-id="518f1-129">确保将**组织外部的成员访问组内容**和**允许组所有者将组织外部的人员添加到组**复选框均选中。</span><span class="sxs-lookup"><span data-stu-id="518f1-129">Ensure that the **Let group members outside your organization access group content** and **Let group owners add people outside your organization to groups** check boxes are both checked.</span></span>
5. <span data-ttu-id="518f1-130">如果进行了更改，请单击 "**保存更改**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-130">If you made changes, click **Save changes**.</span></span>


## <a name="sharepoint-organization-level-sharing-settings"></a><span data-ttu-id="518f1-131">SharePoint 组织级别的共享设置</span><span class="sxs-lookup"><span data-stu-id="518f1-131">SharePoint organization level sharing settings</span></span>

<span data-ttu-id="518f1-132">为使来宾能够访问 SharePoint 网站，SharePoint 组织级别的共享设置必须允许与来宾共享。</span><span class="sxs-lookup"><span data-stu-id="518f1-132">In order for guests to have access to SharePoint sites, the SharePoint organization-level sharing settings must allow for sharing with guests.</span></span>

<span data-ttu-id="518f1-133">组织级别设置确定了哪些设置可用于单个网站。</span><span class="sxs-lookup"><span data-stu-id="518f1-133">The organization-level settings determine what settings are available for individual sites.</span></span> <span data-ttu-id="518f1-134">网站设置不能比组织级别设置更具有更好的许可。</span><span class="sxs-lookup"><span data-stu-id="518f1-134">Site settings cannot be more permissive than the organization-level settings.</span></span>

<span data-ttu-id="518f1-135">如果要允许与匿名用户共享文件和文件夹，请选择 "**任何人**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-135">If you want to allow file and folder sharing with anonymous users, choose **Anyone**.</span></span> <span data-ttu-id="518f1-136">如果要确保所有来宾都必须进行身份验证，请选择 "**新建" 和 "现有来宾**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-136">If you want to ensure that all guests have to authenticate, choose **New and existing guests**.</span></span> <span data-ttu-id="518f1-137">选择组织中的任何网站将需要的 "最高" 设置。</span><span class="sxs-lookup"><span data-stu-id="518f1-137">Choose the most permissive setting that will be needed by any site in your organization.</span></span>

![SharePoint 组织级共享设置的屏幕截图](media/sharepoint-organization-external-sharing-controls.png)


<span data-ttu-id="518f1-139">设置 SharePoint 组织级别的共享设置</span><span class="sxs-lookup"><span data-stu-id="518f1-139">To set SharePoint organization level sharing settings</span></span>

1. <span data-ttu-id="518f1-140">在 Microsoft 365 管理中心的左侧导航栏中，在 "**管理中心**" 下，单击 " **SharePoint**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-140">In the Microsoft 365 admin center, in the left navigation, under **Admin centers**, click **SharePoint**.</span></span>
2. <span data-ttu-id="518f1-141">在 SharePoint 管理中心的左侧导航栏中，单击 "**共享**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-141">In the SharePoint admin center, in the left navigation, click **Sharing**.</span></span>
3. <span data-ttu-id="518f1-142">确保将 SharePoint 的 "外部共享" 设置为 "**任何人**" 或 "**新的和现有的来宾**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-142">Ensure that external sharing for SharePoint is set to **Anyone** or **New and existing guests**.</span></span>
4. <span data-ttu-id="518f1-143">如果进行了更改，请单击 "**保存**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-143">If you made changes, click **Save**.</span></span>

## <a name="create-a-site"></a><span data-ttu-id="518f1-144">创建网站</span><span class="sxs-lookup"><span data-stu-id="518f1-144">Create a site</span></span>

<span data-ttu-id="518f1-145">下一步是创建您计划用于与来宾协作的网站。</span><span class="sxs-lookup"><span data-stu-id="518f1-145">The next step is to create the site that you plan to use for collaborating with guests.</span></span>

<span data-ttu-id="518f1-146">创建网站</span><span class="sxs-lookup"><span data-stu-id="518f1-146">To create a site</span></span>
1. <span data-ttu-id="518f1-147">在 SharePoint 管理中心中的 "**网站**" 下，单击 "**活动网站**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-147">In the SharePoint admin center, under **Sites**, click **Active sites**.</span></span>
2. <span data-ttu-id="518f1-148">单击“**创建**”。 </span><span class="sxs-lookup"><span data-stu-id="518f1-148">Click **Create**.</span></span>
3. <span data-ttu-id="518f1-149">单击 "**团队网站**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-149">Click **Team site**.</span></span>
4. <span data-ttu-id="518f1-150">键入网站名称并输入组所有者的名称（网站所有者）。</span><span class="sxs-lookup"><span data-stu-id="518f1-150">Type a site name and enter a name for the Group owner (site owner).</span></span>
5. <span data-ttu-id="518f1-151">在 "**高级设置**" 下，选择是否希望它成为公用或专用网站。</span><span class="sxs-lookup"><span data-stu-id="518f1-151">Under **Advanced settings**, choose if you want this to be a public or private site.</span></span>
6. <span data-ttu-id="518f1-152">单击"下一步"。</span><span class="sxs-lookup"><span data-stu-id="518f1-152">Click **Next**.</span></span>
7. <span data-ttu-id="518f1-153">单击“完成”\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="518f1-153">Click **Finish**.</span></span>

<span data-ttu-id="518f1-154">我们将稍后邀请用户。</span><span class="sxs-lookup"><span data-stu-id="518f1-154">We'll invite users later.</span></span> <span data-ttu-id="518f1-155">接下来，请务必检查此网站的网站级共享设置。</span><span class="sxs-lookup"><span data-stu-id="518f1-155">Next, it's important to check the site-level sharing settings for this site.</span></span>

## <a name="sharepoint-site-level-sharing-settings"></a><span data-ttu-id="518f1-156">SharePoint 网站级别共享设置</span><span class="sxs-lookup"><span data-stu-id="518f1-156">SharePoint site level sharing settings</span></span>

<span data-ttu-id="518f1-157">检查网站级别的共享设置以确保它们允许您对此网站所需的访问类型。</span><span class="sxs-lookup"><span data-stu-id="518f1-157">Check the site-level sharing settings to make sure that they allow the type of access that you want for this site.</span></span> <span data-ttu-id="518f1-158">例如，如果将组织级别设置设置为 "**任何人**"，但希望所有来宾都对此网站进行身份验证，请确保将网站级别的共享设置设置为 "**新建" 和 "现有来宾**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-158">For example, if you set the organization-level settings to **Anyone**, but you want all guests to authenticate for this site, then make sure the site-level sharing settings are set to **New and existing guests**.</span></span>

<span data-ttu-id="518f1-159">请注意，不能与匿名用户（**任何人**设置）共享网站，但可以对各个文件和文件夹进行共享。</span><span class="sxs-lookup"><span data-stu-id="518f1-159">Note that the site cannot be shared with anonymous users (**Anyone** setting), but individual files and folders can.</span></span>

![SharePoint 网站外部共享设置的屏幕截图](media/sharepoint-site-external-sharing-settings.png)

<span data-ttu-id="518f1-161">设置网站级共享设置</span><span class="sxs-lookup"><span data-stu-id="518f1-161">To set site-level sharing settings</span></span>
1. <span data-ttu-id="518f1-162">在 SharePoint 管理中心中，在左侧导航栏中，展开 "**网站**"，然后单击 "**活动网站**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-162">In the SharePoint admin center, in the left navigation, expand **Sites** and click **Active sites**.</span></span>
2. <span data-ttu-id="518f1-163">选择您刚刚创建的网站。</span><span class="sxs-lookup"><span data-stu-id="518f1-163">Select the site that you just created.</span></span>
3. <span data-ttu-id="518f1-164">在功能区中，单击 "**共享**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-164">In the ribbon, click **Sharing**.</span></span>
4. <span data-ttu-id="518f1-165">确保将 "共享" 设置为 "**任何人**" 或 "**新的和现有的来宾**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-165">Ensure that sharing is set to **Anyone** or **New and existing guests**.</span></span>
5. <span data-ttu-id="518f1-166">如果进行了更改，请单击 "**保存**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-166">If you made changes, click **Save**.</span></span>

## <a name="invite-users"></a><span data-ttu-id="518f1-167">邀请用户</span><span class="sxs-lookup"><span data-stu-id="518f1-167">Invite users</span></span>

<span data-ttu-id="518f1-168">现在已配置来宾共享设置，因此您可以开始向网站添加内部用户和来宾。</span><span class="sxs-lookup"><span data-stu-id="518f1-168">Guest sharing settings are now configured, so you can start adding internal users and guests to your site.</span></span> <span data-ttu-id="518f1-169">网站访问通过关联的 Office 365 组进行控制，因此我们将在此处添加用户。</span><span class="sxs-lookup"><span data-stu-id="518f1-169">Site access is controlled through the associated Office 365 Group, so we'll be adding users there.</span></span>

<span data-ttu-id="518f1-170">向组邀请内部用户</span><span class="sxs-lookup"><span data-stu-id="518f1-170">To invite internal users to a group</span></span>
1. <span data-ttu-id="518f1-171">导航到要在其中添加用户的网站。</span><span class="sxs-lookup"><span data-stu-id="518f1-171">Navigate to the site where you want to add users.</span></span>
2. <span data-ttu-id="518f1-172">单击右上角的 "**成员**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-172">Click **Members** in the upper right.</span></span>
3. <span data-ttu-id="518f1-173">单击“**添加成员**”。</span><span class="sxs-lookup"><span data-stu-id="518f1-173">Click **Add members**.</span></span>
4. <span data-ttu-id="518f1-174">键入要邀请到网站的用户的名称或电子邮件地址，然后单击 "**保存**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-174">Type the names or email addresses of the users that you want to invite to the site, and then click **Save**.</span></span>

<span data-ttu-id="518f1-175">无法从网站添加来宾用户。</span><span class="sxs-lookup"><span data-stu-id="518f1-175">Guest users can't be added from the site.</span></span> <span data-ttu-id="518f1-176">您需要在 web 上使用 Outlook 添加它们。</span><span class="sxs-lookup"><span data-stu-id="518f1-176">You need to add them using Outlook on the web.</span></span>

<span data-ttu-id="518f1-177">将来宾邀请到网站</span><span class="sxs-lookup"><span data-stu-id="518f1-177">To invite guests to a site</span></span>
1. <span data-ttu-id="518f1-178">在 web 上的 Outlook 中的 "**组**" 下，单击要在其中添加成员的组。</span><span class="sxs-lookup"><span data-stu-id="518f1-178">In Outlook on the web, under **Groups**, click the group where you want to add members.</span></span>
2. <span data-ttu-id="518f1-179">打开组联系人卡片，然后在 "**更多选项**（...）" 下，单击 "**添加成员**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-179">Open the group contact card, and then, under **More options** (...), click **Add members**.</span></span>
3. <span data-ttu-id="518f1-180">键入要邀请的来宾的电子邮件地址，然后单击 "**添加**"。</span><span class="sxs-lookup"><span data-stu-id="518f1-180">Type the email addresses of the guests that you want to invite, and then click **Add**.</span></span>
4. <span data-ttu-id="518f1-181">单击“关闭”\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="518f1-181">Click **Close**.</span></span>

## <a name="see-also"></a><span data-ttu-id="518f1-182">另请参阅</span><span class="sxs-lookup"><span data-stu-id="518f1-182">See Also</span></span>