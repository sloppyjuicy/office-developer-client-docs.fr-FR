---
title: Propriété canonique PidLidAppointmentReplyTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyTime
api_type:
- COM
ms.assetid: 80a2608b-fc44-455a-86be-d6235caba99e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ba79498569c544d1b0ee22e968477d5b68812c09
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398275"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="ce609-103">Propriété canonique PidLidAppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="ce609-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="ce609-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce609-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce609-105">Spécifie la date et l’heure lorsque le participant a répondu à une mise à jour de réunion ou une demande de réunion reçue.</span><span class="sxs-lookup"><span data-stu-id="ce609-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce609-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ce609-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce609-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="ce609-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="ce609-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="ce609-108">Property set:</span></span>  <br/> |<span data-ttu-id="ce609-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ce609-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ce609-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="ce609-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ce609-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="ce609-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="ce609-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ce609-112">Data type:</span></span>  <br/> |<span data-ttu-id="ce609-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ce609-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ce609-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ce609-114">Area:</span></span>  <br/> |<span data-ttu-id="ce609-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="ce609-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce609-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce609-116">Remarks</span></span>

<span data-ttu-id="ce609-117">La valeur doit être spécifiée dans le temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="ce609-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ce609-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ce609-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ce609-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ce609-119">Protocol specifications</span></span>

<span data-ttu-id="ce609-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce609-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce609-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ce609-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ce609-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce609-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce609-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="ce609-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ce609-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ce609-124">Header files</span></span>

<span data-ttu-id="ce609-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce609-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce609-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ce609-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce609-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce609-127">See also</span></span>



[<span data-ttu-id="ce609-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ce609-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce609-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ce609-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce609-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ce609-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce609-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ce609-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

