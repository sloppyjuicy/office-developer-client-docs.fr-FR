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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356041"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="f5be4-103">Propriété canonique PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="f5be4-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="f5be4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5be4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5be4-105">Spécifie l’utilisateur qui a répondu pour la dernière fois à la demande de réunion ou à l’objet de mise à jour de réunion.</span><span class="sxs-lookup"><span data-stu-id="f5be4-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5be4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f5be4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5be4-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="f5be4-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="f5be4-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f5be4-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5be4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f5be4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f5be4-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="f5be4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5be4-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="f5be4-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="f5be4-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f5be4-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5be4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f5be4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f5be4-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f5be4-114">Area:</span></span>  <br/> |<span data-ttu-id="f5be4-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="f5be4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5be4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5be4-116">Remarks</span></span>

<span data-ttu-id="f5be4-117">Cette propriété est définie uniquement pour un délégant lorsqu’un délégué a répondu.</span><span class="sxs-lookup"><span data-stu-id="f5be4-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="f5be4-118">La valeur est égale à la **propriété PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) pour la boutique du délégué.</span><span class="sxs-lookup"><span data-stu-id="f5be4-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="f5be4-119">Cette propriété n’a aucune signification pour l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="f5be4-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="f5be4-120">Pour plus **d’informations PR_MAILBOX_OWNER_NAME**, voir le protocole d’objet store spécifié dans [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5be4-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5be4-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f5be4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5be4-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f5be4-122">Protocol specifications</span></span>

<span data-ttu-id="f5be4-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5be4-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5be4-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f5be4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5be4-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5be4-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5be4-126">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f5be4-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5be4-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5be4-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5be4-128">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="f5be4-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5be4-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f5be4-129">Header files</span></span>

<span data-ttu-id="f5be4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5be4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5be4-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f5be4-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5be4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5be4-132">See also</span></span>



[<span data-ttu-id="f5be4-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f5be4-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5be4-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f5be4-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5be4-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f5be4-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5be4-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f5be4-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

