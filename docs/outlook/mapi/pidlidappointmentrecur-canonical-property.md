---
title: Propriété canonique PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785012"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="942a4-103">Propriété canonique PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="942a4-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="942a4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="942a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="942a4-105">Spécifie les dates et heures quand une série périodique se produit à l’aide d’une des plages qui sont spécifiés dans [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)les périodicités.</span><span class="sxs-lookup"><span data-stu-id="942a4-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="942a4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="942a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="942a4-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="942a4-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="942a4-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="942a4-108">Property set:</span></span>  <br/> |<span data-ttu-id="942a4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="942a4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="942a4-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="942a4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="942a4-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="942a4-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="942a4-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="942a4-112">Data type:</span></span>  <br/> |<span data-ttu-id="942a4-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="942a4-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="942a4-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="942a4-114">Area:</span></span>  <br/> |<span data-ttu-id="942a4-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="942a4-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="942a4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="942a4-116">Remarks</span></span>

<span data-ttu-id="942a4-117">Cette propriété spécifie les dates et heures quand une série périodique se produit à l’aide d’un des modèles de périodicité et des plages détaillé dans [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="942a4-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="942a4-118">La valeur de cette propriété contient également des informations sur les exceptions modifiées et supprimées ; informations telles que les dates, objet, emplacement et plusieurs autres propriétés des exceptions.</span><span class="sxs-lookup"><span data-stu-id="942a4-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="942a4-119">Les données binaires dans cette propriété pour les éléments de calendrier périodiques sont stockées en tant que la structure **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="942a4-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="942a4-120">Cette propriété ne doit pas exister sur les éléments de calendrier d’instance unique.</span><span class="sxs-lookup"><span data-stu-id="942a4-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="942a4-121">Il existe certaines limitations pour les périodicités :</span><span class="sxs-lookup"><span data-stu-id="942a4-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="942a4-122">Plusieurs instances ne doivent pas commencer le même jour.</span><span class="sxs-lookup"><span data-stu-id="942a4-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="942a4-123">Occurrences ne doivent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="942a4-123">Occurrences must not overlap.</span></span> <span data-ttu-id="942a4-124">Plus précisément, une exception qui modifie la date de début d’une instance de la série périodique doit se produire sur une date postérieure à la fin de l’instance précédente et le début de l’occurrence suivante de la série périodique.</span><span class="sxs-lookup"><span data-stu-id="942a4-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="942a4-125">Les mêmes a la valeur true si les instances précédents ou suivant dans la série périodique sont les exceptions.</span><span class="sxs-lookup"><span data-stu-id="942a4-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="942a4-126">La planification d’une série périodique est déterminée par sa périodicité et la plage.</span><span class="sxs-lookup"><span data-stu-id="942a4-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="942a4-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="942a4-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="942a4-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="942a4-128">Protocol specifications</span></span>

<span data-ttu-id="942a4-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="942a4-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="942a4-130">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="942a4-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="942a4-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="942a4-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="942a4-132">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="942a4-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="942a4-133">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="942a4-133">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="942a4-134">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="942a4-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="942a4-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="942a4-135">Header files</span></span>

<span data-ttu-id="942a4-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="942a4-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="942a4-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="942a4-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="942a4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="942a4-138">See also</span></span>



[<span data-ttu-id="942a4-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="942a4-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="942a4-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="942a4-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="942a4-141">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="942a4-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="942a4-142">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="942a4-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

