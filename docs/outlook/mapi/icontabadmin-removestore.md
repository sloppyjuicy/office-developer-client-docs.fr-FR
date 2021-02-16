---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435417"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="41f1b-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="41f1b-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="41f1b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41f1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41f1b-105">Supprime le carnet d’adresses de contact spécifié par l’ID d’entrée donné de la hiérarchie du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="41f1b-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="41f1b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41f1b-106">Parameters</span></span>

 <span data-ttu-id="41f1b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="41f1b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="41f1b-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="41f1b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="41f1b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="41f1b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="41f1b-110">[in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="41f1b-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

