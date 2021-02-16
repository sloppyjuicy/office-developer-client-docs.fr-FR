---
title: Propriété canonique PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355775"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="f050c-103">Propriété canonique PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="f050c-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="f050c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f050c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f050c-105">Contient le nom complet de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou de répondre.</span><span class="sxs-lookup"><span data-stu-id="f050c-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f050c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f050c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f050c-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f050c-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f050c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f050c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f050c-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="f050c-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="f050c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f050c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f050c-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="f050c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="f050c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f050c-112">Area:</span></span>  <br/> |<span data-ttu-id="f050c-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="f050c-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f050c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f050c-114">Remarks</span></span>

<span data-ttu-id="f050c-115">Ces propriétés sont des exemples de propriétés d’adresse pour l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="f050c-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="f050c-116">Lors de la première soumission du message, l’application cliente doit définir ces propriétés sur la valeur **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f050c-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="f050c-117">Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.</span><span class="sxs-lookup"><span data-stu-id="f050c-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="f050c-118">Les propriétés d’auteur d’origine permettent la conservation des informations en dehors du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="f050c-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="f050c-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tel qu’Internet, ces propriétés permettent de s’assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="f050c-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f050c-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f050c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f050c-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f050c-121">Protocol specifications</span></span>

<span data-ttu-id="f050c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f050c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f050c-123">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="f050c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f050c-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f050c-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f050c-125">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="f050c-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f050c-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f050c-126">Header files</span></span>

<span data-ttu-id="f050c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f050c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f050c-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f050c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f050c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f050c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f050c-130">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="f050c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f050c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f050c-131">See also</span></span>



[<span data-ttu-id="f050c-132">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="f050c-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="f050c-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f050c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f050c-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f050c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f050c-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f050c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f050c-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f050c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

