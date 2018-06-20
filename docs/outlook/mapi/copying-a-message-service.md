---
title: Copie d’un Service de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783054"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="eb47a-103">Copie d’un Service de Message</span><span class="sxs-lookup"><span data-stu-id="eb47a-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="eb47a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb47a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="eb47a-105">**Pour copier un service de message à un profil**</span><span class="sxs-lookup"><span data-stu-id="eb47a-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="eb47a-106">Appelez [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="eb47a-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="eb47a-107">Lorsqu’un service de message est copié, la nouvelle instance du service est configurée de la même façon que l’original.</span><span class="sxs-lookup"><span data-stu-id="eb47a-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="eb47a-108">Parfois **CopyMsgService** renvoie l’erreur MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="eb47a-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="eb47a-109">La cause la plus courante de retour de cette erreur est un service de message qui n’autorise pas lui-même à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="eb47a-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

