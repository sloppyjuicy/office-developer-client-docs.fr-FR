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
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430405"
---
# <a name="synccont"></a><span data-ttu-id="5e6ae-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="5e6ae-103">SYNCCONT</span></span>

<span data-ttu-id="5e6ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e6ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e6ae-105">Informations pour la synchronisation du contenu des dossiers spécifiés dans un magasin local avec le serveur lors de l'état de la [synchronisation du contenu](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="5e6ae-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="5e6ae-106">Cela implique le simple téléchargement, ou une synchronisation complète impliquant un chargement, puis un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5e6ae-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5e6ae-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="5e6ae-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5e6ae-108">Members</span></span>

<span data-ttu-id="5e6ae-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e6ae-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5e6ae-110">dans Indicateurs permettant de déterminer le comportement approprié lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="5e6ae-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="5e6ae-111">UPC_OK</span></span>
    
  - <span data-ttu-id="5e6ae-112">dans Le chargement ou la synchronisation complète a réussi.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="5e6ae-113">Le client le définit après avoir synchronisé les informations avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="5e6ae-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="5e6ae-114">_iEnt_</span></span>
  
> <span data-ttu-id="5e6ae-115">remarquer Index à suivre pour effectuer le suivi de la synchronisation du contenu dans le nombre de dossiers spécifiés par _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="5e6ae-116">_Motivé_</span><span class="sxs-lookup"><span data-stu-id="5e6ae-116">_cEnt_</span></span>
  
> <span data-ttu-id="5e6ae-117">remarquer Nombre de dossiers à répliquer.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="5e6ae-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="5e6ae-118">_pvReserved_</span></span>
  
> <span data-ttu-id="5e6ae-119">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="5e6ae-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="5e6ae-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="5e6ae-121">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="5e6ae-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="5e6ae-122">_psosReserved_</span></span>
  
> <span data-ttu-id="5e6ae-123">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5e6ae-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5e6ae-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e6ae-124">See also</span></span>

- [<span data-ttu-id="5e6ae-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="5e6ae-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="5e6ae-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="5e6ae-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="5e6ae-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5e6ae-127">MAPI Constants</span></span>](mapi-constants.md)

