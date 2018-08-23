---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b1ab1bd4eb6badc75065ce54d009e034f0fc2b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584673"
---
# <a name="synccont"></a><span data-ttu-id="828fe-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="828fe-103">SYNCCONT</span></span>

<span data-ttu-id="828fe-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="828fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="828fe-105">Informations pour la synchronisation du contenu des dossiers spécifiées dans un magasin local avec le serveur au cours de la [synchronisation de contenu d’un état](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="828fe-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="828fe-106">Cela implique simplement le téléchargement, ou une synchronisation complète impliquant un téléchargement, puis sur Télécharger.</span><span class="sxs-lookup"><span data-stu-id="828fe-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="828fe-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="828fe-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="828fe-108">Members</span><span class="sxs-lookup"><span data-stu-id="828fe-108">Members</span></span>

<span data-ttu-id="828fe-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="828fe-109">_ulFlags_</span></span>
  
> <span data-ttu-id="828fe-110">[in] Indicateurs pour déterminer le comportement approprié lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="828fe-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="828fe-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="828fe-111">UPC_OK</span></span>
    
  - <span data-ttu-id="828fe-112">[in] Synchronisation complète ou transfert a réussi.</span><span class="sxs-lookup"><span data-stu-id="828fe-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="828fe-113">Le client définit après la synchronisation des informations avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="828fe-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="828fe-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="828fe-114">_iEnt_</span></span>
  
> <span data-ttu-id="828fe-115">[out] Index pour effectuer le suivi de synchroniser le contenu dans le nombre de dossiers spécifiée par _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="828fe-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="828fe-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="828fe-116">_cEnt_</span></span>
  
> <span data-ttu-id="828fe-117">[out] Nombre de dossiers à répliquer.</span><span class="sxs-lookup"><span data-stu-id="828fe-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="828fe-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="828fe-118">_pvReserved_</span></span>
  
> <span data-ttu-id="828fe-119">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="828fe-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="828fe-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="828fe-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="828fe-121">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="828fe-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="828fe-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="828fe-122">_psosReserved_</span></span>
  
> <span data-ttu-id="828fe-123">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="828fe-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="828fe-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="828fe-124">See also</span></span>

- [<span data-ttu-id="828fe-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="828fe-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="828fe-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="828fe-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="828fe-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="828fe-127">MAPI Constants</span></span>](mapi-constants.md)

