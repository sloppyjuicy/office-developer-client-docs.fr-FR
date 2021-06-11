---
title: Propriété canonique PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359947"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="2e70a-103">Propriété canonique PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="2e70a-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="2e70a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e70a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e70a-105">Contient la valeur de chaque participant répertorié dans la propriété **dispidNonSendableBCC** ([PidLidNonSendableBcc).](pidlidnonsendablebcc-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="2e70a-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e70a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2e70a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e70a-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="2e70a-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="2e70a-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="2e70a-108">Property set:</span></span>  <br/> |<span data-ttu-id="2e70a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2e70a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2e70a-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="2e70a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2e70a-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="2e70a-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="2e70a-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2e70a-112">Data type:</span></span>  <br/> |<span data-ttu-id="2e70a-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2e70a-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2e70a-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2e70a-114">Area:</span></span>  <br/> |<span data-ttu-id="2e70a-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="2e70a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e70a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e70a-116">Remarks</span></span>

<span data-ttu-id="2e70a-117">Cette propriété est requise uniquement lorsque la **propriété dispidNonSendableBCC** est définie.</span><span class="sxs-lookup"><span data-stu-id="2e70a-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="2e70a-118">Le nombre de valeurs dans cette propriété doit être égal au nombre de valeurs dans le **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="2e70a-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="2e70a-119">Chaque valeur de cette propriété correspond au participant dans la propriété **dispidNonSendableBCC** au même index.</span><span class="sxs-lookup"><span data-stu-id="2e70a-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e70a-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2e70a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e70a-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="2e70a-121">Protocol specifications</span></span>

<span data-ttu-id="2e70a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e70a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e70a-123">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="2e70a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e70a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e70a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e70a-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="2e70a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e70a-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2e70a-126">Header files</span></span>

<span data-ttu-id="2e70a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e70a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e70a-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2e70a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e70a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e70a-129">See also</span></span>



[<span data-ttu-id="2e70a-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2e70a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e70a-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2e70a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e70a-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2e70a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e70a-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2e70a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

