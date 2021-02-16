---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424881"
---
# <a name="updele"></a><span data-ttu-id="429dc-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="429dc-103">UPDELE</span></span>

<span data-ttu-id="429dc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="429dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="429dc-105">Informations étendues pour les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="429dc-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="429dc-106">Ces informations sont utilisées pendant [l’état de suppression de téléchargement.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="429dc-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="429dc-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="429dc-107">Quick info</span></span>

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a><span data-ttu-id="429dc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="429dc-108">Members</span></span>

<span data-ttu-id="429dc-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="429dc-109">_ulFlags_</span></span>
  
> <span data-ttu-id="429dc-110">[out]/[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="429dc-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="429dc-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="429dc-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="429dc-112">[out] L’élément est associé.</span><span class="sxs-lookup"><span data-stu-id="429dc-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="429dc-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="429dc-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="429dc-114">[out] L’élément a été déplacé vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="429dc-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="429dc-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="429dc-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="429dc-116">[in] Le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="429dc-116">[in] Upload was successful.</span></span> <span data-ttu-id="429dc-117">Le client définit cette information après le téléchargement d’informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="429dc-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="429dc-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="429dc-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="429dc-119">[in] L’élément a été déplacé avec succès.</span><span class="sxs-lookup"><span data-stu-id="429dc-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="429dc-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="429dc-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="429dc-121">[in] Marquez l’élément source comme modifié.</span><span class="sxs-lookup"><span data-stu-id="429dc-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="429dc-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="429dc-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="429dc-123">[in] Valider l’état de chargement maintenant (entrée 0).</span><span class="sxs-lookup"><span data-stu-id="429dc-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="429dc-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="429dc-124">_skey_</span></span>
  
> <span data-ttu-id="429dc-125">[out] Clé source de l’élément.</span><span class="sxs-lookup"><span data-stu-id="429dc-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="429dc-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="429dc-126">_dwReserved_</span></span>
  
> <span data-ttu-id="429dc-127">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="429dc-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="429dc-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="429dc-128">_binChg_</span></span>
  
> <span data-ttu-id="429dc-129">[out] Modifier la clé de l’élément de destination si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="429dc-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="429dc-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="429dc-130">_binPcl_</span></span>
  
> <span data-ttu-id="429dc-131">[out] Modifier la liste de l’élément de destination si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="429dc-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="429dc-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="429dc-132">_skeyDst_</span></span>
  
> <span data-ttu-id="429dc-133">[out] Clé source de l’élément de destination si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="429dc-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="429dc-134">_mov_</span><span class="sxs-lookup"><span data-stu-id="429dc-134">_pupmov_</span></span>
  
> <span data-ttu-id="429dc-135">[out] Informations sur le dossier de destination si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="429dc-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="429dc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="429dc-136">See also</span></span>

- [<span data-ttu-id="429dc-137">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="429dc-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="429dc-138">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="429dc-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="429dc-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="429dc-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="429dc-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="429dc-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="429dc-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="429dc-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="429dc-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="429dc-142">UPMOV</span></span>](upmov.md)

