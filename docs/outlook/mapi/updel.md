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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436798"
---
# <a name="updel"></a><span data-ttu-id="9dc86-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="9dc86-103">UPDEL</span></span>

  
  
<span data-ttu-id="9dc86-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dc86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dc86-105">Informations sur les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="9dc86-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="9dc86-106">Ces informations sont utilisées pendant [l’état de suppression de téléchargement.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="9dc86-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9dc86-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="9dc86-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="9dc86-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9dc86-108">Members</span></span>

 <span data-ttu-id="9dc86-109">_édéde_</span><span class="sxs-lookup"><span data-stu-id="9dc86-109">_pupde_</span></span>
  
>  <span data-ttu-id="9dc86-110">[out] Vecteur des [entrées UPDELE.](updele.md)</span><span class="sxs-lookup"><span data-stu-id="9dc86-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="9dc86-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="9dc86-111">_cEnt_</span></span>
  
> <span data-ttu-id="9dc86-112">[out] Nombre d’entrées  *dans le nœud*  .</span><span class="sxs-lookup"><span data-stu-id="9dc86-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9dc86-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dc86-113">See also</span></span>



[<span data-ttu-id="9dc86-114">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="9dc86-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9dc86-115">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="9dc86-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9dc86-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9dc86-116">MAPI Constants</span></span>](mapi-constants.md)

