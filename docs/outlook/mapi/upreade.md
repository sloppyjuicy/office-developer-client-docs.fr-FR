---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787442"
---
# <a name="upreade"></a><span data-ttu-id="7404f-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="7404f-103">UPREADE</span></span>

<span data-ttu-id="7404f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7404f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7404f-105">Obtenir des informations détaillées pour le téléchargement de l’état de lecture d’un élément pendant le [téléchargement lire l’état de l’état](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="7404f-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7404f-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7404f-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="7404f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7404f-107">Members</span></span>

<span data-ttu-id="7404f-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7404f-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="7404f-109">[out] / [in] indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="7404f-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="7404f-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="7404f-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="7404f-111">[out] L’élément est masqué.</span><span class="sxs-lookup"><span data-stu-id="7404f-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="7404f-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="7404f-112">UPR_READ</span></span>
    
    - <span data-ttu-id="7404f-113">[out] L’état de lecture de l’élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="7404f-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="7404f-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="7404f-114">UPR_OK</span></span>
    
    - <span data-ttu-id="7404f-115">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="7404f-115">[in] Upload was successful.</span></span> <span data-ttu-id="7404f-116">Le client définit après le chargement des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7404f-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="7404f-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="7404f-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="7404f-118">[in] Télécharger l’état de lecture de l’élément maintenant, au lieu d’attendre la fin de la [Télécharger l’état de la table](upload-table-state.md) pour le traitement par lots plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="7404f-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="7404f-119">_SKEY_</span><span class="sxs-lookup"><span data-stu-id="7404f-119">_skey_</span></span>
  
> <span data-ttu-id="7404f-120">[out] Clé de la source de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7404f-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7404f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7404f-121">See also</span></span>

- [<span data-ttu-id="7404f-122">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7404f-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="7404f-123">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="7404f-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="7404f-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7404f-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="7404f-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="7404f-125">UPREAD</span></span>](upread.md)

