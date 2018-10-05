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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400830"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="38ce6-103">Propriété canonique PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="38ce6-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="38ce6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38ce6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38ce6-105">Contient une valeur qui indique l’avis de l’expéditeur du message de l’importance d’un message.</span><span class="sxs-lookup"><span data-stu-id="38ce6-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38ce6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="38ce6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38ce6-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="38ce6-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="38ce6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="38ce6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38ce6-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="38ce6-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="38ce6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="38ce6-110">Data type:</span></span>  <br/> |<span data-ttu-id="38ce6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="38ce6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="38ce6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="38ce6-112">Area:</span></span>  <br/> |<span data-ttu-id="38ce6-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="38ce6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38ce6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="38ce6-114">Remarks</span></span>

<span data-ttu-id="38ce6-115">Cette propriété et la propriété **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondus.</span><span class="sxs-lookup"><span data-stu-id="38ce6-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="38ce6-116">Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel de système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="38ce6-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="38ce6-117">Priorité plus élevée indique généralement un coût plus élevé.</span><span class="sxs-lookup"><span data-stu-id="38ce6-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="38ce6-118">Importance supérieure est généralement associée à un autre affichage par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38ce6-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="38ce6-119">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38ce6-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="38ce6-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="38ce6-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="38ce6-121">Le message a une importance faible.</span><span class="sxs-lookup"><span data-stu-id="38ce6-121">The message has low importance.</span></span>
    
<span data-ttu-id="38ce6-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="38ce6-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="38ce6-123">Le message a une haute importance.</span><span class="sxs-lookup"><span data-stu-id="38ce6-123">The message has high importance.</span></span>
    
<span data-ttu-id="38ce6-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="38ce6-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="38ce6-125">Le message a importance normale.</span><span class="sxs-lookup"><span data-stu-id="38ce6-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="38ce6-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="38ce6-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38ce6-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="38ce6-127">Protocol specifications</span></span>

<span data-ttu-id="38ce6-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ce6-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ce6-129">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="38ce6-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38ce6-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ce6-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ce6-131">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38ce6-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38ce6-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="38ce6-132">Header files</span></span>

<span data-ttu-id="38ce6-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38ce6-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="38ce6-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="38ce6-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="38ce6-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="38ce6-135">Mapitags.h</span></span>
  
> <span data-ttu-id="38ce6-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="38ce6-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38ce6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38ce6-137">See also</span></span>



[<span data-ttu-id="38ce6-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="38ce6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38ce6-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="38ce6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38ce6-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="38ce6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38ce6-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="38ce6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

