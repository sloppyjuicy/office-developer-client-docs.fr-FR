---
title: Propriété canonique PidLidAppointmentProposedDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedDuration
api_type:
- COM
ms.assetid: 37806778-a19a-4905-a845-525d3912bf9e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 56891591871831ba9496f50b69bf4b94ef012c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784975"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="bb865-103">Propriété canonique PidLidAppointmentProposedDuration</span><span class="sxs-lookup"><span data-stu-id="bb865-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="bb865-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb865-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb865-105">Indique la valeur proposée pour la propriété **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) d’une proposition de compteur.</span><span class="sxs-lookup"><span data-stu-id="bb865-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb865-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bb865-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb865-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="bb865-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="bb865-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="bb865-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb865-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bb865-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bb865-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="bb865-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb865-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="bb865-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="bb865-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bb865-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb865-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bb865-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bb865-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="bb865-114">Area:</span></span>  <br/> |<span data-ttu-id="bb865-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="bb865-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb865-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb865-116">Remarks</span></span>

<span data-ttu-id="bb865-117">Si la valeur, elle doit être égale au nombre de minutes entre les **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) et les propriétés de **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb865-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb865-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bb865-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb865-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bb865-119">Protocol specifications</span></span>

<span data-ttu-id="bb865-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb865-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb865-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bb865-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb865-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb865-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb865-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="bb865-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb865-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bb865-124">Header files</span></span>

<span data-ttu-id="bb865-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb865-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb865-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bb865-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb865-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb865-127">See also</span></span>



[<span data-ttu-id="bb865-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bb865-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb865-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bb865-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb865-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bb865-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb865-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="bb865-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

