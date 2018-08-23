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
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569854"
---
# <a name="ltid"></a><span data-ttu-id="1ae07-103">LTID</span><span class="sxs-lookup"><span data-stu-id="1ae07-103">LTID</span></span>

  
  
<span data-ttu-id="1ae07-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ae07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ae07-105">Générique ID termes Long d’un objet dans un magasin d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="1ae07-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ae07-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1ae07-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="1ae07-107">Members</span><span class="sxs-lookup"><span data-stu-id="1ae07-107">Members</span></span>

 <span data-ttu-id="1ae07-108">_GUID_</span><span class="sxs-lookup"><span data-stu-id="1ae07-108">_guid_</span></span>
  
- <span data-ttu-id="1ae07-109">[out] Le GUID du serveur qui a créé l’objet.</span><span class="sxs-lookup"><span data-stu-id="1ae07-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="1ae07-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="1ae07-110">_globcnt_</span></span>
  
- <span data-ttu-id="1ae07-111">[out] Numéro unique 6 octets qui identifie l’objet au sein de la banque d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="1ae07-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="1ae07-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="1ae07-112">_wLevel_</span></span>
  
- <span data-ttu-id="1ae07-113">[out] Niveau de la hiérarchie de l’identificateur d’entrée pour un dossier Public favoris Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ae07-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ae07-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae07-114">See also</span></span>



[<span data-ttu-id="1ae07-115">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="1ae07-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1ae07-116">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="1ae07-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1ae07-117">FEID</span><span class="sxs-lookup"><span data-stu-id="1ae07-117">FEID</span></span>](feid.md)

