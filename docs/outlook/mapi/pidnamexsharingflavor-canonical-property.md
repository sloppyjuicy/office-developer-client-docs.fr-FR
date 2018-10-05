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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392122"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="e1480-103">Propriété canonique PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="e1480-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="e1480-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1480-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1480-105">Représente la valeur de la propriété **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1480-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1480-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="e1480-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="e1480-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="e1480-107">None</span></span>  <br/> |
|<span data-ttu-id="e1480-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="e1480-108">Property set:</span></span>  <br/> |<span data-ttu-id="e1480-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="e1480-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="e1480-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="e1480-110">Property name:</span></span>  <br/> |<span data-ttu-id="e1480-111">Version X partage</span><span class="sxs-lookup"><span data-stu-id="e1480-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="e1480-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e1480-112">Data type:</span></span>  <br/> |<span data-ttu-id="e1480-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1480-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e1480-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e1480-114">Area:</span></span>  <br/> |<span data-ttu-id="e1480-115">Partage</span><span class="sxs-lookup"><span data-stu-id="e1480-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1480-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1480-116">Remarks</span></span>

<span data-ttu-id="e1480-117">La propriété **dispidSharingFlavor** doit être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1480-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="e1480-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e1480-118">**Value**</span></span>|<span data-ttu-id="e1480-119">**Type de Message de partage**</span><span class="sxs-lookup"><span data-stu-id="e1480-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1480-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="e1480-120">0x00020310</span></span>  <br/> |<span data-ttu-id="e1480-121">Une invitation de partage pour un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="e1480-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="e1480-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="e1480-122">0x00000310</span></span>  <br/> |<span data-ttu-id="e1480-123">Une invitation de partage pour un dossier qui n’est pas un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="e1480-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="e1480-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="e1480-124">0x00020500</span></span>  <br/> |<span data-ttu-id="e1480-125">Une demande de partage.</span><span class="sxs-lookup"><span data-stu-id="e1480-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="e1480-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="e1480-126">0x00020710</span></span>  <br/> |<span data-ttu-id="e1480-127">Les deux une invitation de partage pour un dossier spécial et une demande de partage pour un dossier spécial équivalente du destinataire.</span><span class="sxs-lookup"><span data-stu-id="e1480-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="e1480-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="e1480-128">0x00025100</span></span>  <br/> |<span data-ttu-id="e1480-129">Une réponse de partage qui refuse une demande.</span><span class="sxs-lookup"><span data-stu-id="e1480-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="e1480-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="e1480-130">0x00023310</span></span>  <br/> |<span data-ttu-id="e1480-131">Une réponse de partage qui accepte une demande (également un type d’invitation de partage).</span><span class="sxs-lookup"><span data-stu-id="e1480-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e1480-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e1480-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1480-133">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e1480-133">Protocol specifications</span></span>

<span data-ttu-id="e1480-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1480-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1480-135">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e1480-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1480-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1480-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1480-137">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="e1480-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1480-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e1480-138">Header files</span></span>

<span data-ttu-id="e1480-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1480-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1480-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e1480-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1480-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1480-141">See also</span></span>



[<span data-ttu-id="e1480-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e1480-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1480-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e1480-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1480-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e1480-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1480-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e1480-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

