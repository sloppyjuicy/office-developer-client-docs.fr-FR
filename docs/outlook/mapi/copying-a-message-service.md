---
title: Copie d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425392"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="1c2e0-103">Copie d'un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c2e0-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="1c2e0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c2e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="1c2e0-105">**Pour copier un service de messagerie vers un profil**</span><span class="sxs-lookup"><span data-stu-id="1c2e0-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="1c2e0-106">Appelez [IMsgServiceAdmin:: CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="1c2e0-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="1c2e0-107">Lors de la copie d'un service de messagerie, la nouvelle instance du service est configurée exactement de la même façon que l'original.</span><span class="sxs-lookup"><span data-stu-id="1c2e0-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="1c2e0-108">Parfois **CopyMsgService** renvoie l'erreur MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="1c2e0-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="1c2e0-109">La cause la plus fréquente de cette erreur renvoyée est un service de messagerie qui ne peut pas être dupliqué.</span><span class="sxs-lookup"><span data-stu-id="1c2e0-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

