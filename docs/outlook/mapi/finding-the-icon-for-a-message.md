---
title: Recherche de l'icône d'un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336952"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="68118-103">Recherche de l'icône d'un message</span><span class="sxs-lookup"><span data-stu-id="68118-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="68118-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68118-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="68118-105">**Pour Rechercher l'icône associée à un message**</span><span class="sxs-lookup"><span data-stu-id="68118-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="68118-106">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour récupérer sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68118-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="68118-107">Appelez [MAPIOpenFormMgr](mapiopenformmgr.md) pour récupérer un pointeur d'interface **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="68118-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="68118-108">TransMettez votre pointeur **IMAPISession** dans le paramètre _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="68118-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="68118-109">Appelez [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour récupérer un pointeur d'interface **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="68118-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="68118-110">Utilisez le pointeur **IMAPIFormInfo** pour appeler [IMAPIProp:: GetProps](imapiprop-getprops.md) et récupérer les **Propriétés PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et/ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68118-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

