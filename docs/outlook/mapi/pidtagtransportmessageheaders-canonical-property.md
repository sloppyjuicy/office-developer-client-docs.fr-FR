---
title: Propriété canonique PidTagTransportMessageHeaders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e184fd0933295984af97258d785df92306160a6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786924"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="6e026-103">Propriété canonique PidTagTransportMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="6e026-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="6e026-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e026-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e026-105">Contient des informations d’enveloppe de message de transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="6e026-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e026-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6e026-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e026-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="6e026-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="6e026-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6e026-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e026-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="6e026-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="6e026-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6e026-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e026-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e026-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6e026-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6e026-112">Area:</span></span>  <br/> |<span data-ttu-id="6e026-113">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="6e026-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e026-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e026-114">Remarks</span></span>

<span data-ttu-id="6e026-115">Le fournisseur de transport peut générer les informations d’en-tête de message pour les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="6e026-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="6e026-116">Ces propriétés offrent une alternative doivent précéder au texte du message ou en supprimant les informations d’en-tête de message transport.</span><span class="sxs-lookup"><span data-stu-id="6e026-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="6e026-117">Le client peut choisir s’il faut afficher les informations.</span><span class="sxs-lookup"><span data-stu-id="6e026-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e026-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6e026-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e026-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6e026-119">Protocol specifications</span></span>

<span data-ttu-id="6e026-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e026-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e026-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6e026-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e026-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e026-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e026-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="6e026-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="6e026-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e026-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e026-125">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="6e026-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e026-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6e026-126">Header files</span></span>

<span data-ttu-id="6e026-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e026-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e026-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6e026-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e026-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6e026-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6e026-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6e026-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e026-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e026-131">See also</span></span>



[<span data-ttu-id="6e026-132">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="6e026-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="6e026-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6e026-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e026-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6e026-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e026-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6e026-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e026-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6e026-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

