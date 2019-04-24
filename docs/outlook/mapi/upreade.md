---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338863"
---
# <a name="upreade"></a><span data-ttu-id="1355e-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="1355e-103">UPREADE</span></span>

<span data-ttu-id="1355e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1355e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1355e-105">Informations étendues pour le téléchargement de l'état de lecture d'un élément pendant l'état de [lecture de téléchargement](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="1355e-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1355e-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1355e-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="1355e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1355e-107">Members</span></span>

<span data-ttu-id="1355e-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1355e-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="1355e-109">[out]/[in] indicateurs pour déterminer le comportement approprié pendant le chargement.</span><span class="sxs-lookup"><span data-stu-id="1355e-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="1355e-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="1355e-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="1355e-111">remarquer L'élément est masqué.</span><span class="sxs-lookup"><span data-stu-id="1355e-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="1355e-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="1355e-112">UPR_READ</span></span>
    
    - <span data-ttu-id="1355e-113">remarquer L'état de lecture de l'élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1355e-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="1355e-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="1355e-114">UPR_OK</span></span>
    
    - <span data-ttu-id="1355e-115">dans Le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="1355e-115">[in] Upload was successful.</span></span> <span data-ttu-id="1355e-116">Le client le définit après avoir téléchargé des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1355e-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="1355e-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1355e-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="1355e-118">dans Télécharger l'état de lecture de l'élément maintenant, au lieu d'attendre la fin de l'état de la [table de chargement](upload-table-state.md) pour traiter plus d'un élément.</span><span class="sxs-lookup"><span data-stu-id="1355e-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="1355e-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="1355e-119">_skey_</span></span>
  
> <span data-ttu-id="1355e-120">remarquer Clé source de l'élément.</span><span class="sxs-lookup"><span data-stu-id="1355e-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1355e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1355e-121">See also</span></span>

- [<span data-ttu-id="1355e-122">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="1355e-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="1355e-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="1355e-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1355e-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1355e-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="1355e-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="1355e-125">UPREAD</span></span>](upread.md)

