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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327922"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="ea7d5-103">Propriété canonique PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="ea7d5-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="ea7d5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea7d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea7d5-105">Contient une valeur qui indique l’avis de l’expéditeur du message sur l’importance d’un message.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea7d5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ea7d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea7d5-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="ea7d5-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="ea7d5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ea7d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea7d5-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="ea7d5-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="ea7d5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ea7d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea7d5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea7d5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea7d5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ea7d5-112">Area:</span></span>  <br/> |<span data-ttu-id="ea7d5-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="ea7d5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea7d5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea7d5-114">Remarks</span></span>

<span data-ttu-id="ea7d5-115">Cette propriété et la **propriété PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="ea7d5-116">Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse d’envoi du message par le logiciel système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="ea7d5-117">Une priorité plus élevée indique généralement un coût plus élevé.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="ea7d5-118">Une importance plus élevée est généralement associée à un affichage différent par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="ea7d5-119">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea7d5-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="ea7d5-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="ea7d5-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="ea7d5-121">Le message a une faible importance.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-121">The message has low importance.</span></span>
    
<span data-ttu-id="ea7d5-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="ea7d5-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="ea7d5-123">Le message a une importance particulière.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-123">The message has high importance.</span></span>
    
<span data-ttu-id="ea7d5-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="ea7d5-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="ea7d5-125">Le message a une importance normale.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ea7d5-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ea7d5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea7d5-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ea7d5-127">Protocol specifications</span></span>

<span data-ttu-id="ea7d5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea7d5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea7d5-129">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea7d5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea7d5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea7d5-131">Gère les objets de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea7d5-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ea7d5-132">Header files</span></span>

<span data-ttu-id="ea7d5-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea7d5-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea7d5-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea7d5-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea7d5-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ea7d5-136">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="ea7d5-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea7d5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea7d5-137">See also</span></span>



[<span data-ttu-id="ea7d5-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ea7d5-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea7d5-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ea7d5-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea7d5-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ea7d5-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea7d5-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ea7d5-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

