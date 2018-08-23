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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bcdca783778e1a310be638ce376d408acf0b247f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580039"
---
# <a name="pidnamexsharingflavor-canonical-property"></a><span data-ttu-id="77943-103">Propriété canonique PidNameXSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="77943-103">PidNameXSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="77943-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77943-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77943-105">Représente la valeur de la propriété **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="77943-105">Represents the value of the **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77943-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="77943-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="77943-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="77943-107">None</span></span>  <br/> |
|<span data-ttu-id="77943-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="77943-108">Property set:</span></span>  <br/> |<span data-ttu-id="77943-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="77943-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="77943-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="77943-110">Property name:</span></span>  <br/> |<span data-ttu-id="77943-111">Version X partage</span><span class="sxs-lookup"><span data-stu-id="77943-111">X-Sharing-Flavor</span></span>  <br/> |
|<span data-ttu-id="77943-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="77943-112">Data type:</span></span>  <br/> |<span data-ttu-id="77943-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="77943-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="77943-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="77943-114">Area:</span></span>  <br/> |<span data-ttu-id="77943-115">Partage</span><span class="sxs-lookup"><span data-stu-id="77943-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77943-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="77943-116">Remarks</span></span>

<span data-ttu-id="77943-117">La propriété **dispidSharingFlavor** doit être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="77943-117">The **dispidSharingFlavor** property must be one of the following values.</span></span> 
  
|<span data-ttu-id="77943-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="77943-118">**Value**</span></span>|<span data-ttu-id="77943-119">**Type de Message de partage**</span><span class="sxs-lookup"><span data-stu-id="77943-119">**Type of Sharing Message**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77943-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="77943-120">0x00020310</span></span>  <br/> |<span data-ttu-id="77943-121">Une invitation de partage pour un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="77943-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="77943-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="77943-122">0x00000310</span></span>  <br/> |<span data-ttu-id="77943-123">Une invitation de partage pour un dossier qui n’est pas un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="77943-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="77943-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="77943-124">0x00020500</span></span>  <br/> |<span data-ttu-id="77943-125">Une demande de partage.</span><span class="sxs-lookup"><span data-stu-id="77943-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="77943-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="77943-126">0x00020710</span></span>  <br/> |<span data-ttu-id="77943-127">Les deux une invitation de partage pour un dossier spécial et une demande de partage pour un dossier spécial équivalente du destinataire.</span><span class="sxs-lookup"><span data-stu-id="77943-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="77943-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="77943-128">0x00025100</span></span>  <br/> |<span data-ttu-id="77943-129">Une réponse de partage qui refuse une demande.</span><span class="sxs-lookup"><span data-stu-id="77943-129">A sharing response that denies a request.</span></span>  <br/> |
|<span data-ttu-id="77943-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="77943-130">0x00023310</span></span>  <br/> |<span data-ttu-id="77943-131">Une réponse de partage qui accepte une demande (également un type d’invitation de partage).</span><span class="sxs-lookup"><span data-stu-id="77943-131">A sharing response that accepts a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="77943-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="77943-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77943-133">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="77943-133">Protocol specifications</span></span>

<span data-ttu-id="77943-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77943-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77943-135">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="77943-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="77943-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77943-136">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77943-137">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="77943-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77943-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="77943-138">Header files</span></span>

<span data-ttu-id="77943-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77943-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="77943-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="77943-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77943-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77943-141">See also</span></span>



[<span data-ttu-id="77943-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="77943-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77943-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="77943-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77943-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="77943-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77943-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="77943-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

