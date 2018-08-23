---
title: Recherche d’une icône pour un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567810"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="b70ee-103">Recherche d’une icône pour un message</span><span class="sxs-lookup"><span data-stu-id="b70ee-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="b70ee-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b70ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b70ee-105">**Pour rechercher l’icône associée à un message**</span><span class="sxs-lookup"><span data-stu-id="b70ee-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="b70ee-106">Appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message pour récupérer la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b70ee-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="b70ee-107">Appelez [MAPIOpenFormMgr](mapiopenformmgr.md) pour récupérer un pointeur d’interface **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="b70ee-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="b70ee-108">Passez le pointeur **IMAPISession** dans le paramètre _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="b70ee-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="b70ee-109">Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d’interface **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="b70ee-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="b70ee-110">Utiliser le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp::GetProps](imapiprop-getprops.md) et de récupérer les propriétés **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) et/ou de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b70ee-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

