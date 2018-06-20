---
title: Propriété canonique PidTagRecipientProposedEndTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f0310d8dcde9acc1e14f0be124543897e9867951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786536"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="3d264-103">Propriété canonique PidTagRecipientProposedEndTime</span><span class="sxs-lookup"><span data-stu-id="3d264-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="3d264-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d264-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d264-105">Indique une heure de fin proposée d’une réunion.</span><span class="sxs-lookup"><span data-stu-id="3d264-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d264-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3d264-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d264-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="3d264-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="3d264-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3d264-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d264-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="3d264-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="3d264-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3d264-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d264-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3d264-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3d264-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3d264-112">Area:</span></span>  <br/> |<span data-ttu-id="3d264-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="3d264-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d264-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d264-114">Remarks</span></span>

<span data-ttu-id="3d264-115">Lorsque la valeur de la propriété **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) est définie sur TRUE, la valeur de cette propriété indique la valeur demandée par le participant à définir comme valeur de la **dispidApptEndWhole** ([ PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) la propriété de l’objet de réunion d’instance unique ou d’un objet exception.</span><span class="sxs-lookup"><span data-stu-id="3d264-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d264-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3d264-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d264-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3d264-117">Protocol specifications</span></span>

<span data-ttu-id="3d264-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d264-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d264-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3d264-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d264-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d264-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d264-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="3d264-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d264-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3d264-122">Header files</span></span>

<span data-ttu-id="3d264-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d264-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d264-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3d264-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d264-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3d264-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3d264-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3d264-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d264-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d264-127">See also</span></span>



[<span data-ttu-id="3d264-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3d264-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d264-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3d264-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d264-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3d264-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d264-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3d264-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

