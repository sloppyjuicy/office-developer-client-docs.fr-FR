---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787417"
---
# <a name="updel"></a><span data-ttu-id="a8f63-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="a8f63-103">UPDEL</span></span>

  
  
<span data-ttu-id="a8f63-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8f63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8f63-105">Informations pour les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="a8f63-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="a8f63-106">Ces informations sont utilisées pendant le [téléchargement supprimer l’état](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="a8f63-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8f63-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a8f63-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="a8f63-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a8f63-108">Members</span></span>

 <span data-ttu-id="a8f63-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="a8f63-109">_pupde_</span></span>
  
>  <span data-ttu-id="a8f63-110">[out] Vecteur d’entrées [UPDELE](updele.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f63-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="a8f63-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="a8f63-111">_cEnt_</span></span>
  
> <span data-ttu-id="a8f63-112">[out] Nombre d’entrées dans *pupde* .</span><span class="sxs-lookup"><span data-stu-id="a8f63-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8f63-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8f63-113">See also</span></span>



[<span data-ttu-id="a8f63-114">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="a8f63-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a8f63-115">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="a8f63-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a8f63-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a8f63-116">MAPI Constants</span></span>](mapi-constants.md)

