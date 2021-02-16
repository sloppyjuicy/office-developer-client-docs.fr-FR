---
title: Propriété canonique PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360885"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="5e398-103">Propriété canonique PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="5e398-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="5e398-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e398-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e398-105">Représente la valeur de la **propriété dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5e398-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e398-106">Noms convivial :</span><span class="sxs-lookup"><span data-stu-id="5e398-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="5e398-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="5e398-107">None</span></span>  <br/> |
|<span data-ttu-id="5e398-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5e398-108">Property set:</span></span>  <br/> |<span data-ttu-id="5e398-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5e398-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="5e398-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="5e398-110">Property name:</span></span>  <br/> |<span data-ttu-id="5e398-111">X-Sharing-Flavor</span><span class="sxs-lookup"><span data-stu-id="5e398-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="5e398-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5e398-112">Data type:</span></span>  <br/> |<span data-ttu-id="5e398-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e398-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5e398-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5e398-114">Area:</span></span>  <br/> |<span data-ttu-id="5e398-115">Partage</span><span class="sxs-lookup"><span data-stu-id="5e398-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e398-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e398-116">Remarks</span></span>

<span data-ttu-id="5e398-117">La **propriété dispidSharingFlavor** doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e398-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="5e398-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5e398-118">**Value**</span></span>|<span data-ttu-id="5e398-119">**Type de message de partage**</span><span class="sxs-lookup"><span data-stu-id="5e398-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e398-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="5e398-120">0x00020310</span></span>  <br/> |<span data-ttu-id="5e398-121">Invitation de partage pour un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="5e398-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="5e398-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="5e398-122">0x00000310</span></span>  <br/> |<span data-ttu-id="5e398-123">Invitation de partage pour un dossier qui n’est pas un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="5e398-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="5e398-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="5e398-124">0x00020500</span></span>  <br/> |<span data-ttu-id="5e398-125">Demande de partage.</span><span class="sxs-lookup"><span data-stu-id="5e398-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="5e398-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="5e398-126">0x00020710</span></span>  <br/> |<span data-ttu-id="5e398-127">Invitation de partage pour un dossier spécial et demande de partage pour le dossier spécial équivalent du destinataire.</span><span class="sxs-lookup"><span data-stu-id="5e398-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="5e398-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="5e398-128">0x00025100</span></span>  <br/> |<span data-ttu-id="5e398-129">Réponse de partage qui refuse une demande.</span><span class="sxs-lookup"><span data-stu-id="5e398-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="5e398-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="5e398-130">0x00023310</span></span>  <br/> |<span data-ttu-id="5e398-131">Réponse de partage qui accepte une demande (également un type d’invitation de partage).</span><span class="sxs-lookup"><span data-stu-id="5e398-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5e398-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5e398-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e398-133">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5e398-133">Protocol specifications</span></span>

<span data-ttu-id="5e398-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e398-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e398-135">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="5e398-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e398-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e398-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e398-137">Partage des dossiers de boîte aux lettres entre clients.</span><span class="sxs-lookup"><span data-stu-id="5e398-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e398-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5e398-138">Header files</span></span>

<span data-ttu-id="5e398-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e398-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e398-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5e398-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e398-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e398-141">See also</span></span>



[<span data-ttu-id="5e398-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5e398-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e398-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5e398-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e398-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5e398-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e398-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5e398-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

