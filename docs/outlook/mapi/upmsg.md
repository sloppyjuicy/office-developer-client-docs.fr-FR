---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787439"
---
# <a name="upmsg"></a><span data-ttu-id="d44db-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="d44db-103">UPMSG</span></span>

<span data-ttu-id="d44db-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d44db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d44db-105">Informations de téléchargement d’un élément Outlook pendant la [Télécharger l’état du message](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="d44db-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d44db-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d44db-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d44db-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d44db-107">Members</span></span>

 <span data-ttu-id="d44db-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d44db-108">_ulFlags_</span></span>
  
> <span data-ttu-id="d44db-109">[out] / [in] indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d44db-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="d44db-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="d44db-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="d44db-111">[out] Élément est associé.</span><span class="sxs-lookup"><span data-stu-id="d44db-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="d44db-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="d44db-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="d44db-113">[out] Nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="d44db-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="d44db-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="d44db-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="d44db-115">[out] Élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d44db-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="d44db-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="d44db-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="d44db-117">[out] Propriétés des éléments ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="d44db-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="d44db-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="d44db-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="d44db-119">[out] Item est un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="d44db-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="d44db-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="d44db-120">UPM_OK</span></span>
    
    - <span data-ttu-id="d44db-121">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="d44db-121">[in] Upload was successful.</span></span> <span data-ttu-id="d44db-122">Le client définit après le chargement des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d44db-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="d44db-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="d44db-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="d44db-124">[in] Élément a été déplacé avec succès.</span><span class="sxs-lookup"><span data-stu-id="d44db-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="d44db-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d44db-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="d44db-126">[in] Valider : état du téléchargement maintenant.</span><span class="sxs-lookup"><span data-stu-id="d44db-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="d44db-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="d44db-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="d44db-128">[in] Supprimer l’élément maintenant.</span><span class="sxs-lookup"><span data-stu-id="d44db-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="d44db-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="d44db-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="d44db-130">[in] Enregistrez les modifications apportées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="d44db-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="d44db-131">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="d44db-131">_pmsg_</span></span>
  
> <span data-ttu-id="d44db-132">[out] Ouvrir l’élément objet.</span><span class="sxs-lookup"><span data-stu-id="d44db-132">[out] Open item object.</span></span> <span data-ttu-id="d44db-133">Voir mapidefs.h pour la définition du type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="d44db-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="d44db-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="d44db-134">_meid_</span></span>
  
> <span data-ttu-id="d44db-135">[out] ID d’entrée de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d44db-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="d44db-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="d44db-136">_binReserved1_</span></span>
  
> <span data-ttu-id="d44db-137">[in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d44db-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d44db-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="d44db-138">_binReserved2_</span></span>
  
> <span data-ttu-id="d44db-139">[in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d44db-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d44db-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="d44db-140">_feid_</span></span>
  
> <span data-ttu-id="d44db-141">[out] ID d’entrée du dossier source, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d44db-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="d44db-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="d44db-142">_binChg_</span></span>
  
> <span data-ttu-id="d44db-143">[out] Modifier la clé de l’élément de destination, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d44db-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="d44db-144">Voir mapidefs.h pour la définition du type de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="d44db-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="d44db-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="d44db-145">_binPcl_</span></span>
  
> <span data-ttu-id="d44db-146">[out] Modifier la liste de l’élément de destination, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d44db-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="d44db-147">Voir mapidefs.h pour la définition du type de **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="d44db-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="d44db-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="d44db-148">_skeySrc_</span></span>
  
> <span data-ttu-id="d44db-149">[out] Clé de la source de l’élément source, si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d44db-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d44db-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d44db-150">See also</span></span>

- [<span data-ttu-id="d44db-151">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="d44db-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d44db-152">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="d44db-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d44db-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d44db-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="d44db-154">FEID</span><span class="sxs-lookup"><span data-stu-id="d44db-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="d44db-155">MEID</span><span class="sxs-lookup"><span data-stu-id="d44db-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="d44db-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="d44db-156">SKEY</span></span>](skey.md)

