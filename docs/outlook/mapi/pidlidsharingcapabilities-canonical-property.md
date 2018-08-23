---
title: Propriété canonique PidLidSharingCapabilities
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b6bf95a68c868bfca247ea21d56dd872092c3e02
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578366"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="115df-103">Propriété canonique PidLidSharingCapabilities</span><span class="sxs-lookup"><span data-stu-id="115df-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="115df-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="115df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="115df-105">Désigne comme une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="115df-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="115df-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="115df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="115df-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="115df-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="115df-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="115df-108">Property set:</span></span>  <br/> |<span data-ttu-id="115df-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="115df-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="115df-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="115df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="115df-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="115df-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="115df-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="115df-112">Data type:</span></span>  <br/> |<span data-ttu-id="115df-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="115df-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="115df-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="115df-114">Area:</span></span>  <br/> |<span data-ttu-id="115df-115">Partage</span><span class="sxs-lookup"><span data-stu-id="115df-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="115df-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="115df-116">Remarks</span></span>

<span data-ttu-id="115df-117">Cette propriété doit être définie sur une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="115df-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="115df-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="115df-118">**Value**</span></span>|<span data-ttu-id="115df-119">**Scénario**</span><span class="sxs-lookup"><span data-stu-id="115df-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="115df-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="115df-120">0x00040290</span></span>  <br/> |<span data-ttu-id="115df-121">Cet objet de Message de partage est lié à un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="115df-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="115df-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="115df-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="115df-123">Cet objet de Message de partage n’est pas relié à un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="115df-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="115df-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="115df-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="115df-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="115df-125">Protocol specifications</span></span>

<span data-ttu-id="115df-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115df-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115df-127">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="115df-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="115df-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="115df-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="115df-129">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="115df-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="115df-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="115df-130">Header files</span></span>

<span data-ttu-id="115df-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="115df-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="115df-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="115df-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="115df-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="115df-133">See also</span></span>



[<span data-ttu-id="115df-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="115df-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="115df-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="115df-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="115df-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="115df-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="115df-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="115df-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

