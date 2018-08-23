---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bdfabdf02fc0fa6222418bd0fb87e9b6c17d936a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580438"
---
# <a name="uptbl"></a><span data-ttu-id="ff1aa-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="ff1aa-103">UPTBL</span></span>

<span data-ttu-id="ff1aa-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff1aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff1aa-105">Informations de téléchargement du contenu d’un dossier pendant la [Télécharger l’état de la table](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="ff1aa-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff1aa-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ff1aa-106">Quick info</span></span>

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a><span data-ttu-id="ff1aa-107">Members</span><span class="sxs-lookup"><span data-stu-id="ff1aa-107">Members</span></span>

<span data-ttu-id="ff1aa-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-108">_ulFlags_</span></span>
  
> <span data-ttu-id="ff1aa-109">[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="ff1aa-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="ff1aa-110">UPT_OK</span></span>
    
    - <span data-ttu-id="ff1aa-111">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-111">[in] Upload was successful.</span></span> <span data-ttu-id="ff1aa-112">Le client définit après avoir téléchargé le contenu du dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="ff1aa-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="ff1aa-114">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ff1aa-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-115">_pszName_</span></span>
  
> <span data-ttu-id="ff1aa-116">[out] Nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="ff1aa-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-117">_feid_</span></span>
  
> <span data-ttu-id="ff1aa-118">[out] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="ff1aa-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-119">_uintReserved_</span></span>
  
> <span data-ttu-id="ff1aa-120">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ff1aa-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-121">_rgte_</span></span>
  
> <span data-ttu-id="ff1aa-122">[out] Structure contenant les informations suivantes pour les éléments normales (ou non masqués) et associée (ou masqué) dans le dossier : _rgte [0]_ est pour les éléments normales et _rgte [1]_ des éléments associés.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="ff1aa-123">le nombre d’éléments nouveaux ou modifiés</span><span class="sxs-lookup"><span data-stu-id="ff1aa-123">the number of new or modified items</span></span>
   - <span data-ttu-id="ff1aa-124">le nombre d’éléments lus</span><span class="sxs-lookup"><span data-stu-id="ff1aa-124">the number of read items</span></span> 
   - <span data-ttu-id="ff1aa-125">le nombre d’éléments supprimés</span><span class="sxs-lookup"><span data-stu-id="ff1aa-125">the number of deleted items</span></span>
    
 <span data-ttu-id="ff1aa-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-126">_iEnt_</span></span>
  
> <span data-ttu-id="ff1aa-127">[out] Index pour effectuer le suivi de téléchargement le nombre de modifications spécifié par _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="ff1aa-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-128">_cEnt_</span></span>
  
> <span data-ttu-id="ff1aa-129">[out] Nombre de modifications dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="ff1aa-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="ff1aa-131">[out] Chaîne de structures [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1aa-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="ff1aa-132">_Conservés_</span><span class="sxs-lookup"><span data-stu-id="ff1aa-132">_pReserved_</span></span>
  
> <span data-ttu-id="ff1aa-133">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ff1aa-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff1aa-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff1aa-134">See also</span></span>

- [<span data-ttu-id="ff1aa-135">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="ff1aa-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="ff1aa-136">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="ff1aa-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="ff1aa-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ff1aa-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="ff1aa-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="ff1aa-138">UPTBLE</span></span>](uptble.md)

