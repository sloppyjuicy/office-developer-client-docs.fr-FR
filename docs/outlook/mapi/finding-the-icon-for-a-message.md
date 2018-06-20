---
title: Recherche de l’icône d’un Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783295"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="b09ad-103">Recherche de l’icône d’un Message</span><span class="sxs-lookup"><span data-stu-id="b09ad-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="b09ad-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b09ad-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="b09ad-105">**Pour rechercher l’icône associée à un message**</span><span class="sxs-lookup"><span data-stu-id="b09ad-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="b09ad-106">Appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message pour récupérer la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b09ad-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="b09ad-107">Appelez [MAPIOpenFormMgr](mapiopenformmgr.md) pour récupérer un pointeur d’interface **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="b09ad-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="b09ad-108">Passez le pointeur **IMAPISession** dans le paramètre _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="b09ad-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="b09ad-109">Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d’interface **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="b09ad-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="b09ad-110">Utiliser le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp::GetProps](imapiprop-getprops.md) et de récupérer les propriétés **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) et/ou de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b09ad-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

