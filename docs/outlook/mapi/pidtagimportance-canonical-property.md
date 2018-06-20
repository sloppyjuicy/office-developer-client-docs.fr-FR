---
title: Propriété canonique PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786098"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="38075-103">Propriété canonique PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="38075-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="38075-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38075-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38075-105">Contient une valeur qui indique l’avis de l’expéditeur du message de l’importance d’un message.</span><span class="sxs-lookup"><span data-stu-id="38075-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38075-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="38075-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38075-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="38075-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="38075-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="38075-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38075-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="38075-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="38075-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="38075-110">Data type:</span></span>  <br/> |<span data-ttu-id="38075-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="38075-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="38075-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="38075-112">Area:</span></span>  <br/> |<span data-ttu-id="38075-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="38075-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38075-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="38075-114">Remarks</span></span>

<span data-ttu-id="38075-115">Cette propriété et la propriété **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondus.</span><span class="sxs-lookup"><span data-stu-id="38075-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="38075-116">Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel de système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="38075-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="38075-117">Priorité plus élevée indique généralement un coût plus élevé.</span><span class="sxs-lookup"><span data-stu-id="38075-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="38075-118">Importance supérieure est généralement associée à un autre affichage par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38075-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="38075-119">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38075-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="38075-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="38075-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="38075-121">Le message a une importance faible.</span><span class="sxs-lookup"><span data-stu-id="38075-121">The message has low importance.</span></span>
    
<span data-ttu-id="38075-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="38075-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="38075-123">Le message a une haute importance.</span><span class="sxs-lookup"><span data-stu-id="38075-123">The message has high importance.</span></span>
    
<span data-ttu-id="38075-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="38075-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="38075-125">Le message a importance normale.</span><span class="sxs-lookup"><span data-stu-id="38075-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="38075-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="38075-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38075-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="38075-127">Protocol specifications</span></span>

<span data-ttu-id="38075-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38075-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38075-129">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="38075-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38075-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38075-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38075-131">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38075-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38075-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="38075-132">Header files</span></span>

<span data-ttu-id="38075-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38075-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="38075-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="38075-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="38075-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="38075-135">Mapitags.h</span></span>
  
> <span data-ttu-id="38075-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="38075-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38075-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38075-137">See also</span></span>



[<span data-ttu-id="38075-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="38075-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38075-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="38075-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38075-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="38075-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38075-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="38075-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

