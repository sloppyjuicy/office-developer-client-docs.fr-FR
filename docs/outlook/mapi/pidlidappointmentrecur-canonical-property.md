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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393368"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="3a54c-103">Propriété canonique PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="3a54c-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="3a54c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a54c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a54c-105">Spécifie les dates et heures quand une série périodique se produit à l’aide d’une des plages qui sont spécifiés dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)les périodicités.</span><span class="sxs-lookup"><span data-stu-id="3a54c-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a54c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3a54c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a54c-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="3a54c-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="3a54c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3a54c-108">Property set:</span></span>  <br/> |<span data-ttu-id="3a54c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="3a54c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="3a54c-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="3a54c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3a54c-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="3a54c-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="3a54c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3a54c-112">Data type:</span></span>  <br/> |<span data-ttu-id="3a54c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3a54c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3a54c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3a54c-114">Area:</span></span>  <br/> |<span data-ttu-id="3a54c-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="3a54c-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a54c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a54c-116">Remarks</span></span>

<span data-ttu-id="3a54c-117">Cette propriété spécifie les dates et heures quand une série périodique se produit à l’aide d’un des modèles de périodicité et des plages détaillé dans [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a54c-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="3a54c-118">La valeur de cette propriété contient également des informations sur les exceptions modifiées et supprimées ; informations telles que les dates, objet, emplacement et plusieurs autres propriétés des exceptions.</span><span class="sxs-lookup"><span data-stu-id="3a54c-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="3a54c-119">Les données binaires dans cette propriété pour les éléments de calendrier périodiques sont stockées en tant que la structure **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="3a54c-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="3a54c-120">Cette propriété ne doit pas exister sur les éléments de calendrier d’instance unique.</span><span class="sxs-lookup"><span data-stu-id="3a54c-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="3a54c-121">Il existe certaines limitations pour les périodicités :</span><span class="sxs-lookup"><span data-stu-id="3a54c-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="3a54c-122">Plusieurs instances ne doivent pas commencer le même jour.</span><span class="sxs-lookup"><span data-stu-id="3a54c-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="3a54c-123">Occurrences ne doivent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="3a54c-123">Occurrences must not overlap.</span></span> <span data-ttu-id="3a54c-124">Plus précisément, une exception qui modifie la date de début d’une instance de la série périodique doit se produire sur une date postérieure à la fin de l’instance précédente et le début de l’occurrence suivante de la série périodique.</span><span class="sxs-lookup"><span data-stu-id="3a54c-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="3a54c-125">Les mêmes a la valeur true si les instances précédents ou suivant dans la série périodique sont les exceptions.</span><span class="sxs-lookup"><span data-stu-id="3a54c-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="3a54c-126">La planification d’une série périodique est déterminée par sa périodicité et la plage.</span><span class="sxs-lookup"><span data-stu-id="3a54c-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a54c-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3a54c-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a54c-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3a54c-128">Protocol specifications</span></span>

<span data-ttu-id="3a54c-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a54c-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a54c-130">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="3a54c-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a54c-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a54c-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a54c-132">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="3a54c-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="3a54c-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a54c-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a54c-134">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3a54c-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a54c-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3a54c-135">Header files</span></span>

<span data-ttu-id="3a54c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a54c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a54c-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3a54c-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a54c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a54c-138">See also</span></span>



[<span data-ttu-id="3a54c-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3a54c-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a54c-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3a54c-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a54c-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3a54c-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a54c-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3a54c-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

