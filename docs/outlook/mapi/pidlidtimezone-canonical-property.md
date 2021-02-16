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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319270"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="0ea0e-103">Propriété canonique PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="0ea0e-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="0ea0e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ea0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ea0e-105">Spécifie des informations sur le fuseau horaire d’une réunion périodique.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ea0e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0ea0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ea0e-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="0ea0e-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="0ea0e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0ea0e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0ea0e-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0ea0e-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0ea0e-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="0ea0e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ea0e-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="0ea0e-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="0ea0e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0ea0e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0ea0e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0ea0e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0ea0e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0ea0e-114">Area:</span></span>  <br/> |<span data-ttu-id="0ea0e-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="0ea0e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ea0e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ea0e-116">Remarks</span></span>

<span data-ttu-id="0ea0e-117">Cette propriété est lue uniquement si la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) n’est pas définie, mais si la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) est TRUE et la propriété **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) est FALSE.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="0ea0e-118">Word inférieur spécifie un index dans un tableau qui contient des informations de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="0ea0e-119">Dans la partie supérieure de WORD, seul le bit le plus élevé est lu.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="0ea0e-120">Si ce bit est définie, le fuseau horaire référencé n’observera pas l’heure d’été , sinon les dates d’été détaillées dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) seront suivies.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ea0e-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0ea0e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ea0e-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0ea0e-122">Protocol specifications</span></span>

<span data-ttu-id="0ea0e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea0e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ea0e-124">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ea0e-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea0e-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ea0e-126">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ea0e-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0ea0e-127">Header files</span></span>

<span data-ttu-id="0ea0e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ea0e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ea0e-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0ea0e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ea0e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea0e-130">See also</span></span>



[<span data-ttu-id="0ea0e-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea0e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ea0e-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea0e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ea0e-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea0e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ea0e-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0ea0e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

