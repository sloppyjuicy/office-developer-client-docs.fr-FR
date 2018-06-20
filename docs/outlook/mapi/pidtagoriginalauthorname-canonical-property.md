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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786295"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="c1a18-103">Propriété canonique PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="c1a18-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="c1a18-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1a18-105">Contient le nom complet de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="c1a18-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1a18-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c1a18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1a18-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="c1a18-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c1a18-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c1a18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1a18-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="c1a18-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="c1a18-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c1a18-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1a18-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c1a18-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c1a18-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c1a18-112">Area:</span></span>  <br/> |<span data-ttu-id="c1a18-113">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="c1a18-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1a18-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1a18-114">Remarks</span></span>

<span data-ttu-id="c1a18-115">Ces propriétés sont des exemples de propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="c1a18-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="c1a18-116">Au premier envoi du message, l’application cliente doit définir ces propriétés à la valeur de **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c1a18-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="c1a18-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="c1a18-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="c1a18-118">Les propriétés de l’auteur d’origine autoriser pour la conservation des informations à partir de l’extérieur du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="c1a18-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="c1a18-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels qu’à partir d’Internet, ces propriétés fournissent un moyen pour vous assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="c1a18-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c1a18-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c1a18-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1a18-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c1a18-121">Protocol specifications</span></span>

<span data-ttu-id="c1a18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a18-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a18-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c1a18-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1a18-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a18-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a18-125">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="c1a18-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1a18-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c1a18-126">Header files</span></span>

<span data-ttu-id="c1a18-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1a18-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1a18-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c1a18-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1a18-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c1a18-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c1a18-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c1a18-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1a18-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a18-131">See also</span></span>



[<span data-ttu-id="c1a18-132">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="c1a18-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="c1a18-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a18-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1a18-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a18-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1a18-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a18-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1a18-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c1a18-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

