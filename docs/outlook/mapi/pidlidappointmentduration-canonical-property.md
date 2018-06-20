---
title: Propriété canonique PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0d124bd3aa4350863351284a9e4b19ca4533e382
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784978"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="bc498-103">Propriété canonique PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="bc498-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="bc498-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc498-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc498-105">Représente la durée, en minutes, quand il est prévu un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="bc498-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc498-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bc498-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc498-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="bc498-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="bc498-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="bc498-108">Property set:</span></span>  <br/> |<span data-ttu-id="bc498-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bc498-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bc498-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="bc498-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bc498-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="bc498-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="bc498-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bc498-112">Data type:</span></span>  <br/> |<span data-ttu-id="bc498-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bc498-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bc498-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="bc498-114">Area:</span></span>  <br/> |<span data-ttu-id="bc498-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="bc498-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc498-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc498-116">Remarks</span></span>

<span data-ttu-id="bc498-117">La valeur doit être le nombre de minutes entre la valeur de la **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) et les propriétés **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bc498-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc498-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bc498-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc498-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bc498-119">Protocol specifications</span></span>

<span data-ttu-id="bc498-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc498-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc498-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bc498-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc498-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc498-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc498-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="bc498-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc498-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bc498-124">Header files</span></span>

<span data-ttu-id="bc498-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc498-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc498-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bc498-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc498-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc498-127">See also</span></span>



[<span data-ttu-id="bc498-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bc498-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc498-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bc498-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc498-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bc498-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc498-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="bc498-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

