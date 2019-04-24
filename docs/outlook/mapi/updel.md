---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360486"
---
# <a name="updel"></a><span data-ttu-id="83a6f-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="83a6f-103">UPDEL</span></span>

  
  
<span data-ttu-id="83a6f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83a6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83a6f-105">Informations pour les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="83a6f-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="83a6f-106">Ces informations sont utilisées lors de l' [État de suppression de chargement](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="83a6f-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="83a6f-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="83a6f-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="83a6f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="83a6f-108">Members</span></span>

 <span data-ttu-id="83a6f-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="83a6f-109">_pupde_</span></span>
  
>  <span data-ttu-id="83a6f-110">remarquer Vecteur des [](updele.md) entrées de la préversion.</span><span class="sxs-lookup"><span data-stu-id="83a6f-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="83a6f-111">_Motivé_</span><span class="sxs-lookup"><span data-stu-id="83a6f-111">_cEnt_</span></span>
  
> <span data-ttu-id="83a6f-112">remarquer Nombre d'entrées dans *pupde* .</span><span class="sxs-lookup"><span data-stu-id="83a6f-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="83a6f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83a6f-113">See also</span></span>



[<span data-ttu-id="83a6f-114">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="83a6f-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="83a6f-115">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="83a6f-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="83a6f-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="83a6f-116">MAPI Constants</span></span>](mapi-constants.md)

