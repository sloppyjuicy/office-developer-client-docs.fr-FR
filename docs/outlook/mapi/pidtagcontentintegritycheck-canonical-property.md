---
title: Propriété canonique PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415725"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="f4fdf-103">Propriété canonique PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="f4fdf-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="f4fdf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4fdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4fdf-105">Contient une valeur de vérification de l’intégrité du contenu ASN.1 qui permet à un expéditeur de message de protéger le contenu du message contre la divulgation à des destinataires non autorisés.</span><span class="sxs-lookup"><span data-stu-id="f4fdf-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4fdf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f4fdf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4fdf-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="f4fdf-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="f4fdf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f4fdf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4fdf-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="f4fdf-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="f4fdf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f4fdf-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4fdf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f4fdf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f4fdf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f4fdf-112">Area:</span></span>  <br/> |<span data-ttu-id="f4fdf-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f4fdf-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4fdf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4fdf-114">Remarks</span></span>

<span data-ttu-id="f4fdf-115">Cette propriété permet de ne pas répudier le contenu des messages.</span><span class="sxs-lookup"><span data-stu-id="f4fdf-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="f4fdf-116">Conjointement **avec PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), il garantit que le contenu d’un message arrive à sa destination inchangée.</span><span class="sxs-lookup"><span data-stu-id="f4fdf-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4fdf-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f4fdf-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f4fdf-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f4fdf-118">Header files</span></span>

<span data-ttu-id="f4fdf-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4fdf-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4fdf-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f4fdf-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4fdf-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4fdf-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f4fdf-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="f4fdf-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4fdf-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4fdf-123">See also</span></span>



[<span data-ttu-id="f4fdf-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f4fdf-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4fdf-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f4fdf-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4fdf-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f4fdf-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4fdf-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f4fdf-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

