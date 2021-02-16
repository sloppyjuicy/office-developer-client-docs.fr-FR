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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315931"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="03af0-103">Propriété canonique PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="03af0-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="03af0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03af0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03af0-105">Spécifie une description de la récurrence de l’objet calendrier.</span><span class="sxs-lookup"><span data-stu-id="03af0-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03af0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="03af0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03af0-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="03af0-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="03af0-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="03af0-108">Property set:</span></span>  <br/> |<span data-ttu-id="03af0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="03af0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="03af0-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="03af0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="03af0-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="03af0-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="03af0-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="03af0-112">Data type:</span></span>  <br/> |<span data-ttu-id="03af0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="03af0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="03af0-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="03af0-114">Area:</span></span>  <br/> |<span data-ttu-id="03af0-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="03af0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03af0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="03af0-116">Remarks</span></span>

<span data-ttu-id="03af0-117">Si cette propriété est définie, elle doit être définie sur une description de la périodisation spécifiée par la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03af0-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03af0-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="03af0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03af0-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="03af0-119">Protocol specifications</span></span>

<span data-ttu-id="03af0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03af0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03af0-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="03af0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03af0-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03af0-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03af0-123">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="03af0-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03af0-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="03af0-124">Header files</span></span>

<span data-ttu-id="03af0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03af0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="03af0-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="03af0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03af0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03af0-127">See also</span></span>



[<span data-ttu-id="03af0-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="03af0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03af0-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="03af0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03af0-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="03af0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03af0-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="03af0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

