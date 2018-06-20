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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cb9f4e0f58ea27d36ba911ed60527a2e53f23727
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785050"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="b9a94-103">Propriété canonique PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="b9a94-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="b9a94-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9a94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9a94-105">Spécifie si l’événement est toute la journée.</span><span class="sxs-lookup"><span data-stu-id="b9a94-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9a94-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b9a94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9a94-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="b9a94-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="b9a94-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="b9a94-108">Property set:</span></span>  <br/> |<span data-ttu-id="b9a94-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b9a94-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b9a94-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="b9a94-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b9a94-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="b9a94-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="b9a94-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b9a94-112">Data type:</span></span>  <br/> |<span data-ttu-id="b9a94-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b9a94-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b9a94-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="b9a94-114">Area:</span></span>  <br/> |<span data-ttu-id="b9a94-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="b9a94-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9a94-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9a94-116">Remarks</span></span>

<span data-ttu-id="b9a94-117">Cette propriété spécifie si l’événement est un événement, tel que spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9a94-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="b9a94-118">La valeur TRUE indique que l’événement est un événement d’une journée entière, auquel cas l’heure de début et heure de fin doivent être minuit afin que la durée est un multiple de 24 heures et au moins 24 heures.</span><span class="sxs-lookup"><span data-stu-id="b9a94-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="b9a94-119">La valeur FALSE ou l’absence de cette propriété indique que l’événement n’est pas une journée entière.</span><span class="sxs-lookup"><span data-stu-id="b9a94-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="b9a94-120">Le client ou le serveur doit déduire pas la valeur True lorsqu’un utilisateur se produit pour créer un événement qui est de 24 heures, même si l’événement démarre et se termine à minuit.</span><span class="sxs-lookup"><span data-stu-id="b9a94-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9a94-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b9a94-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9a94-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b9a94-122">Protocol specifications</span></span>

<span data-ttu-id="b9a94-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9a94-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9a94-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b9a94-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9a94-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9a94-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9a94-126">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="b9a94-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9a94-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b9a94-127">Header files</span></span>

<span data-ttu-id="b9a94-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9a94-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9a94-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b9a94-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9a94-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9a94-130">See also</span></span>



[<span data-ttu-id="b9a94-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b9a94-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9a94-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b9a94-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9a94-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b9a94-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9a94-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b9a94-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

