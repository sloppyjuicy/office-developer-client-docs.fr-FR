---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581124"
---
# <a name="updel"></a><span data-ttu-id="2ac8f-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="2ac8f-103">UPDEL</span></span>

  
  
<span data-ttu-id="2ac8f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ac8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ac8f-105">Informations pour les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="2ac8f-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="2ac8f-106">Ces informations sont utilisées pendant le [téléchargement supprimer l’état](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="2ac8f-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2ac8f-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2ac8f-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="2ac8f-108">Members</span><span class="sxs-lookup"><span data-stu-id="2ac8f-108">Members</span></span>

 <span data-ttu-id="2ac8f-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="2ac8f-109">_pupde_</span></span>
  
>  <span data-ttu-id="2ac8f-110">[out] Vecteur d’entrées [UPDELE](updele.md) .</span><span class="sxs-lookup"><span data-stu-id="2ac8f-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="2ac8f-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="2ac8f-111">_cEnt_</span></span>
  
> <span data-ttu-id="2ac8f-112">[out] Nombre d’entrées dans *pupde* .</span><span class="sxs-lookup"><span data-stu-id="2ac8f-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2ac8f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ac8f-113">See also</span></span>



[<span data-ttu-id="2ac8f-114">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="2ac8f-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2ac8f-115">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="2ac8f-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2ac8f-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2ac8f-116">MAPI Constants</span></span>](mapi-constants.md)

