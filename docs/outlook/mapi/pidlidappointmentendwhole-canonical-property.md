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
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358897"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="4e18d-103">Propriété canonique PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="4e18d-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="4e18d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e18d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e18d-105">Représente la date et l'heure de fin d'un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="4e18d-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e18d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4e18d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e18d-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="4e18d-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="4e18d-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="4e18d-108">Property set:</span></span>  <br/> |<span data-ttu-id="4e18d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4e18d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4e18d-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="4e18d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4e18d-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="4e18d-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="4e18d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4e18d-112">Data type:</span></span>  <br/> |<span data-ttu-id="4e18d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4e18d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4e18d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4e18d-114">Area:</span></span>  <br/> |<span data-ttu-id="4e18d-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="4e18d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e18d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e18d-116">Remarks</span></span>

<span data-ttu-id="4e18d-117">Cette propriété correspond à la propriété **dispidApptEndWhole** du rendez-vous dans le modèle objet Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="4e18d-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="4e18d-118">Cette énumération spécifie la date et l'heure de fin de l'événement; elle doit être au format UTC (temps universel coordonné) et doit être supérieure à la valeur de la propriété **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e18d-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="4e18d-119">Pour une série périodique, la propriété **dispidApptEndWhole** est la date et l'heure de fin de la première instance en fonction de la périodicité.</span><span class="sxs-lookup"><span data-stu-id="4e18d-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e18d-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="4e18d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e18d-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4e18d-121">Protocol specifications</span></span>

<span data-ttu-id="4e18d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e18d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e18d-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="4e18d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e18d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e18d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e18d-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="4e18d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e18d-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="4e18d-126">Header files</span></span>

<span data-ttu-id="4e18d-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4e18d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e18d-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4e18d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e18d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e18d-129">See also</span></span>



[<span data-ttu-id="4e18d-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4e18d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e18d-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4e18d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e18d-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4e18d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e18d-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4e18d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

