---
title: Propriété canonique PidTagRecipientProposedStartTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8815728adce809641586c4da5beb4c9fad735507
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397113"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="8b994-103">Propriété canonique PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="8b994-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="8b994-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b994-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b994-105">Indique une heure de début d’une réunion.</span><span class="sxs-lookup"><span data-stu-id="8b994-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b994-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8b994-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b994-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="8b994-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="8b994-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8b994-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b994-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="8b994-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="8b994-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8b994-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b994-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8b994-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8b994-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8b994-112">Area:</span></span>  <br/> |<span data-ttu-id="8b994-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="8b994-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b994-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b994-114">Remarks</span></span>

<span data-ttu-id="8b994-115">Lorsque la valeur de la propriété **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) est définie sur TRUE, la valeur de cette propriété indique la valeur demandée par le participant à définir comme valeur de la **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) la propriété de l’objet de réunion d’instance unique ou d’un objet exception.</span><span class="sxs-lookup"><span data-stu-id="8b994-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b994-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8b994-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b994-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8b994-117">Protocol specifications</span></span>

<span data-ttu-id="8b994-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b994-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b994-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8b994-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b994-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b994-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b994-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="8b994-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b994-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8b994-122">Header files</span></span>

<span data-ttu-id="8b994-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b994-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b994-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8b994-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b994-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8b994-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8b994-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8b994-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b994-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b994-127">See also</span></span>



[<span data-ttu-id="8b994-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8b994-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b994-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8b994-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b994-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8b994-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b994-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8b994-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

