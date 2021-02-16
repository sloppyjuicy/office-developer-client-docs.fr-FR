---
title: Propriété canonique PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 596e416624fb6f2bf1fdaef64c2179feb7787815
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431413"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="8e14e-103">Propriété canonique PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="8e14e-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="8e14e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e14e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e14e-105">Contient le type d’adresse de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou de répondre.</span><span class="sxs-lookup"><span data-stu-id="8e14e-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e14e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8e14e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e14e-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="8e14e-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="8e14e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8e14e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e14e-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="8e14e-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="8e14e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8e14e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e14e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e14e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8e14e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8e14e-112">Area:</span></span>  <br/> |<span data-ttu-id="8e14e-113">Server</span><span class="sxs-lookup"><span data-stu-id="8e14e-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e14e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e14e-114">Remarks</span></span>

<span data-ttu-id="8e14e-115">Ces propriétés sont des exemples de propriétés d’adresse pour l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="8e14e-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="8e14e-116">Lors de la première soumission du message, l’application cliente doit définir cette propriété sur la valeur de la propriété **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e14e-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="8e14e-117">Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.</span><span class="sxs-lookup"><span data-stu-id="8e14e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="8e14e-118">Les propriétés d’auteur d’origine permettent la conservation des informations en dehors du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="8e14e-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="8e14e-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tel qu’Internet, ces propriétés permettent de s’assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="8e14e-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e14e-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8e14e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8e14e-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8e14e-121">Header files</span></span>

<span data-ttu-id="8e14e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e14e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e14e-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8e14e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e14e-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e14e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8e14e-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="8e14e-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e14e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e14e-126">See also</span></span>



[<span data-ttu-id="8e14e-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8e14e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e14e-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8e14e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e14e-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8e14e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e14e-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8e14e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

