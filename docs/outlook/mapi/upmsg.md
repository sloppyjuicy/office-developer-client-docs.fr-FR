---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427268"
---
# <a name="upmsg"></a><span data-ttu-id="c8d60-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="c8d60-103">UPMSG</span></span>

<span data-ttu-id="c8d60-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8d60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8d60-105">Informations pour le téléchargement d'un élément Outlook lors de l' [État du message de chargement](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="c8d60-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c8d60-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c8d60-106">Quick info</span></span>

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a><span data-ttu-id="c8d60-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c8d60-107">Members</span></span>

 <span data-ttu-id="c8d60-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8d60-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c8d60-109">[out]/[in] indicateurs pour déterminer le comportement approprié pendant le chargement.</span><span class="sxs-lookup"><span data-stu-id="c8d60-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="c8d60-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="c8d60-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="c8d60-111">remarquer L'élément est associé.</span><span class="sxs-lookup"><span data-stu-id="c8d60-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="c8d60-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="c8d60-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="c8d60-113">remarquer Nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="c8d60-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="c8d60-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="c8d60-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="c8d60-115">remarquer L'élément a été déplacé ici.</span><span class="sxs-lookup"><span data-stu-id="c8d60-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="c8d60-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="c8d60-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="c8d60-117">remarquer Les propriétés de l'élément ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="c8d60-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="c8d60-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="c8d60-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="c8d60-119">remarquer L'élément est un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="c8d60-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="c8d60-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="c8d60-120">UPM_OK</span></span>
    
    - <span data-ttu-id="c8d60-121">dans Le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="c8d60-121">[in] Upload was successful.</span></span> <span data-ttu-id="c8d60-122">Le client le définit après avoir téléchargé des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c8d60-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="c8d60-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="c8d60-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="c8d60-124">dans L'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c8d60-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="c8d60-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="c8d60-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="c8d60-126">dans Valider l'état du chargement maintenant.</span><span class="sxs-lookup"><span data-stu-id="c8d60-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="c8d60-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="c8d60-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="c8d60-128">dans Supprimez l'élément maintenant.</span><span class="sxs-lookup"><span data-stu-id="c8d60-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="c8d60-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="c8d60-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="c8d60-130">dans Enregistrer les modifications apportées à l'élément.</span><span class="sxs-lookup"><span data-stu-id="c8d60-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="c8d60-131">_PMSG_</span><span class="sxs-lookup"><span data-stu-id="c8d60-131">_pmsg_</span></span>
  
> <span data-ttu-id="c8d60-132">remarquer Ouvrir un objet d'élément.</span><span class="sxs-lookup"><span data-stu-id="c8d60-132">[out] Open item object.</span></span> <span data-ttu-id="c8d60-133">Voir mapidefs. h pour la définition de type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="c8d60-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="c8d60-134">_MEID_</span><span class="sxs-lookup"><span data-stu-id="c8d60-134">_meid_</span></span>
  
> <span data-ttu-id="c8d60-135">remarquer ID d'entrée de l'élément.</span><span class="sxs-lookup"><span data-stu-id="c8d60-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="c8d60-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="c8d60-136">_binReserved1_</span></span>
  
> <span data-ttu-id="c8d60-137">dans Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c8d60-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c8d60-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="c8d60-138">_binReserved2_</span></span>
  
> <span data-ttu-id="c8d60-139">dans Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c8d60-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c8d60-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="c8d60-140">_feid_</span></span>
  
> <span data-ttu-id="c8d60-141">remarquer ID d'entrée du dossier source, si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c8d60-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="c8d60-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="c8d60-142">_binChg_</span></span>
  
> <span data-ttu-id="c8d60-143">remarquer Modifier la clé de l'élément de destination, si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c8d60-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="c8d60-144">Voir mapidefs. h pour la définition de type de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="c8d60-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="c8d60-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="c8d60-145">_binPcl_</span></span>
  
> <span data-ttu-id="c8d60-146">remarquer Modifier la liste de l'élément de destination, si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c8d60-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="c8d60-147">Voir mapidefs. h pour la définition de type de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="c8d60-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="c8d60-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="c8d60-148">_skeySrc_</span></span>
  
> <span data-ttu-id="c8d60-149">remarquer Clé source de l'élément source, si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c8d60-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8d60-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8d60-150">See also</span></span>

- [<span data-ttu-id="c8d60-151">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="c8d60-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="c8d60-152">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="c8d60-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="c8d60-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c8d60-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="c8d60-154">FEID</span><span class="sxs-lookup"><span data-stu-id="c8d60-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="c8d60-155">MEID</span><span class="sxs-lookup"><span data-stu-id="c8d60-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="c8d60-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="c8d60-156">SKEY</span></span>](skey.md)

