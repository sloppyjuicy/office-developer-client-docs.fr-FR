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
# <a name="updele"></a><span data-ttu-id="7e6dd-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="7e6dd-103">UPDELE</span></span>

<span data-ttu-id="7e6dd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e6dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e6dd-105">Informations étendues pour les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="7e6dd-106">Ces informations sont utilisées lors de l' [État de suppression de chargement](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="7e6dd-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7e6dd-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7e6dd-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7e6dd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7e6dd-108">Members</span></span>

<span data-ttu-id="7e6dd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7e6dd-110">[out]/[in] indicateurs pour déterminer le comportement approprié pendant le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="7e6dd-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="7e6dd-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="7e6dd-112">remarquer L'élément est associé.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="7e6dd-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="7e6dd-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="7e6dd-114">remarquer L'élément a été déplacé vers l'extérieur.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="7e6dd-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="7e6dd-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="7e6dd-116">dans Le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-116">[in] Upload was successful.</span></span> <span data-ttu-id="7e6dd-117">Le client le définit après avoir téléchargé des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="7e6dd-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="7e6dd-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="7e6dd-119">dans L'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="7e6dd-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7e6dd-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="7e6dd-121">dans Marquer l'élément source comme modifié.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="7e6dd-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="7e6dd-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="7e6dd-123">dans Valider l'état de chargement maintenant (entrée 0).</span><span class="sxs-lookup"><span data-stu-id="7e6dd-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="7e6dd-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-124">_skey_</span></span>
  
> <span data-ttu-id="7e6dd-125">remarquer Clé source de l'élément.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="7e6dd-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-126">_dwReserved_</span></span>
  
> <span data-ttu-id="7e6dd-127">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="7e6dd-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-128">_binChg_</span></span>
  
> <span data-ttu-id="7e6dd-129">remarquer Modifier la clé de l'élément de destination si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="7e6dd-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-130">_binPcl_</span></span>
  
> <span data-ttu-id="7e6dd-131">remarquer Modifier la liste des éléments de destination si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="7e6dd-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-132">_skeyDst_</span></span>
  
> <span data-ttu-id="7e6dd-133">remarquer Clé source de l'élément de destination si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="7e6dd-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="7e6dd-134">_pupmov_</span></span>
  
> <span data-ttu-id="7e6dd-135">remarquer Informations sur le dossier de destination si l'élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="7e6dd-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e6dd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e6dd-136">See also</span></span>

- [<span data-ttu-id="7e6dd-137">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7e6dd-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="7e6dd-138">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7e6dd-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="7e6dd-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7e6dd-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="7e6dd-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="7e6dd-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="7e6dd-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="7e6dd-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="7e6dd-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="7e6dd-142">UPMOV</span></span>](upmov.md)

