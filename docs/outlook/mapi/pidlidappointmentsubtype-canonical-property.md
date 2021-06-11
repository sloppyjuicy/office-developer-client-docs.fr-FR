---
title: Propriété canonique PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345415"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="86976-103">Propriété canonique PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="86976-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="86976-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86976-105">Spécifie si l’événement s’agit de la journée.</span><span class="sxs-lookup"><span data-stu-id="86976-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86976-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="86976-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86976-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="86976-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="86976-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="86976-108">Property set:</span></span>  <br/> |<span data-ttu-id="86976-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="86976-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="86976-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="86976-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="86976-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="86976-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="86976-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="86976-112">Data type:</span></span>  <br/> |<span data-ttu-id="86976-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="86976-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="86976-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="86976-114">Area:</span></span>  <br/> |<span data-ttu-id="86976-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="86976-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86976-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="86976-116">Remarks</span></span>

<span data-ttu-id="86976-117">Cette propriété spécifie si l’événement est un événement d’une journée, comme spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86976-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="86976-118">La valeur TRUE indique que l’événement est un événement d’une journée, auquel cas l’heure de début et l’heure de fin doivent être minuit afin que la durée soit un multiple de 24 heures et d’au moins 24 heures.</span><span class="sxs-lookup"><span data-stu-id="86976-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="86976-119">La valeur FALSE ou l’absence de cette propriété indique que l’événement n’est pas un événement d’une journée complète.</span><span class="sxs-lookup"><span data-stu-id="86976-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="86976-120">Le client ou le serveur ne doit pas déduire la valeur comme TRUE lorsqu’un utilisateur crée un événement de 24 heures, même si l’événement commence et se termine à minuit.</span><span class="sxs-lookup"><span data-stu-id="86976-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86976-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="86976-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86976-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="86976-122">Protocol specifications</span></span>

<span data-ttu-id="86976-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86976-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86976-124">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="86976-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86976-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86976-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86976-126">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="86976-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86976-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="86976-127">Header files</span></span>

<span data-ttu-id="86976-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86976-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="86976-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="86976-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86976-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86976-130">See also</span></span>



[<span data-ttu-id="86976-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="86976-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86976-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="86976-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86976-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="86976-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86976-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="86976-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

