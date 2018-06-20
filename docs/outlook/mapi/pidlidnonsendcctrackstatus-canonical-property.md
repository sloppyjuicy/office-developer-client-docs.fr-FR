---
title: Propriété canonique PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1b61bbcbe3530e95924689f2729b23769e90c13d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785293"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="9358e-103">Propriété canonique PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="9358e-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="9358e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9358e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9358e-105">Contient la valeur de chaque participant répertoriés dans la propriété **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9358e-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9358e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9358e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9358e-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="9358e-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="9358e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="9358e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9358e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9358e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9358e-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="9358e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9358e-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="9358e-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="9358e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9358e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9358e-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="9358e-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="9358e-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="9358e-114">Area:</span></span>  <br/> |<span data-ttu-id="9358e-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="9358e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9358e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9358e-116">Remarks</span></span>

<span data-ttu-id="9358e-117">Cette propriété est requise uniquement lorsque la valeur de la propriété **dispidNonSendableCC** .</span><span class="sxs-lookup"><span data-stu-id="9358e-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="9358e-118">Le nombre de valeurs dans cette propriété doit correspondre au nombre de valeurs dans **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="9358e-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="9358e-119">Chaque valeur PT_LONG dans cette propriété correspond au participant de la propriété **dispidNonSendableCC** dans le même index.</span><span class="sxs-lookup"><span data-stu-id="9358e-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9358e-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9358e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9358e-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9358e-121">Protocol specifications</span></span>

<span data-ttu-id="9358e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9358e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9358e-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9358e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9358e-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9358e-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9358e-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="9358e-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9358e-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9358e-126">Header files</span></span>

<span data-ttu-id="9358e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9358e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9358e-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9358e-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9358e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9358e-129">See also</span></span>



[<span data-ttu-id="9358e-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9358e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9358e-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9358e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9358e-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9358e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9358e-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9358e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

