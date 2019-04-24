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
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360759"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="c1b49-103">Propriété canonique PidTagTransportMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="c1b49-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="c1b49-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1b49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1b49-105">Contient des informations d'enveloppe de message propres au transport.</span><span class="sxs-lookup"><span data-stu-id="c1b49-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1b49-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c1b49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1b49-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="c1b49-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="c1b49-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c1b49-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1b49-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="c1b49-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="c1b49-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c1b49-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1b49-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1b49-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c1b49-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c1b49-112">Area:</span></span>  <br/> |<span data-ttu-id="c1b49-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="c1b49-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1b49-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1b49-114">Remarks</span></span>

<span data-ttu-id="c1b49-115">Le fournisseur de transport peut générer les informations d'en-tête de message pour les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="c1b49-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="c1b49-116">Ces propriétés offrent une alternative à la possibilité d'ignorer les informations d'en-tête de message de transport ou de l'en faire glisser vers le texte du message.</span><span class="sxs-lookup"><span data-stu-id="c1b49-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="c1b49-117">Le client peut choisir d'afficher ou non les informations.</span><span class="sxs-lookup"><span data-stu-id="c1b49-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c1b49-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="c1b49-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1b49-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c1b49-119">Protocol specifications</span></span>

<span data-ttu-id="c1b49-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b49-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b49-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="c1b49-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1b49-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b49-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b49-123">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="c1b49-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="c1b49-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b49-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b49-125">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="c1b49-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1b49-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="c1b49-126">Header files</span></span>

<span data-ttu-id="c1b49-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c1b49-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1b49-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c1b49-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1b49-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c1b49-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c1b49-130">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="c1b49-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1b49-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b49-131">See also</span></span>



[<span data-ttu-id="c1b49-132">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="c1b49-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="c1b49-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c1b49-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1b49-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c1b49-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1b49-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c1b49-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1b49-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c1b49-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

