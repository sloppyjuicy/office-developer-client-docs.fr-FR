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
# <a name="upmsg"></a><span data-ttu-id="0a0ca-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="0a0ca-103">UPMSG</span></span>

<span data-ttu-id="0a0ca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a0ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a0ca-105">Informations pour le chargement d’un Outlook pendant [l’état de chargement du message.](upload-message-state.md)</span><span class="sxs-lookup"><span data-stu-id="0a0ca-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0a0ca-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0a0ca-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="0a0ca-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0a0ca-107">Members</span></span>

 <span data-ttu-id="0a0ca-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-108">_ulFlags_</span></span>
  
> <span data-ttu-id="0a0ca-109">[out]/[in] Indicateurs pour déterminer le comportement approprié pendant le chargement.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="0a0ca-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="0a0ca-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="0a0ca-111">[out] L’élément est associé.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="0a0ca-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="0a0ca-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="0a0ca-113">[out] Nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="0a0ca-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="0a0ca-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="0a0ca-115">[out] L’élément a été déplacé ici.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="0a0ca-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="0a0ca-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="0a0ca-117">[out] Les propriétés d’élément ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="0a0ca-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="0a0ca-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="0a0ca-119">[out] L’élément est un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="0a0ca-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="0a0ca-120">UPM_OK</span></span>
    
    - <span data-ttu-id="0a0ca-121">[in] Télécharger a réussi.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-121">[in] Upload was successful.</span></span> <span data-ttu-id="0a0ca-122">Le client définit cette information après le téléchargement d’informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="0a0ca-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="0a0ca-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="0a0ca-124">[in] L’élément a été déplacé avec succès.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="0a0ca-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="0a0ca-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="0a0ca-126">[in] Valider l’état de chargement maintenant.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="0a0ca-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="0a0ca-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="0a0ca-128">[in] Supprimez l’élément maintenant.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="0a0ca-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="0a0ca-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="0a0ca-130">[in] Enregistrez les modifications apportées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="0a0ca-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-131">_pmsg_</span></span>
  
> <span data-ttu-id="0a0ca-132">[out] Ouvrir l’objet d’élément.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-132">[out] Open item object.</span></span> <span data-ttu-id="0a0ca-133">Voir mapidefs.h pour la définition de type **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="0a0ca-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-134">_meid_</span></span>
  
> <span data-ttu-id="0a0ca-135">[out] ID d’entrée de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="0a0ca-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-136">_binReserved1_</span></span>
  
> <span data-ttu-id="0a0ca-137">[in] Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="0a0ca-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-138">_binReserved2_</span></span>
  
> <span data-ttu-id="0a0ca-139">[in] Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="0a0ca-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-140">_feid_</span></span>
  
> <span data-ttu-id="0a0ca-141">[out] ID d’entrée du dossier source, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="0a0ca-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-142">_binChg_</span></span>
  
> <span data-ttu-id="0a0ca-143">[out] Modifier la clé de l’élément de destination, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="0a0ca-144">Voir mapidefs.h pour la définition de type **de SBinary**.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="0a0ca-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-145">_binPcl_</span></span>
  
> <span data-ttu-id="0a0ca-146">[out] Modifier la liste de l’élément de destination, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="0a0ca-147">Voir mapidefs.h pour la définition de type **de SBinary**.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="0a0ca-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="0a0ca-148">_skeySrc_</span></span>
  
> <span data-ttu-id="0a0ca-149">[out] Clé source de l’élément source, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="0a0ca-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a0ca-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a0ca-150">See also</span></span>

- [<span data-ttu-id="0a0ca-151">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="0a0ca-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="0a0ca-152">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="0a0ca-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="0a0ca-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0a0ca-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="0a0ca-154">FEID</span><span class="sxs-lookup"><span data-stu-id="0a0ca-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="0a0ca-155">MEID</span><span class="sxs-lookup"><span data-stu-id="0a0ca-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="0a0ca-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="0a0ca-156">SKEY</span></span>](skey.md)

