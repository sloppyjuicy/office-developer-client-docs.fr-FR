---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419435"
---
# <a name="ltid"></a><span data-ttu-id="7ce9d-103">LTID</span><span class="sxs-lookup"><span data-stu-id="7ce9d-103">LTID</span></span>

  
  
<span data-ttu-id="7ce9d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ce9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ce9d-105">ID générique à long terme d’un objet dans un magasin Outlook de données.</span><span class="sxs-lookup"><span data-stu-id="7ce9d-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7ce9d-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7ce9d-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="7ce9d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7ce9d-107">Members</span></span>

 <span data-ttu-id="7ce9d-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="7ce9d-108">_guid_</span></span>
  
- <span data-ttu-id="7ce9d-109">[out] GUID du serveur qui a créé l’objet.</span><span class="sxs-lookup"><span data-stu-id="7ce9d-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="7ce9d-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="7ce9d-110">_globcnt_</span></span>
  
- <span data-ttu-id="7ce9d-111">[out] Nombre unique de 6 Outlook.</span><span class="sxs-lookup"><span data-stu-id="7ce9d-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="7ce9d-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="7ce9d-112">_wLevel_</span></span>
  
- <span data-ttu-id="7ce9d-113">[out] Niveau de hiérarchie de l’ID d’entrée d’Exchange dossier public favori.</span><span class="sxs-lookup"><span data-stu-id="7ce9d-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ce9d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ce9d-114">See also</span></span>



[<span data-ttu-id="7ce9d-115">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7ce9d-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7ce9d-116">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7ce9d-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7ce9d-117">FEID</span><span class="sxs-lookup"><span data-stu-id="7ce9d-117">FEID</span></span>](feid.md)

