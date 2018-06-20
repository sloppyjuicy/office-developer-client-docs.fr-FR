---
title: Propriété canonique PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785080"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="521ec-103">Propriété canonique PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="521ec-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="521ec-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="521ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="521ec-105">Spécifie la valeur du champ CalendarType à partir de la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="521ec-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="521ec-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="521ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="521ec-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="521ec-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="521ec-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="521ec-108">Property set:</span></span>  <br/> |<span data-ttu-id="521ec-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="521ec-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="521ec-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="521ec-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="521ec-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="521ec-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="521ec-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="521ec-112">Data type:</span></span>  <br/> |<span data-ttu-id="521ec-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="521ec-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="521ec-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="521ec-114">Area:</span></span>  <br/> |<span data-ttu-id="521ec-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="521ec-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="521ec-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="521ec-116">Remarks</span></span>

<span data-ttu-id="521ec-117">Lorsque la demande de réunion représente une série périodique ou une exception, il s’agit de la valeur du champ CalendarType à partir de la propriété **dispidApptRecur** .</span><span class="sxs-lookup"><span data-stu-id="521ec-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="521ec-118">Dans le cas contraire, cette propriété n’est pas définie et par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="521ec-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="521ec-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="521ec-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="521ec-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="521ec-120">Protocol specifications</span></span>

<span data-ttu-id="521ec-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521ec-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521ec-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="521ec-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="521ec-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="521ec-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="521ec-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="521ec-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="521ec-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="521ec-125">Header files</span></span>

<span data-ttu-id="521ec-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="521ec-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="521ec-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="521ec-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="521ec-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="521ec-128">See also</span></span>



[<span data-ttu-id="521ec-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="521ec-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="521ec-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="521ec-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="521ec-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="521ec-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="521ec-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="521ec-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

