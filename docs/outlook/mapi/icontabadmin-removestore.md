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
ms.openlocfilehash: 2ec8a28dc52e2aa1f1fa63410b6bd6c13fb5bd57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583987"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="8d18e-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="8d18e-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="8d18e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d18e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d18e-105">Supprime le Contact adresse livre (CAB) spécifié par l’ID d’entrée donné à partir de la hiérarchie de carnets d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8d18e-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="8d18e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d18e-106">Parameters</span></span>

 <span data-ttu-id="8d18e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d18e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8d18e-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="8d18e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8d18e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8d18e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8d18e-110">[in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="8d18e-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

