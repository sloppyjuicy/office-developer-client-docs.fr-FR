---
title: Copie d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333053"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="eb187-103">Copie d'un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="eb187-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="eb187-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb187-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="eb187-105">**Pour copier un service de messagerie vers un profil**</span><span class="sxs-lookup"><span data-stu-id="eb187-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="eb187-106">Appelez [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="eb187-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="eb187-107">Lors de la copie d'un service de messagerie, la nouvelle instance du service est configurée exactement de la même façon que l'original.</span><span class="sxs-lookup"><span data-stu-id="eb187-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="eb187-108">Parfois **CopyMsgService** renvoie l'erreur MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="eb187-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="eb187-109">La cause la plus fréquente de cette erreur renvoyée est un service de messagerie qui ne peut pas être dupliqué.</span><span class="sxs-lookup"><span data-stu-id="eb187-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

