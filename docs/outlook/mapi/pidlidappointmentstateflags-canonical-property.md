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
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345359"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="a91bb-103">Propriété canonique PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="a91bb-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a91bb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a91bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a91bb-105">Spécifie un champ de bits qui décrit l'état de l'objet.</span><span class="sxs-lookup"><span data-stu-id="a91bb-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a91bb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a91bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a91bb-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="a91bb-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="a91bb-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="a91bb-108">Property set:</span></span>  <br/> |<span data-ttu-id="a91bb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a91bb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a91bb-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="a91bb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a91bb-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="a91bb-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="a91bb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a91bb-112">Data type:</span></span>  <br/> |<span data-ttu-id="a91bb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a91bb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a91bb-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a91bb-114">Area:</span></span>  <br/> |<span data-ttu-id="a91bb-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="a91bb-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a91bb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a91bb-116">Remarks</span></span>

<span data-ttu-id="a91bb-117">Cette propriété n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a91bb-117">This property is not required.</span></span> <span data-ttu-id="a91bb-118">Vous trouverez ci-dessous les indicateurs individuels qui peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="a91bb-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="a91bb-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a91bb-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="a91bb-120">Cet indicateur indique que l'objet est un objet de réunion ou un objet de réunion.</span><span class="sxs-lookup"><span data-stu-id="a91bb-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="a91bb-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a91bb-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="a91bb-122">Cet indicateur indique que l'objet représenté a été reçu d'une autre personne.</span><span class="sxs-lookup"><span data-stu-id="a91bb-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="a91bb-123">C (asfCanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="a91bb-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="a91bb-124">Cet indicateur indique que l'objet de réunion représenté par l'objet a été annulé.</span><span class="sxs-lookup"><span data-stu-id="a91bb-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a91bb-125">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a91bb-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a91bb-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a91bb-126">Protocol specifications</span></span>

<span data-ttu-id="a91bb-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a91bb-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a91bb-128">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a91bb-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a91bb-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a91bb-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a91bb-130">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="a91bb-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a91bb-131">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a91bb-131">Header files</span></span>

<span data-ttu-id="a91bb-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a91bb-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="a91bb-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a91bb-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a91bb-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a91bb-134">See also</span></span>



[<span data-ttu-id="a91bb-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a91bb-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a91bb-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a91bb-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a91bb-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a91bb-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a91bb-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a91bb-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

