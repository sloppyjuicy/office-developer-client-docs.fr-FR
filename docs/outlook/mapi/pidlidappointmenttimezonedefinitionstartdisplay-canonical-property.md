---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785072"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="174ef-103">Propriété canonique PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="174ef-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="174ef-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="174ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="174ef-105">Contient un flux qui mappe sur le format persistant d’une structure [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description pour le fuseau horaire qui est utilisé lorsque l’heure de début d’un rendez-vous ou d’une demande de réunion est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="174ef-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="174ef-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="174ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="174ef-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="174ef-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="174ef-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="174ef-108">Property set:</span></span>  <br/> |<span data-ttu-id="174ef-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="174ef-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="174ef-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="174ef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="174ef-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="174ef-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="174ef-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="174ef-112">Data type:</span></span>  <br/> |<span data-ttu-id="174ef-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="174ef-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="174ef-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="174ef-114">Area:</span></span>  <br/> |<span data-ttu-id="174ef-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="174ef-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="174ef-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="174ef-116">Remarks</span></span>

<span data-ttu-id="174ef-117">Microsoft Office Outlook 2003 ou version antérieure et les solutions qui sont basées sur les objets CDO (Collaboration Data) 1.2.1 et qui n’ont pas exécuter l’outil de mise à jour de calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et heure de fin de l’instance unique rendez-vous et demandes de réunion en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="174ef-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="174ef-118">Ces clients ne stockent pas les informations pour le fuseau horaire dans lequel la demande de réunion ou de rendez-vous est créée.</span><span class="sxs-lookup"><span data-stu-id="174ef-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="174ef-119">Versions d’Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 et que vous ont exécuté l’outil de mise à jour de calendrier Outlook ou Exchange Server, utilisent cette propriété pour stocker le fuseau horaire de l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="174ef-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="174ef-120">La propriété **dispidApptTZDefStartDisplay** indique le rendez-vous ou la réunion dans le fuseau horaire d’origine qu’il a été planifiée.</span><span class="sxs-lookup"><span data-stu-id="174ef-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="174ef-121">Il détermine si l’heure de début doit être ajusté si Modifier les règles du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="174ef-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="174ef-122">Si cette propriété est manquante, le fuseau horaire local est supposé.</span><span class="sxs-lookup"><span data-stu-id="174ef-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="174ef-123">Cette propriété est utilisée uniquement à des fins d’affichage et n’est pas utilisée dans l’extension de périodicité.</span><span class="sxs-lookup"><span data-stu-id="174ef-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="174ef-124">Un analyseur doit être prudent lorsqu’il lit un flux de données obtenu à partir de cette propriété, ou lorsqu’il persiste **TZDEFINITION** à un flux d’engagement à une propriété binaire, tel que **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="174ef-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="174ef-125">Pour plus d’informations, voir [About persistance TZDEFINITION dans un flux de validation dans une propriété binaire](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="174ef-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="174ef-126">Cette propriété spécifie les informations de fuseau horaire pour la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="174ef-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="174ef-127">La valeur de **dispidApptTZDefStartDisplay** est utilisée pour convertir la date de début et l’heure UTC du fuseau horaire local à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="174ef-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="174ef-128">Pour chaque **TZRULE** spécifié par cette propriété, l’indicateur TZRULE_FLAG_RECUR_CURRENT_TZREG ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="174ef-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="174ef-129">Par exemple, si la **TZRULE** est la règle effective, la valeur du champ, **TZRULE** doit être « 0 x 0002 » ; dans le cas contraire, elle doit être « 0 x 0000 ».</span><span class="sxs-lookup"><span data-stu-id="174ef-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="174ef-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="174ef-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="174ef-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="174ef-131">Protocol specifications</span></span>

<span data-ttu-id="174ef-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="174ef-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="174ef-133">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes...</span><span class="sxs-lookup"><span data-stu-id="174ef-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="174ef-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="174ef-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="174ef-135">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="174ef-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="174ef-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="174ef-136">Header files</span></span>

<span data-ttu-id="174ef-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="174ef-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="174ef-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="174ef-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="174ef-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="174ef-139">See also</span></span>



[<span data-ttu-id="174ef-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="174ef-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="174ef-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="174ef-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="174ef-142">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="174ef-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="174ef-143">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="174ef-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

