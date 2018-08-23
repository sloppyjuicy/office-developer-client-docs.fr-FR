---
title: Propriété canonique PidTagInReplyToId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6f3ae69243da185430836903da9e7b0644c5db90
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594781"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="40c7b-103">Propriété canonique PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="40c7b-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="40c7b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40c7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40c7b-105">Contient la valeur de la propriété **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="40c7b-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40c7b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="40c7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40c7b-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="40c7b-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="40c7b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="40c7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40c7b-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="40c7b-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="40c7b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="40c7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="40c7b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40c7b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40c7b-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="40c7b-112">Area:</span></span>  <br/> |<span data-ttu-id="40c7b-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="40c7b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40c7b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="40c7b-114">Remarks</span></span>

<span data-ttu-id="40c7b-115">Ces propriétés doivent être définies sur tous les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="40c7b-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40c7b-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="40c7b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40c7b-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="40c7b-117">Protocol specifications</span></span>

<span data-ttu-id="40c7b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40c7b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40c7b-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="40c7b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40c7b-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40c7b-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40c7b-121">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="40c7b-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="40c7b-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40c7b-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40c7b-123">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="40c7b-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40c7b-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="40c7b-124">Header files</span></span>

<span data-ttu-id="40c7b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40c7b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="40c7b-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="40c7b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="40c7b-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="40c7b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="40c7b-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="40c7b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40c7b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40c7b-129">See also</span></span>



[<span data-ttu-id="40c7b-130">Propriété canonique PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="40c7b-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="40c7b-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="40c7b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40c7b-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="40c7b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40c7b-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="40c7b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40c7b-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="40c7b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

