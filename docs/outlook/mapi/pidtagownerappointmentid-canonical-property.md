---
title: Propriété canonique PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386046"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="f750d-103">Propriété canonique PidTagOwnerAppointmentId</span><span class="sxs-lookup"><span data-stu-id="f750d-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="f750d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f750d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f750d-105">Contient un identificateur pour un rendez-vous du calendrier du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="f750d-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f750d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f750d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f750d-107">PROPRIÉTÉ PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="f750d-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="f750d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f750d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f750d-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="f750d-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="f750d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f750d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f750d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f750d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f750d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f750d-112">Area:</span></span>  <br/> |<span data-ttu-id="f750d-113">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="f750d-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f750d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f750d-114">Remarks</span></span>

<span data-ttu-id="f750d-115">Cette propriété est utilisée dans les demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="f750d-115">This property is used in meeting requests.</span></span> <span data-ttu-id="f750d-116">Il ne représente pas un identificateur d’entrée, mais un entier long qui identifie de manière unique le rendez-vous au sein de la planification de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="f750d-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f750d-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f750d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f750d-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f750d-118">Protocol specifications</span></span>

<span data-ttu-id="f750d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f750d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f750d-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f750d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f750d-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f750d-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f750d-122">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="f750d-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f750d-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f750d-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f750d-124">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="f750d-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="f750d-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f750d-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f750d-126">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="f750d-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f750d-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f750d-127">Header files</span></span>

<span data-ttu-id="f750d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f750d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f750d-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f750d-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="f750d-130">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f750d-130">mapitags.h</span></span>
  
> <span data-ttu-id="f750d-131">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="f750d-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f750d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f750d-132">See also</span></span>



[<span data-ttu-id="f750d-133">Propriété canonique PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="f750d-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="f750d-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f750d-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f750d-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f750d-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f750d-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f750d-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f750d-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f750d-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

