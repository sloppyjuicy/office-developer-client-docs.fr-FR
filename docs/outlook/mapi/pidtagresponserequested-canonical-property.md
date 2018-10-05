---
title: Propriété canonique PidTagResponseRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396742"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="e37c1-103">Propriété canonique PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="e37c1-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="e37c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e37c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e37c1-105">Contient la valeur TRUE si l’expéditeur du message souhaite une réponse à une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="e37c1-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e37c1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e37c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e37c1-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="e37c1-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="e37c1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e37c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e37c1-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="e37c1-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="e37c1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e37c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="e37c1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e37c1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e37c1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e37c1-112">Area:</span></span>  <br/> |<span data-ttu-id="e37c1-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="e37c1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e37c1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e37c1-114">Remarks</span></span>

<span data-ttu-id="e37c1-115">Cette propriété est utilisée pour les demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="e37c1-115">This property is used for meeting requests.</span></span> <span data-ttu-id="e37c1-116">L’application client destinataire doit inviter l’utilisateur à accepter ou refuser la demande, puis envoyer cette réponse à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="e37c1-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e37c1-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e37c1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e37c1-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e37c1-118">Protocol specifications</span></span>

<span data-ttu-id="e37c1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e37c1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e37c1-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="e37c1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e37c1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e37c1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e37c1-122">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="e37c1-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="e37c1-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e37c1-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e37c1-124">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="e37c1-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="e37c1-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e37c1-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e37c1-126">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="e37c1-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e37c1-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e37c1-127">Header files</span></span>

<span data-ttu-id="e37c1-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e37c1-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e37c1-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e37c1-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="e37c1-130">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e37c1-130">Mapitags.h</span></span>
  
> <span data-ttu-id="e37c1-131">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e37c1-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e37c1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e37c1-132">See also</span></span>



[<span data-ttu-id="e37c1-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e37c1-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e37c1-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e37c1-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e37c1-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e37c1-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e37c1-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e37c1-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

