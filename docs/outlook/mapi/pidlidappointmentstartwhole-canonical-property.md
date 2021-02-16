---
title: Propriété canonique PidLidAppointmentStartWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345373"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="050a8-103">Propriété canonique PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="050a8-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="050a8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="050a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="050a8-105">Représente la date et l’heure de début d’un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="050a8-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="050a8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="050a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="050a8-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="050a8-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="050a8-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="050a8-108">Property set:</span></span>  <br/> |<span data-ttu-id="050a8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="050a8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="050a8-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="050a8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="050a8-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="050a8-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="050a8-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="050a8-112">Data type:</span></span>  <br/> |<span data-ttu-id="050a8-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="050a8-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="050a8-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="050a8-114">Area:</span></span>  <br/> |<span data-ttu-id="050a8-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="050a8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="050a8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="050a8-116">Remarks</span></span>

<span data-ttu-id="050a8-117">Cette propriété spécifie la date et l’heure de début de l’événement.</span><span class="sxs-lookup"><span data-stu-id="050a8-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="050a8-118">Cette propriété doit être en temps universel coordonné (UTC) et doit être inférieure à la valeur de la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="050a8-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="050a8-119">Pour une série périodique, cette propriété est la date et l’heure de début de la première instance en fonction de la récurrence.</span><span class="sxs-lookup"><span data-stu-id="050a8-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="050a8-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="050a8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="050a8-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="050a8-121">Protocol specifications</span></span>

<span data-ttu-id="050a8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="050a8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="050a8-123">Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="050a8-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="050a8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="050a8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="050a8-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="050a8-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="050a8-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="050a8-126">Header files</span></span>

<span data-ttu-id="050a8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="050a8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="050a8-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="050a8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="050a8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="050a8-129">See also</span></span>



[<span data-ttu-id="050a8-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="050a8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="050a8-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="050a8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="050a8-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="050a8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="050a8-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="050a8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

