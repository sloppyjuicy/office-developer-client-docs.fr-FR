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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e3983a110ee9a72f3c82eaf1bbebc810d07f3c4b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591302"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="97101-103">Propriété canonique PidLidAppointmentProposedDuration</span><span class="sxs-lookup"><span data-stu-id="97101-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="97101-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97101-105">Indique la valeur proposée pour la propriété **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) d’une proposition de compteur.</span><span class="sxs-lookup"><span data-stu-id="97101-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97101-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="97101-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97101-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="97101-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="97101-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="97101-108">Property set:</span></span>  <br/> |<span data-ttu-id="97101-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="97101-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="97101-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="97101-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="97101-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="97101-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="97101-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="97101-112">Data type:</span></span>  <br/> |<span data-ttu-id="97101-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97101-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97101-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="97101-114">Area:</span></span>  <br/> |<span data-ttu-id="97101-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="97101-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97101-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="97101-116">Remarks</span></span>

<span data-ttu-id="97101-117">Si la valeur, elle doit être égale au nombre de minutes entre les **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) et les propriétés de **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="97101-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97101-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="97101-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97101-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="97101-119">Protocol specifications</span></span>

<span data-ttu-id="97101-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97101-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97101-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="97101-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97101-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97101-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97101-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="97101-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97101-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="97101-124">Header files</span></span>

<span data-ttu-id="97101-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97101-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="97101-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="97101-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97101-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97101-127">See also</span></span>



[<span data-ttu-id="97101-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="97101-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97101-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="97101-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97101-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="97101-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97101-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="97101-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

