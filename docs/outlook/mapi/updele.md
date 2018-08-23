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
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566585"
---
# <a name="updele"></a><span data-ttu-id="97426-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="97426-103">UPDELE</span></span>

<span data-ttu-id="97426-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97426-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97426-105">Étendue des informations pour les éléments qui ont été supprimés dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="97426-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="97426-106">Ces informations sont utilisées pendant le [téléchargement supprimer l’état](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="97426-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="97426-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="97426-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="97426-108">Members</span><span class="sxs-lookup"><span data-stu-id="97426-108">Members</span></span>

<span data-ttu-id="97426-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97426-109">_ulFlags_</span></span>
  
> <span data-ttu-id="97426-110">[out] / [in] indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="97426-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="97426-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="97426-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="97426-112">[out] Élément est associé.</span><span class="sxs-lookup"><span data-stu-id="97426-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="97426-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="97426-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="97426-114">[out] Élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="97426-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="97426-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="97426-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="97426-116">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="97426-116">[in] Upload was successful.</span></span> <span data-ttu-id="97426-117">Le client définit après le téléchargement des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="97426-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="97426-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="97426-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="97426-119">[in] Élément a été déplacé avec succès.</span><span class="sxs-lookup"><span data-stu-id="97426-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="97426-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="97426-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="97426-121">[in] Élément source marque modifiée.</span><span class="sxs-lookup"><span data-stu-id="97426-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="97426-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="97426-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="97426-123">[in] Valider l’état du téléchargement maintenant (entrée 0).</span><span class="sxs-lookup"><span data-stu-id="97426-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="97426-124">_SKEY_</span><span class="sxs-lookup"><span data-stu-id="97426-124">_skey_</span></span>
  
> <span data-ttu-id="97426-125">[out] Clé de la source de l’élément.</span><span class="sxs-lookup"><span data-stu-id="97426-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="97426-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="97426-126">_dwReserved_</span></span>
  
> <span data-ttu-id="97426-127">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="97426-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="97426-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="97426-128">_binChg_</span></span>
  
> <span data-ttu-id="97426-129">[out] Modifier la clé de l’élément de destination si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="97426-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="97426-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="97426-130">_binPcl_</span></span>
  
> <span data-ttu-id="97426-131">[out] Modifier la liste des éléments de destination si l’élément a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="97426-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="97426-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="97426-132">_skeyDst_</span></span>
  
> <span data-ttu-id="97426-133">[out] Clé de la source de l’élément de destination, si l’élément a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="97426-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="97426-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="97426-134">_pupmov_</span></span>
  
> <span data-ttu-id="97426-135">[out] Informations de dossier de destination si l’élément a été déplacées.</span><span class="sxs-lookup"><span data-stu-id="97426-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97426-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97426-136">See also</span></span>

- [<span data-ttu-id="97426-137">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="97426-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="97426-138">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="97426-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="97426-139">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="97426-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="97426-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="97426-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="97426-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="97426-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="97426-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="97426-142">UPMOV</span></span>](upmov.md)

