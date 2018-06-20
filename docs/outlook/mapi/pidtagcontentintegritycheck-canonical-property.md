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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2082db4ccd107fcd02e37882707e4e3ee697695d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785858"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="07b53-103">Propriété canonique PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="07b53-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="07b53-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07b53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07b53-105">Contient une valeur de vérification de l’intégrité du contenu ASN.1 qui permet à un expéditeur du message protéger le contenu des messages de divulgation à des destinataires non autorisés.</span><span class="sxs-lookup"><span data-stu-id="07b53-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07b53-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="07b53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07b53-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="07b53-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="07b53-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="07b53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07b53-109">0x0c00</span><span class="sxs-lookup"><span data-stu-id="07b53-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="07b53-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="07b53-110">Data type:</span></span>  <br/> |<span data-ttu-id="07b53-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="07b53-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="07b53-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="07b53-112">Area:</span></span>  <br/> |<span data-ttu-id="07b53-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="07b53-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07b53-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="07b53-114">Remarks</span></span>

<span data-ttu-id="07b53-115">Cette propriété fournit pour la non-répudiation du contenu du message.</span><span class="sxs-lookup"><span data-stu-id="07b53-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="07b53-116">Conjointement avec **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), elle garantit que le contenu d’un message arrive à sa destination inchangée.</span><span class="sxs-lookup"><span data-stu-id="07b53-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07b53-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="07b53-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="07b53-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="07b53-118">Header files</span></span>

<span data-ttu-id="07b53-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07b53-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="07b53-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="07b53-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="07b53-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="07b53-121">Mapitags.h</span></span>
  
> <span data-ttu-id="07b53-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="07b53-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07b53-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07b53-123">See also</span></span>



[<span data-ttu-id="07b53-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="07b53-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07b53-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="07b53-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07b53-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="07b53-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07b53-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="07b53-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

