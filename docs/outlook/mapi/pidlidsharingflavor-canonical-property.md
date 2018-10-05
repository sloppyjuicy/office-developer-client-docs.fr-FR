---
title: Propriété canonique PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383610"
---
# <a name="pidlidsharingflavor-canonical-property"></a><span data-ttu-id="c544e-103">Propriété canonique PidLidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="c544e-103">PidLidSharingFlavor Canonical Property</span></span>

  
  
<span data-ttu-id="c544e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c544e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c544e-105">Désigne comme une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="c544e-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c544e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c544e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c544e-107">dispidSharingFlavor</span><span class="sxs-lookup"><span data-stu-id="c544e-107">dispidSharingFlavor</span></span>  <br/> |
|<span data-ttu-id="c544e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="c544e-108">Property set:</span></span>  <br/> |<span data-ttu-id="c544e-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="c544e-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="c544e-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="c544e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c544e-111">0x00008A18</span><span class="sxs-lookup"><span data-stu-id="c544e-111">0x00008A18</span></span>  <br/> |
|<span data-ttu-id="c544e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c544e-112">Data type:</span></span>  <br/> |<span data-ttu-id="c544e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c544e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c544e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c544e-114">Area:</span></span>  <br/> |<span data-ttu-id="c544e-115">Partage</span><span class="sxs-lookup"><span data-stu-id="c544e-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c544e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c544e-116">Remarks</span></span>

<span data-ttu-id="c544e-117">La valeur de cette propriété doit être une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c544e-117">The value of this property must be one of the following:</span></span>
  
|<span data-ttu-id="c544e-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c544e-118">**Value**</span></span>|<span data-ttu-id="c544e-119">**Type d’objet du Message de partage**</span><span class="sxs-lookup"><span data-stu-id="c544e-119">**Type of Sharing Message object**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c544e-120">0x00020310</span><span class="sxs-lookup"><span data-stu-id="c544e-120">0x00020310</span></span>  <br/> |<span data-ttu-id="c544e-121">Une invitation de partage pour un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="c544e-121">A sharing invitation for a special folder.</span></span>  <br/> |
|<span data-ttu-id="c544e-122">0x00000310</span><span class="sxs-lookup"><span data-stu-id="c544e-122">0x00000310</span></span>  <br/> |<span data-ttu-id="c544e-123">Une invitation de partage pour un dossier qui n’est pas un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="c544e-123">A sharing invitation for a folder that is not a special folder.</span></span>  <br/> |
|<span data-ttu-id="c544e-124">0x00020500</span><span class="sxs-lookup"><span data-stu-id="c544e-124">0x00020500</span></span>  <br/> |<span data-ttu-id="c544e-125">Une demande de partage.</span><span class="sxs-lookup"><span data-stu-id="c544e-125">A sharing request.</span></span>  <br/> |
|<span data-ttu-id="c544e-126">0x00020710</span><span class="sxs-lookup"><span data-stu-id="c544e-126">0x00020710</span></span>  <br/> |<span data-ttu-id="c544e-127">Les deux une invitation de partage pour un dossier spécial et une demande de partage pour un dossier spécial équivalente du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c544e-127">Both a sharing invitation for a special folder and a sharing request for the recipient's equivalent special folder.</span></span>  <br/> |
|<span data-ttu-id="c544e-128">0x00025100</span><span class="sxs-lookup"><span data-stu-id="c544e-128">0x00025100</span></span>  <br/> |<span data-ttu-id="c544e-129">Le refus d’une demande d’une réponse de partage.</span><span class="sxs-lookup"><span data-stu-id="c544e-129">A sharing response denying a request.</span></span>  <br/> |
|<span data-ttu-id="c544e-130">0x00023310</span><span class="sxs-lookup"><span data-stu-id="c544e-130">0x00023310</span></span>  <br/> |<span data-ttu-id="c544e-131">Acceptation d’une demande (également un type d’invitation de partage) une réponse de partage.</span><span class="sxs-lookup"><span data-stu-id="c544e-131">A sharing response accepting a request (also a type of sharing invitation).</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c544e-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c544e-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c544e-133">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c544e-133">Protocol specifications</span></span>

<span data-ttu-id="c544e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c544e-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c544e-135">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="c544e-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c544e-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c544e-136">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c544e-137">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="c544e-137">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c544e-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c544e-138">Header files</span></span>

<span data-ttu-id="c544e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c544e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="c544e-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c544e-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c544e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c544e-141">See also</span></span>



[<span data-ttu-id="c544e-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c544e-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c544e-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c544e-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c544e-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c544e-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c544e-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c544e-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

