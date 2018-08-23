---
title: Propriété canonique PidLidRecurrencePattern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 12a55ec4dfe0fb53a07aef73cb4e96771379e483
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589223"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="10a02-103">Propriété canonique PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="10a02-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="10a02-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10a02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10a02-105">Spécifie une description de la périodicité de l’objet calendar.</span><span class="sxs-lookup"><span data-stu-id="10a02-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10a02-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="10a02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10a02-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="10a02-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="10a02-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="10a02-108">Property set:</span></span>  <br/> |<span data-ttu-id="10a02-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="10a02-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="10a02-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="10a02-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10a02-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="10a02-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="10a02-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="10a02-112">Data type:</span></span>  <br/> |<span data-ttu-id="10a02-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10a02-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="10a02-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="10a02-114">Area:</span></span>  <br/> |<span data-ttu-id="10a02-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="10a02-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10a02-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="10a02-116">Remarks</span></span>

<span data-ttu-id="10a02-117">Si cette propriété est définie, elle doit être définie pour une description de la périodicité qui est spécifiée par la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="10a02-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10a02-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="10a02-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10a02-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="10a02-119">Protocol specifications</span></span>

<span data-ttu-id="10a02-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10a02-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10a02-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="10a02-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10a02-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10a02-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10a02-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="10a02-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10a02-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="10a02-124">Header files</span></span>

<span data-ttu-id="10a02-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10a02-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="10a02-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="10a02-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10a02-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a02-127">See also</span></span>



[<span data-ttu-id="10a02-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="10a02-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10a02-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="10a02-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10a02-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="10a02-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10a02-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="10a02-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

