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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 54b1f0f3bf837ad21e1b271111d4be2ad2c2b3f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573984"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="10934-103">Propriété canonique PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="10934-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="10934-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10934-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10934-105">Spécifie l’utilisateur qui a répondu dernière à la demande de réunion ou réunion mettre à jour l’objet.</span><span class="sxs-lookup"><span data-stu-id="10934-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10934-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="10934-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10934-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="10934-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="10934-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="10934-108">Property set:</span></span>  <br/> |<span data-ttu-id="10934-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="10934-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="10934-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="10934-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10934-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="10934-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="10934-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="10934-112">Data type:</span></span>  <br/> |<span data-ttu-id="10934-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10934-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="10934-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="10934-114">Area:</span></span>  <br/> |<span data-ttu-id="10934-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="10934-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10934-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="10934-116">Remarks</span></span>

<span data-ttu-id="10934-117">Cette propriété est définie uniquement pour une personne lorsqu’un délégué a répondu.</span><span class="sxs-lookup"><span data-stu-id="10934-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="10934-118">La valeur est égale à la propriété **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) pour le magasin du délégué.</span><span class="sxs-lookup"><span data-stu-id="10934-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="10934-119">Cette propriété n’a aucune signification pour l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="10934-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="10934-120">Pour plus d’informations sur **PR_MAILBOX_OWNER_NAME**, voir stocker le protocole de l’objet spécifié dans [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="10934-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10934-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="10934-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10934-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="10934-122">Protocol specifications</span></span>

<span data-ttu-id="10934-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10934-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10934-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="10934-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="10934-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10934-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10934-126">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="10934-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10934-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10934-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10934-128">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="10934-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10934-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="10934-129">Header files</span></span>

<span data-ttu-id="10934-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10934-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="10934-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="10934-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10934-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10934-132">See also</span></span>



[<span data-ttu-id="10934-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="10934-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10934-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="10934-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10934-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="10934-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10934-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="10934-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

