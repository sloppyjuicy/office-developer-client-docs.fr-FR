---
title: Propriété canonique PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785051"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="88eb1-103">Propriété canonique PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="88eb1-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="88eb1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88eb1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88eb1-105">Spécifie un champ de bits qui décrit l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="88eb1-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88eb1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="88eb1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88eb1-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="88eb1-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="88eb1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="88eb1-108">Property set:</span></span>  <br/> |<span data-ttu-id="88eb1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="88eb1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="88eb1-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="88eb1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="88eb1-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="88eb1-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="88eb1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="88eb1-112">Data type:</span></span>  <br/> |<span data-ttu-id="88eb1-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="88eb1-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="88eb1-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="88eb1-114">Area:</span></span>  <br/> |<span data-ttu-id="88eb1-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="88eb1-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88eb1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="88eb1-116">Remarks</span></span>

<span data-ttu-id="88eb1-117">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="88eb1-117">This property is not required.</span></span> <span data-ttu-id="88eb1-118">Vous trouverez ci-dessous les indicateurs individuels qui peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="88eb1-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="88eb1-119">M (asfMeeting, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="88eb1-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="88eb1-120">Cet indicateur indique que l’objet est un objet de la réunion ou d’un objet liées à la réunion.</span><span class="sxs-lookup"><span data-stu-id="88eb1-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="88eb1-121">R (asfReceived, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="88eb1-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="88eb1-122">Cet indicateur indique que l’objet représenté a été reçu à partir d’une autre personne.</span><span class="sxs-lookup"><span data-stu-id="88eb1-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="88eb1-123">C (asfCanceled, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="88eb1-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="88eb1-124">Cet indicateur indique que l’objet de la réunion représenté par l’objet a été annulée.</span><span class="sxs-lookup"><span data-stu-id="88eb1-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="88eb1-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="88eb1-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88eb1-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="88eb1-126">Protocol specifications</span></span>

<span data-ttu-id="88eb1-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88eb1-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88eb1-128">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="88eb1-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88eb1-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88eb1-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88eb1-130">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="88eb1-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88eb1-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88eb1-131">Header files</span></span>

<span data-ttu-id="88eb1-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88eb1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="88eb1-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="88eb1-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88eb1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88eb1-134">See also</span></span>



[<span data-ttu-id="88eb1-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="88eb1-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88eb1-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="88eb1-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88eb1-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="88eb1-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88eb1-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="88eb1-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

