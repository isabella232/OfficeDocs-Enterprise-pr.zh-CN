---
title: Office 365 视频网络常见问题
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 12/13/2016
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Adm_O365
search.appverid:
- MET150
- MOE150
- BCS160
ms.assetid: 2bed67a1-4052-49ff-a4ce-b7e6530eb98e
description: Office 365 视频存储库和流式处理服务进行存储和流式处理贵组织中的视频简单。没有大量的关于 Office 365 视频; 绝佳信息此网络常见问题旨在应答周围带宽规划、 加密和服务如何利用内容交付网络 (Cdn) 的最常见问题。
ms.openlocfilehash: bea9838277b5752e4c9905162c0e8525e8aded04
ms.sourcegitcommit: 69d60723e611f3c973a6d6779722aa9da77f647f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2018
ms.locfileid: "22539603"
---
# <a name="office-365-video-networking-frequently-asked-questions"></a><span data-ttu-id="81127-104">Office 365 视频网络常见问题</span><span class="sxs-lookup"><span data-stu-id="81127-104">Office 365 Video networking Frequently Asked Questions</span></span>

<span data-ttu-id="81127-p102">Office 365 视频存储库和流式处理服务进行存储和流式处理贵组织中的视频简单。没有大量的绝佳[关于 Office 365 视频的信息](https://support.office.com/article/Find-help-about-Office-365-Video-b435f99a-f47e-4ebd-a946-f5c965844f50);此网络常见问题旨在应答周围带宽规划、 加密和服务如何利用[内容交付网络 (Cdn)](https://support.office.com/article/Content-delivery-networks-0140f704-6614-49bb-aa6c-89b75dcd7f1f)的最常见问题。</span><span class="sxs-lookup"><span data-stu-id="81127-p102">The Office 365 Video repository and streaming services make storing and streaming videos within your organization simple. There's a lot of great [information about Office 365 Video](https://support.office.com/article/Find-help-about-Office-365-Video-b435f99a-f47e-4ebd-a946-f5c965844f50); this networking FAQ is designed to answer the most common questions around bandwidth planning, encryption, and how the service leverages [content delivery networks (CDNs)](https://support.office.com/article/Content-delivery-networks-0140f704-6614-49bb-aa6c-89b75dcd7f1f).</span></span>
  
<span data-ttu-id="81127-107">如果不已彻底了解上载视频时，会发生什么情况或播放，具有此视频一下我们将在一起，[会发生什么情况到视频文件上载到 Office 365 视频时](https://www.youtube.com/watch?v=HXSZ0jYBKlM)。</span><span class="sxs-lookup"><span data-stu-id="81127-107">If you don't already have a thorough understanding of what happens when a video is uploaded or played back, have a look at this video we put together, [What happens to a video file when uploaded to Office 365 Video](https://www.youtube.com/watch?v=HXSZ0jYBKlM).</span></span>
  
## <a name="what-are-the-office-365-video-bandwidth-requirements"></a><span data-ttu-id="81127-108">Office 365 视频带宽要求是什么？</span><span class="sxs-lookup"><span data-stu-id="81127-108">What are the Office 365 Video bandwidth requirements?</span></span>

<span data-ttu-id="81127-p103">有许多[支持的视频格式](https://support.office.com/article/dd1af01c-fd8e-4640-b17b-93ee02b9b817)可以上载到 Office 365。使用多个不同的视频质量进行播放，每个视频文件然后编码为标准格式。Office 365 视频使用自适应比特率流选择最佳视频播放质量根据可用网络带宽和视频播放器的大小。若要执行此操作，将播放器最初请求最低播放质量。该服务然后开始到视频播放器发送 2 秒视频段。播放器然后可以请求基于速度传递每段的高或较低播放质量。</span><span class="sxs-lookup"><span data-stu-id="81127-p103">There are a numerous [supported video formats](https://support.office.com/article/dd1af01c-fd8e-4640-b17b-93ee02b9b817) that can be uploaded to Office 365. Each video file is then encoded to a standard format with several different video qualities for playback. Office 365 Video uses adaptive bitrate streaming to select the best video playback quality based on the available network bandwidth and size of the video player. To do this, the player initially requests the lowest playback quality. The service then begins sending 2-second video segments to the video player. The player can then request higher or lower playback quality based on how quickly each segment is delivered.</span></span>
  
<span data-ttu-id="81127-p104">自适应比特率流式处理所有这是在后台时以最少中断或缓冲的视频播放。视频播放期间视频播放器，查看者手动重写自动播放质量，若要选择特定的视频播放质量。</span><span class="sxs-lookup"><span data-stu-id="81127-p104">The adaptive bitrate streaming does all this in the background while the video plays with the least amount of disruption or buffering. During video playback, the video player allows the viewer to manually override the automatic playback quality, to select a specific video playback quality.</span></span>
  
<span data-ttu-id="81127-p105">下面是一个快速的表，其中列出了每个视频播放质量的网络要求。每个用户需要播放视频的最小带宽是 802 Kbps。</span><span class="sxs-lookup"><span data-stu-id="81127-p105">Here's a quick table that outlines the network requirements for each of the video playback qualities. The minimum bandwidth per person needed to play a video is 802Kbps.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81127-119">**播放质量**</span><span class="sxs-lookup"><span data-stu-id="81127-119">**Playback Quality**</span></span> <br/> |<span data-ttu-id="81127-120">**网络速度**</span><span class="sxs-lookup"><span data-stu-id="81127-120">**Network Speed**</span></span> <br/> |
|<span data-ttu-id="81127-121">288 p</span><span class="sxs-lookup"><span data-stu-id="81127-121">288p</span></span>  <br/> |<span data-ttu-id="81127-122">802 kbps</span><span class="sxs-lookup"><span data-stu-id="81127-122">802Kbps</span></span>  <br/> |
|<span data-ttu-id="81127-123">360 p</span><span class="sxs-lookup"><span data-stu-id="81127-123">360p</span></span>  <br/> |<span data-ttu-id="81127-124">1.2 Mbps</span><span class="sxs-lookup"><span data-stu-id="81127-124">1.2 Mbps</span></span>  <br/> |
|<span data-ttu-id="81127-125">576 p</span><span class="sxs-lookup"><span data-stu-id="81127-125">576p</span></span>  <br/> |<span data-ttu-id="81127-126">2.5 Mbps</span><span class="sxs-lookup"><span data-stu-id="81127-126">2.5 Mbps</span></span>  <br/> |
|<span data-ttu-id="81127-127">720 p</span><span class="sxs-lookup"><span data-stu-id="81127-127">720p</span></span>  <br/> |<span data-ttu-id="81127-128">3.8 Mbps</span><span class="sxs-lookup"><span data-stu-id="81127-128">3.8 Mbps</span></span>  <br/> |

<span data-ttu-id="81127-129">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-129">([Back to top](office-365-video-networking-faq.md))</span></span>
  
## <a name="how-do-cdns-help-video-playback"></a><span data-ttu-id="81127-130">Cdn 如何帮助视频播放？</span><span class="sxs-lookup"><span data-stu-id="81127-130">How do CDNs help video playback?</span></span>

<span data-ttu-id="81127-p106">如果从同一组织中的相同的地理位置的多个人进行流式处理相同 video(s)，Cdn 将接近到该地理区域的位置中存储这些视频的副本。使用视频存储或缓存最近位置功能、 每个人离开流它们而不是进一步的位置最近的位置的视频。Office 365 视频使用 Azure 媒体服务来管理内容缓存在 Azure Cdn，以及长。Azure 媒体服务可以使用[Azure CDN 位置](https://azure.microsoft.com/documentation/articles/cdn-pop-locations/)任一缓存视频片段和几天的清单。如果您的组织中的用户可以继续观看缓存的视频它们将保持在缓存中。如果几天，视频视频最终将任何一个访问投递被丢弃从缓存中。下次某人尝试观看视频它再次缓存的最接近 CDN 位置。</span><span class="sxs-lookup"><span data-stu-id="81127-p106">If several people from the same organization within the same geographic location are streaming the same video(s), CDNs will store a copy of these videos in a location closer to that geographic region. With the video stored, or cached at the closest location, each person streams the video from the location closest to them instead of a location further away. Office 365 Video uses Azure Media Services to manage what is cached in the Azure CDNs, and for how long. Azure Media Services can use any of the [Azure CDN locations](https://azure.microsoft.com/documentation/articles/cdn-pop-locations/) to cache video fragments and manifests for a few days. If people in your organization continue to watch the cached videos they'll stay in the cache. If no one accesses the video for several days, the video will eventually drop be dropped from the cache. The next time someone attempts to watch the video it's once again cached at the nearest CDN location.</span></span>
  
<span data-ttu-id="81127-p107">若要观看视频内容时，尝试的所有人附近的 CDN 好处从正在靠近，视频，并在小于跃点离开的大多数情况下在缓存。这将提高视频播放速度;但是，它不会更改播放视频网络要求。</span><span class="sxs-lookup"><span data-stu-id="81127-p107">Everyone who attempts to watch the video while the content is cached at a nearby CDN benefits from the video being closer, and in most cases less hops, away. This improves video playback speed; however, it doesn't change the network requirement to play the video.</span></span>
  
> [!NOTE]
> <span data-ttu-id="81127-140">有某些情况下，如已达到，已到达三天之前可能删除视频我们容量限制。</span><span class="sxs-lookup"><span data-stu-id="81127-140">There are some circumstances, such as our capacity limit being reached, where the video may be removed before the three days has been reached.</span></span>
  
<span data-ttu-id="81127-141">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-141">([Back to top](office-365-video-networking-faq.md))</span></span>
  
## <a name="can-i-cache-the-videos-locally-for-faster-playback"></a><span data-ttu-id="81127-142">我可以缓存本地进行更快地播放的视频？</span><span class="sxs-lookup"><span data-stu-id="81127-142">Can I cache the videos locally for faster playback?</span></span>

<span data-ttu-id="81127-p108">是的。Office 365 不会阻止您使用本地 CDN 或缓存代理视频或其他 Office 365 内容引入的更快地访问您的本地网络。有几种方法，以实现您的网络上的本地缓存解决方案，最常用的方法是使用缓存本地内容的代理解决方案。一旦代理或专用 CDN 已缓存的视频片段和清单，将来请求路由到的代理服务器或专用 CDN 这些文件是从本地缓存提取，并且不是从 internet 位置中拉取。考虑类似解决方案的规划过程中的网络带宽、 容量和视频播放并发。</span><span class="sxs-lookup"><span data-stu-id="81127-p108">Yes. Office 365 won't prevent you from using a local CDN or a caching proxy to bring video or other Office 365 content into your local network for faster access. There are several ways to implement a local caching solution on your network, the most common method is to use a proxy solution that caches content locally. Once a proxy or private CDN has cached the video fragments and manifests, future requests for those files that route through the proxy or private CDN are pulled from the local cache and not pulled from an internet location. Consider network bandwidth, capacity, and video playback concurrency during the planning of a solution like this.</span></span>
  
<span data-ttu-id="81127-148">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-148">([Back to top](office-365-video-networking-faq.md))</span></span>
  
## <a name="how-videos-are-encrypted-and-secured"></a><span data-ttu-id="81127-149">如何视频的加密和安全？</span><span class="sxs-lookup"><span data-stu-id="81127-149">How videos are encrypted and secured?</span></span>

<span data-ttu-id="81127-p109">Office 365 视频知道以保持数据安全和专用是多么重要。[Office 365 信任中心](https://products.office.com/business/office-365-trust-center-cloud-computing-security)介绍我们承诺的隐私和安全性内容。视频播放速度很重要的好的体验;但是，我们不会危害您的安全或以换取速度的隐私。下面是我们容纳速度、 安全性和隐私的方式。</span><span class="sxs-lookup"><span data-stu-id="81127-p109">Office 365 Video knows how important it is to keep your data secure and private. [The Office 365 Trust Center](https://products.office.com/business/office-365-trust-center-cloud-computing-security) describes our commitment to the privacy and security of your content. With video playback, speed is important for a good experience; however, we don't compromise your security or privacy in exchange for speed. Here's how we accommodate speed, security and privacy.</span></span>
  
<span data-ttu-id="81127-p110">当您或您的组织中的某人上载新的视频时，视频将是转换代码，用 AES 128 加密，并存储在 Azure 媒体服务。这意味着视频传输过程中和 rest 进行加密。</span><span class="sxs-lookup"><span data-stu-id="81127-p110">When you or someone in your organization uploads a new video, that video is transcoded, encrypted with AES-128 encryption, and stored in Azure Media Services. This means the videos are encrypted both in transit and at rest.</span></span>
  
<span data-ttu-id="81127-156">当您的组织中的某人尝试观看新视频时，它们执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="81127-156">When someone in your organization attempts to watch a new video, they follow these steps:</span></span>
  
1. <span data-ttu-id="81127-157">询问 SharePoint Online 是否有权查看视频。</span><span class="sxs-lookup"><span data-stu-id="81127-157">Ask SharePoint Online if they have permission to view the video.</span></span>

2. <span data-ttu-id="81127-158">SharePoint Online 使用文件权限来确定联系人可以观看视频。</span><span class="sxs-lookup"><span data-stu-id="81127-158">SharePoint Online uses the file permissions to determine if the person can watch the video.</span></span>

3. <span data-ttu-id="81127-159">如果它们允许，SharePoint Online 检索令牌 Azure 授予视频播放器。</span><span class="sxs-lookup"><span data-stu-id="81127-159">If they're allowed, SharePoint Online retrieves a token from Azure to give to the video player.</span></span>

4. <span data-ttu-id="81127-160">视频播放器然后使用令牌从 Azure 请求解密密钥。</span><span class="sxs-lookup"><span data-stu-id="81127-160">The video player then uses the token to request the decryption key from Azure.</span></span>

5. <span data-ttu-id="81127-161">具有 hand 中的加密密钥，视频播放器是能够 stream 视频。</span><span class="sxs-lookup"><span data-stu-id="81127-161">With the decryption key in hand, the video player is able to stream the video.</span></span>

![O365 视频播放](media/9d3c6e76-151d-48a3-a30e-ba8dd07db0b7.png)
  
<span data-ttu-id="81127-163">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-163">([Back to top](office-365-video-networking-faq.md))</span></span>
  
## <a name="what-are-the-requirements-to-playback-office-365-video"></a><span data-ttu-id="81127-164">Office 365 视频播放要求是什么？</span><span class="sxs-lookup"><span data-stu-id="81127-164">What are the requirements to playback Office 365 Video?</span></span>

<span data-ttu-id="81127-p111">Office 365 视频支持的操作系统和 web 浏览器是[Office 365 系统要求](https://support.office.com/article/Office-365-system-requirements-719254c0-2671-4648-9c84-c6a3d4f3be45)中的 SharePoint Online 要求相同。具体取决于哪些操作系统和 web 浏览器配置，您必须将确定视频播放器的特定需求。下面是[视频播放要求](https://support.office.com/article/ca1cc1a9-a615-46e1-b6a3-40dbd99939a6)的详细信息。</span><span class="sxs-lookup"><span data-stu-id="81127-p111">Office 365 Video supported operating systems and web browsers are the same as the SharePoint Online requirements in [Office 365 system requirements](https://support.office.com/article/Office-365-system-requirements-719254c0-2671-4648-9c84-c6a3d4f3be45). Depending on which operating system and web browser configuration you have will determine the specific needs of the video player. Here's more information on [video playback requirements](https://support.office.com/article/ca1cc1a9-a615-46e1-b6a3-40dbd99939a6).</span></span>
  
<span data-ttu-id="81127-168">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-168">([Back to top](office-365-video-networking-faq.md))</span></span>
  
## <a name="i-cant-get-office-365-video-to-work-where-should-i-start"></a><span data-ttu-id="81127-169">无法获取 Office 365 视频起作用，其中应开始？</span><span class="sxs-lookup"><span data-stu-id="81127-169">I can't get Office 365 video to work, where should I start?</span></span>

<span data-ttu-id="81127-p112">Office 365 视频连接疑难解答涉及疑难解答网络、 您 ISP(s)，以及您的 Office 365 的配置。若要启动的第一个位置是服务运行状况仪表板。这将告知您的 Office 365 视频时遇到问题，或不。如果一切正常存在，下面是一些可帮助您的其他资源。</span><span class="sxs-lookup"><span data-stu-id="81127-p112">Troubleshooting connectivity to Office 365 Video involves troubleshooting your network, your ISP(s), and your configuration of Office 365. The first place to start is the service health dashboard. This will tell you of Office 365 Video is having a problem or not. If everything looks great there, here's some additional resources to help you.</span></span>
  
- <span data-ttu-id="81127-174">请确保您可以连接到[Office 365 视频所需的网络终结点](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2)。</span><span class="sxs-lookup"><span data-stu-id="81127-174">Make sure you can connect to the [network endpoints required for Office 365 Video](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2).</span></span>

- <span data-ttu-id="81127-175">检查网络连接使用我们的[Office 365 网络故障排除指南](https://support.office.com/article/Office-365-performance-tuning-and-troubleshooting-Admin-and-IT-Pro-1492cb94-bd62-43e6-b8d0-2a61ed88ebae)。</span><span class="sxs-lookup"><span data-stu-id="81127-175">Check your network connectivity using our [Office 365 network troubleshooting guide](https://support.office.com/article/Office-365-performance-tuning-and-troubleshooting-Admin-and-IT-Pro-1492cb94-bd62-43e6-b8d0-2a61ed88ebae).</span></span>

- <span data-ttu-id="81127-176">请参阅我们[使用在低速网络中的 Office 365 的最佳实践](https://support.office.com/article/Best-practices-for-using-Office-365-on-a-slow-network-fd16c8d2-4799-4c39-8fd7-045f06640166)。</span><span class="sxs-lookup"><span data-stu-id="81127-176">See our [best practices for using Office 365 on a slow network](https://support.office.com/article/Best-practices-for-using-Office-365-on-a-slow-network-fd16c8d2-4799-4c39-8fd7-045f06640166).</span></span>

- <span data-ttu-id="81127-177">查找[有关 Office 365 视频配置帮助](https://support.office.com/article/Find-help-about-Office-365-Video-b435f99a-f47e-4ebd-a946-f5c965844f50)。</span><span class="sxs-lookup"><span data-stu-id="81127-177">Find [help about Office 365 Video configuration](https://support.office.com/article/Find-help-about-Office-365-Video-b435f99a-f47e-4ebd-a946-f5c965844f50).</span></span>

<span data-ttu-id="81127-178">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-178">([Back to top](office-365-video-networking-faq.md))</span></span>
  
## <a name="office-365-video-resources"></a><span data-ttu-id="81127-179">Office 365 视频资源</span><span class="sxs-lookup"><span data-stu-id="81127-179">Office 365 Video resources</span></span>

<span data-ttu-id="81127-p113">评价这一主题和留言，让我们了解如果我们回答您的问题，或者如果您仍在寻找答案。下面是几个我们其他资源以帮助您成功部署和使用 Office 365 视频：</span><span class="sxs-lookup"><span data-stu-id="81127-p113">Rate the topic and leave a comment to let us know if we answered your questions or if you're still looking for answers. Here's a few of our other resources to help you successfully deploy and use Office 365 Video:</span></span>
  
<span data-ttu-id="81127-182">[查找有关 Office 365 视频配置的帮助](https://support.office.com/article/Find-help-about-Office-365-Video-b435f99a-f47e-4ebd-a946-f5c965844f50)。</span><span class="sxs-lookup"><span data-stu-id="81127-182">[Find help about Office 365 Video configuration](https://support.office.com/article/Find-help-about-Office-365-Video-b435f99a-f47e-4ebd-a946-f5c965844f50).</span></span>
  
[<span data-ttu-id="81127-183">满足 Office 365 视频</span><span class="sxs-lookup"><span data-stu-id="81127-183">Meet Office 365 Video</span></span>](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6)
  
[<span data-ttu-id="81127-184">创建和管理 Office 365 视频中的通道</span><span class="sxs-lookup"><span data-stu-id="81127-184">Create and manage a channel in Office 365 Video</span></span>](https://support.office.com/article/Create-and-manage-a-channel-in-Office-365-Video-1fede4cc-13c0-435a-b585-e7fbf1c83bb2)
  
[<span data-ttu-id="81127-185">管理 Office 365 视频门户</span><span class="sxs-lookup"><span data-stu-id="81127-185">Manage your Office 365 Video portal</span></span>](https://support.office.com/article/Manage-your-Office-365-Video-portal-c059465b-eba9-44e1-b8c7-8ff7793ff5da)
  
[<span data-ttu-id="81127-186">在 Office 365 视频中工作的视频格式</span><span class="sxs-lookup"><span data-stu-id="81127-186">Video formats that work in Office 365 Video</span></span>](https://support.office.com/article/Video-formats-that-work-in-Office-365-Video-dd1af01c-fd8e-4640-b17b-93ee02b9b817)
  
<span data-ttu-id="81127-187">（[返回页首](office-365-video-networking-faq.md)）</span><span class="sxs-lookup"><span data-stu-id="81127-187">([Back to top](office-365-video-networking-faq.md))</span></span>
  
<span data-ttu-id="81127-188">这是一个简短的链接，您可以使用回来：[https://aka.ms/video365networkfaq](https://aka.ms/video365networkfaq)</span><span class="sxs-lookup"><span data-stu-id="81127-188">Here's a short link you can use to come back: [https://aka.ms/video365networkfaq](https://aka.ms/video365networkfaq)</span></span>