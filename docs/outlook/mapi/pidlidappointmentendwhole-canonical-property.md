---
title: Propriété canonique PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 155300d3c3043713ce2197d3b70843c589d777e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784973"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="840f0-103">Propriété canonique PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="840f0-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="840f0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="840f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="840f0-105">Représente la date et l’heure de fin d’un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="840f0-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="840f0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="840f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="840f0-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="840f0-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="840f0-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="840f0-108">Property set:</span></span>  <br/> |<span data-ttu-id="840f0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="840f0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="840f0-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="840f0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="840f0-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="840f0-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="840f0-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="840f0-112">Data type:</span></span>  <br/> |<span data-ttu-id="840f0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="840f0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="840f0-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="840f0-114">Area:</span></span>  <br/> |<span data-ttu-id="840f0-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="840f0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="840f0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="840f0-116">Remarks</span></span>

<span data-ttu-id="840f0-117">Cette propriété correspond à la propriété **dispidApptEndWhole** du rendez-vous dans le modèle objet Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="840f0-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="840f0-118">Spécifie la date de fin et l’heure de l’événement ; Il doit être en temps universel coordonné (UTC) et doit être supérieure à la valeur de la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="840f0-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="840f0-119">Pour une série périodique, la propriété **dispidApptEndWhole** est la date de fin et l’heure de la première instance en fonction de la périodicité.</span><span class="sxs-lookup"><span data-stu-id="840f0-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="840f0-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="840f0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="840f0-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="840f0-121">Protocol specifications</span></span>

<span data-ttu-id="840f0-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="840f0-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="840f0-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="840f0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="840f0-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="840f0-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="840f0-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="840f0-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="840f0-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="840f0-126">Header files</span></span>

<span data-ttu-id="840f0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="840f0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="840f0-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="840f0-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="840f0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="840f0-129">See also</span></span>



[<span data-ttu-id="840f0-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="840f0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="840f0-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="840f0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="840f0-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="840f0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="840f0-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="840f0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

