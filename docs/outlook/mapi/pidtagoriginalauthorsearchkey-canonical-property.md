---
title: Propriété canonique PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409579"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="97133-103">Propriété canonique PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="97133-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="97133-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97133-105">Contient la clé de recherche de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou de répondre.</span><span class="sxs-lookup"><span data-stu-id="97133-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97133-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="97133-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97133-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="97133-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="97133-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="97133-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97133-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="97133-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="97133-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="97133-110">Data type:</span></span>  <br/> |<span data-ttu-id="97133-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="97133-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="97133-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="97133-112">Area:</span></span>  <br/> |<span data-ttu-id="97133-113">Server</span><span class="sxs-lookup"><span data-stu-id="97133-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97133-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="97133-114">Remarks</span></span>

<span data-ttu-id="97133-115">Cette propriété est l’une des propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="97133-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="97133-116">Lors de la première soumission du message, l’application cliente doit définir cette propriété sur la valeur de la **propriété PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey.](pidtagsendersearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="97133-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="97133-117">Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.</span><span class="sxs-lookup"><span data-stu-id="97133-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="97133-118">Les propriétés d’auteur d’origine permettent la conservation des informations en dehors du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="97133-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="97133-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tel qu’Internet, ces propriétés permettent de s’assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="97133-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97133-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="97133-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="97133-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="97133-121">Header files</span></span>

<span data-ttu-id="97133-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97133-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="97133-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="97133-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="97133-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97133-124">Mapitags.h</span></span>
  
> <span data-ttu-id="97133-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="97133-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97133-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97133-126">See also</span></span>



[<span data-ttu-id="97133-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="97133-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97133-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="97133-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97133-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="97133-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97133-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="97133-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

