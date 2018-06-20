---
title: Propriété canonique PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785507"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="0ec23-103">Propriété canonique PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="0ec23-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="0ec23-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ec23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ec23-105">Spécifie des informations sur le fuseau horaire d’une réunion périodique.</span><span class="sxs-lookup"><span data-stu-id="0ec23-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ec23-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0ec23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ec23-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="0ec23-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="0ec23-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0ec23-108">Property set:</span></span>  <br/> |<span data-ttu-id="0ec23-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0ec23-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0ec23-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="0ec23-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ec23-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="0ec23-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="0ec23-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0ec23-112">Data type:</span></span>  <br/> |<span data-ttu-id="0ec23-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0ec23-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0ec23-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="0ec23-114">Area:</span></span>  <br/> |<span data-ttu-id="0ec23-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="0ec23-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ec23-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ec23-116">Remarks</span></span>

<span data-ttu-id="0ec23-117">Cette propriété est en lecture uniquement si la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) n’est pas définie, mais si la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) est TRUE et la **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) la propriété est FALSE.</span><span class="sxs-lookup"><span data-stu-id="0ec23-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="0ec23-118">Le mot de poids faible spécifie un index dans un tableau qui contient des informations de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="0ec23-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="0ec23-119">À partir du mot supérieur, uniquement le bit le plus élevé est en lecture.</span><span class="sxs-lookup"><span data-stu-id="0ec23-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="0ec23-120">Si ce bit est activé, puis le fuseau horaire référencé n’observera est suivi de l’heure (heure), sinon les dates de l’heure d’été détaillées dans [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0ec23-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ec23-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0ec23-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ec23-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0ec23-122">Protocol specifications</span></span>

<span data-ttu-id="0ec23-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ec23-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ec23-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0ec23-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ec23-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ec23-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ec23-126">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="0ec23-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ec23-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0ec23-127">Header files</span></span>

<span data-ttu-id="0ec23-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ec23-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ec23-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0ec23-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ec23-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ec23-130">See also</span></span>



[<span data-ttu-id="0ec23-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec23-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ec23-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec23-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ec23-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0ec23-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ec23-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0ec23-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

