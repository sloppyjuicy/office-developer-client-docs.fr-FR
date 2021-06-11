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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332773"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="65458-103">Propriété canonique PidTagRecipientProposedEndTime</span><span class="sxs-lookup"><span data-stu-id="65458-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="65458-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65458-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65458-105">Indique l’heure de fin proposée d’une réunion.</span><span class="sxs-lookup"><span data-stu-id="65458-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65458-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="65458-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65458-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="65458-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="65458-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="65458-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65458-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="65458-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="65458-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="65458-110">Data type:</span></span>  <br/> |<span data-ttu-id="65458-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="65458-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="65458-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="65458-112">Area:</span></span>  <br/> |<span data-ttu-id="65458-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="65458-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65458-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="65458-114">Remarks</span></span>

<span data-ttu-id="65458-115">Lorsque la valeur de la propriété **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) est définie sur TRUE, la valeur de cette propriété indique la valeur demandée par le participant à définir en tant que valeur de la propriété **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) pour l’objet de réunion ou d’exception d’instance unique.</span><span class="sxs-lookup"><span data-stu-id="65458-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="65458-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="65458-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65458-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="65458-117">Protocol specifications</span></span>

<span data-ttu-id="65458-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65458-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65458-119">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="65458-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="65458-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65458-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65458-121">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="65458-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65458-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="65458-122">Header files</span></span>

<span data-ttu-id="65458-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65458-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="65458-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="65458-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="65458-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="65458-125">Mapitags.h</span></span>
  
> <span data-ttu-id="65458-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="65458-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65458-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65458-127">See also</span></span>



[<span data-ttu-id="65458-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="65458-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65458-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="65458-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65458-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="65458-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65458-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="65458-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

