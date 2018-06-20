---
title: Propriété canonique PidLidAppointmentReplyName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5b6d88b60f9f5c6a01a92ecc5905f711fbf3ab3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785021"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="bce03-103">Propriété canonique PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="bce03-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="bce03-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bce03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bce03-105">Spécifie l’utilisateur qui a répondu dernière à la demande de réunion ou réunion mettre à jour l’objet.</span><span class="sxs-lookup"><span data-stu-id="bce03-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bce03-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bce03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bce03-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="bce03-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="bce03-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="bce03-108">Property set:</span></span>  <br/> |<span data-ttu-id="bce03-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bce03-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bce03-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="bce03-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bce03-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="bce03-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="bce03-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bce03-112">Data type:</span></span>  <br/> |<span data-ttu-id="bce03-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bce03-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bce03-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="bce03-114">Area:</span></span>  <br/> |<span data-ttu-id="bce03-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="bce03-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bce03-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="bce03-116">Remarks</span></span>

<span data-ttu-id="bce03-117">Cette propriété est définie uniquement pour une personne lorsqu’un délégué a répondu.</span><span class="sxs-lookup"><span data-stu-id="bce03-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="bce03-118">La valeur est égale à la propriété **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) pour le magasin du délégué.</span><span class="sxs-lookup"><span data-stu-id="bce03-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="bce03-119">Cette propriété n’a aucune signification pour l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="bce03-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="bce03-120">Pour plus d’informations sur **PR_MAILBOX_OWNER_NAME**, voir stocker le protocole de l’objet spécifié dans [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bce03-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bce03-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bce03-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bce03-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bce03-122">Protocol specifications</span></span>

<span data-ttu-id="bce03-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bce03-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bce03-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bce03-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bce03-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bce03-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bce03-126">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bce03-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bce03-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bce03-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bce03-128">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="bce03-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bce03-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bce03-129">Header files</span></span>

<span data-ttu-id="bce03-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bce03-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bce03-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bce03-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bce03-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bce03-132">See also</span></span>



[<span data-ttu-id="bce03-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bce03-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bce03-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bce03-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bce03-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bce03-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bce03-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="bce03-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

