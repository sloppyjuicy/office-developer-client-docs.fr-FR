---
title: Propriété canonique PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bdfbd553e130a4e463017168a76dc94fc0df827b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331366"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="03882-103">Propriété canonique PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="03882-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="03882-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03882-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03882-105">Contient la valeur de chaque participant répertorié dans la **propriété dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03882-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03882-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="03882-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03882-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="03882-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="03882-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="03882-108">Property set:</span></span>  <br/> |<span data-ttu-id="03882-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="03882-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="03882-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="03882-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="03882-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="03882-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="03882-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="03882-112">Data type:</span></span>  <br/> |<span data-ttu-id="03882-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="03882-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="03882-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="03882-114">Area:</span></span>  <br/> |<span data-ttu-id="03882-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="03882-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03882-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="03882-116">Remarks</span></span>

<span data-ttu-id="03882-117">Cette propriété n’est requise que lorsque la **propriété dispidNonSendableTo** est définie.</span><span class="sxs-lookup"><span data-stu-id="03882-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="03882-118">Le nombre de valeurs dans cette propriété doit être égal au nombre de valeurs dans **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="03882-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="03882-119">Chaque PT_LONG valeur de cette propriété correspond au participant dans la **propriété dispidNonSendableTo** au même index.</span><span class="sxs-lookup"><span data-stu-id="03882-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03882-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="03882-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03882-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="03882-121">Protocol specifications</span></span>

<span data-ttu-id="03882-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03882-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03882-123">Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="03882-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03882-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03882-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03882-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="03882-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03882-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="03882-126">Header files</span></span>

<span data-ttu-id="03882-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03882-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="03882-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="03882-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03882-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03882-129">See also</span></span>



[<span data-ttu-id="03882-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="03882-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03882-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="03882-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03882-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="03882-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03882-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="03882-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

