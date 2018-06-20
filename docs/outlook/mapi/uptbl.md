---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787460"
---
# <a name="uptbl"></a><span data-ttu-id="fc9b7-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="fc9b7-103">UPTBL</span></span>

<span data-ttu-id="fc9b7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc9b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc9b7-105">Informations de téléchargement du contenu d’un dossier pendant la [Télécharger l’état de la table](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="fc9b7-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc9b7-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fc9b7-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="fc9b7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fc9b7-107">Members</span></span>

<span data-ttu-id="fc9b7-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-108">_ulFlags_</span></span>
  
> <span data-ttu-id="fc9b7-109">[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="fc9b7-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="fc9b7-110">UPT_OK</span></span>
    
    - <span data-ttu-id="fc9b7-111">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-111">[in] Upload was successful.</span></span> <span data-ttu-id="fc9b7-112">Le client définit après avoir téléchargé le contenu du dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="fc9b7-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="fc9b7-114">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="fc9b7-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-115">_pszName_</span></span>
  
> <span data-ttu-id="fc9b7-116">[out] Nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="fc9b7-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-117">_feid_</span></span>
  
> <span data-ttu-id="fc9b7-118">[out] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="fc9b7-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-119">_uintReserved_</span></span>
  
> <span data-ttu-id="fc9b7-120">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="fc9b7-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-121">_rgte_</span></span>
  
> <span data-ttu-id="fc9b7-122">[out] Structure contenant les informations suivantes pour les éléments normales (ou non masqués) et associée (ou masqué) dans le dossier : _rgte [0]_ est pour les éléments normales et _rgte [1]_ des éléments associés.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="fc9b7-123">le nombre d’éléments nouveaux ou modifiés</span><span class="sxs-lookup"><span data-stu-id="fc9b7-123">the number of new or modified items</span></span>
   - <span data-ttu-id="fc9b7-124">le nombre d’éléments lus</span><span class="sxs-lookup"><span data-stu-id="fc9b7-124">the number of read items</span></span> 
   - <span data-ttu-id="fc9b7-125">le nombre d’éléments supprimés</span><span class="sxs-lookup"><span data-stu-id="fc9b7-125">the number of deleted items</span></span>
    
 <span data-ttu-id="fc9b7-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-126">_iEnt_</span></span>
  
> <span data-ttu-id="fc9b7-127">[out] Index pour effectuer le suivi de téléchargement le nombre de modifications spécifié par _cEnt_.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="fc9b7-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-128">_cEnt_</span></span>
  
> <span data-ttu-id="fc9b7-129">[out] Nombre de modifications dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="fc9b7-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="fc9b7-131">[out] Chaîne de structures [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9b7-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="fc9b7-132">_Conservés_</span><span class="sxs-lookup"><span data-stu-id="fc9b7-132">_pReserved_</span></span>
  
> <span data-ttu-id="fc9b7-133">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc9b7-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc9b7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc9b7-134">See also</span></span>

- [<span data-ttu-id="fc9b7-135">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="fc9b7-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="fc9b7-136">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="fc9b7-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="fc9b7-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fc9b7-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="fc9b7-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="fc9b7-138">UPTBLE</span></span>](uptble.md)

