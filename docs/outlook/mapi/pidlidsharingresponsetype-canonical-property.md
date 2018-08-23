---
title: Propriété canonique PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: beb2c46b43ae77de08900aeb987d875e85575aba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563183"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="cc211-103">Propriété canonique PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="cc211-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="cc211-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc211-105">Spécifie le type de réponse à laquelle le destinataire de la demande de partage a répondu.</span><span class="sxs-lookup"><span data-stu-id="cc211-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="cc211-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="cc211-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc211-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cc211-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc211-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="cc211-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="cc211-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="cc211-109">Property set:</span></span>  <br/> |<span data-ttu-id="cc211-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="cc211-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="cc211-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="cc211-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cc211-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="cc211-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="cc211-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cc211-113">Data type:</span></span>  <br/> |<span data-ttu-id="cc211-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc211-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc211-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cc211-115">Area:</span></span>  <br/> |<span data-ttu-id="cc211-116">Partage</span><span class="sxs-lookup"><span data-stu-id="cc211-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc211-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc211-117">Remarks</span></span>

<span data-ttu-id="cc211-118">La valeur de cette propriété doit avoir une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc211-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="cc211-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="cc211-119">**Value**</span></span>|<span data-ttu-id="cc211-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc211-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc211-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc211-121">0x00000000</span></span>  <br/> |<span data-ttu-id="cc211-122">Aucune réponse</span><span class="sxs-lookup"><span data-stu-id="cc211-122">No response</span></span>  <br/> |
|<span data-ttu-id="cc211-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc211-123">0x00000001</span></span>  <br/> |<span data-ttu-id="cc211-124">Acceptée</span><span class="sxs-lookup"><span data-stu-id="cc211-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="cc211-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cc211-125">0x00000002</span></span>  <br/> |<span data-ttu-id="cc211-126">Refusé</span><span class="sxs-lookup"><span data-stu-id="cc211-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cc211-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cc211-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc211-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="cc211-128">Protocol specifications</span></span>

<span data-ttu-id="cc211-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc211-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc211-130">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="cc211-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc211-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc211-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc211-132">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="cc211-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc211-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cc211-133">Header files</span></span>

<span data-ttu-id="cc211-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc211-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc211-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cc211-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc211-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc211-136">See also</span></span>



[<span data-ttu-id="cc211-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cc211-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc211-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cc211-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc211-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cc211-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc211-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cc211-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

