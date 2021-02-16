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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 036f38c1228e08cfc9a2093c027195a802904f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358834"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="01d80-103">Propriété canonique PidTagInReplyToId</span><span class="sxs-lookup"><span data-stu-id="01d80-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="01d80-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01d80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01d80-105">Contient la valeur de la **propriété PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="01d80-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01d80-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="01d80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01d80-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="01d80-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="01d80-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="01d80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01d80-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="01d80-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="01d80-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="01d80-110">Data type:</span></span>  <br/> |<span data-ttu-id="01d80-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="01d80-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="01d80-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="01d80-112">Area:</span></span>  <br/> |<span data-ttu-id="01d80-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="01d80-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01d80-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="01d80-114">Remarks</span></span>

<span data-ttu-id="01d80-115">Ces propriétés doivent être définies sur toutes les réponses de message.</span><span class="sxs-lookup"><span data-stu-id="01d80-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="01d80-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="01d80-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01d80-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="01d80-117">Protocol specifications</span></span>

<span data-ttu-id="01d80-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01d80-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01d80-119">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="01d80-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01d80-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01d80-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01d80-121">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="01d80-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="01d80-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01d80-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01d80-123">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="01d80-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01d80-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="01d80-124">Header files</span></span>

<span data-ttu-id="01d80-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01d80-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="01d80-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="01d80-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="01d80-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01d80-127">Mapitags.h</span></span>
  
> <span data-ttu-id="01d80-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="01d80-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01d80-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d80-129">See also</span></span>



[<span data-ttu-id="01d80-130">Propriété canonique PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="01d80-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="01d80-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="01d80-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01d80-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="01d80-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01d80-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="01d80-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01d80-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="01d80-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

