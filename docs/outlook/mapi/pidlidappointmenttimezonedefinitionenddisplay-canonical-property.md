---
title: Propriété canonique PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: facbcb9eed18db304cac334be845c0b3869ba508
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574803"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="5aa8e-103">Propriété canonique PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="5aa8e-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="5aa8e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5aa8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5aa8e-105">Contient un flux qui mappe sur le format persistant d’une structure [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , qui stocke la description pour le fuseau horaire qui est utilisé lorsque l’heure de fin d’un rendez-vous ou d’une demande de réunion est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5aa8e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5aa8e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5aa8e-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="5aa8e-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="5aa8e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5aa8e-108">Property set:</span></span>  <br/> |<span data-ttu-id="5aa8e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5aa8e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5aa8e-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="5aa8e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5aa8e-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="5aa8e-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="5aa8e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5aa8e-112">Data type:</span></span>  <br/> |<span data-ttu-id="5aa8e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5aa8e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5aa8e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5aa8e-114">Area:</span></span>  <br/> |<span data-ttu-id="5aa8e-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="5aa8e-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5aa8e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5aa8e-116">Remarks</span></span>

<span data-ttu-id="5aa8e-117">Microsoft Office Outlook 2003 ou version antérieure et les solutions qui sont basées sur les objets CDO (Collaboration Data) 1.2.1 et qui n’ont pas exécuter l’outil de mise à jour de calendrier pour Outlook ou Microsoft Exchange Server, stockent l’heure de début et heure de fin de l’instance unique rendez-vous et demandes de réunion en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="5aa8e-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5aa8e-118">Ces clients ne stockent pas les informations pour le fuseau horaire dans lequel la demande de réunion ou de rendez-vous est créée.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="5aa8e-119">Mettre à jour les versions de Microsoft Outlook depuis Microsoft Office Outlook 2007 et les solutions basées sur CDO 1.2.1 qui ont été exécutés le calendrier Outlook ou Exchange Server outil utiliser **dispidApptTZDefEndDisplay** pour stocker le fuseau horaire de l’heure de fin.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="5aa8e-120">**dispidApptTZDefEndDisplay** affiche le rendez-vous ou la réunion dans le fuseau horaire d’origine qu’elle a été planifiée et détermine si l’heure de fin doit être ajustée si Modifier les règles du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="5aa8e-121">Si cette propriété est manquante, le fuseau horaire spécifié par la propriété **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="5aa8e-122">Si **dispidApptTZDefStartDisplay** est manquant ou non valide, le fuseau horaire local est supposé.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="5aa8e-123">**dispidApptTZDefEndDisplay** est utilisé à des fins d’affichage uniquement et n’est pas utilisée dans l’extension de périodicité.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="5aa8e-124">Un analyseur doit être prudent lorsqu’il lit un flux de données provenant de **dispidApptTZDefEndDisplay**, ou lorsqu’il persiste **TZDEFINITION** à un flux d’engagement à une propriété binaire, tel que **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="5aa8e-125">Pour plus d’informations, voir [About persistance TZDEFINITION dans un flux de validation dans une propriété binaire](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5aa8e-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="5aa8e-126">**dispidApptTZDefEndDisplay** spécifie les informations de fuseau horaire pour la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5aa8e-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="5aa8e-127">Le format, les contraintes et calcul de **dispidApptTZDefEndDisplay** sont les mêmes que spécifié dans la propriété **dispidApptTZDefStartDisplay** .</span><span class="sxs-lookup"><span data-stu-id="5aa8e-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5aa8e-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5aa8e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5aa8e-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5aa8e-129">Protocol specifications</span></span>

<span data-ttu-id="5aa8e-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5aa8e-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5aa8e-131">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5aa8e-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5aa8e-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5aa8e-133">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5aa8e-134">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5aa8e-134">Header files</span></span>

<span data-ttu-id="5aa8e-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5aa8e-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="5aa8e-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5aa8e-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5aa8e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aa8e-137">See also</span></span>



[<span data-ttu-id="5aa8e-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5aa8e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5aa8e-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5aa8e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5aa8e-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5aa8e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5aa8e-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5aa8e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

