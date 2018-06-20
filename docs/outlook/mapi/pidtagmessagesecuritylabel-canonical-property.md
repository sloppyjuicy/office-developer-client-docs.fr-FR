---
title: Propriété canonique PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786235"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="26c4f-103">Propriété canonique PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="26c4f-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="26c4f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26c4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26c4f-105">Contient une étiquette de sécurité pour un message.</span><span class="sxs-lookup"><span data-stu-id="26c4f-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26c4f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="26c4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26c4f-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="26c4f-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="26c4f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="26c4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26c4f-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="26c4f-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="26c4f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="26c4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="26c4f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="26c4f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="26c4f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="26c4f-112">Area:</span></span>  <br/> |<span data-ttu-id="26c4f-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="26c4f-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26c4f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="26c4f-114">Remarks</span></span>

<span data-ttu-id="26c4f-115">Cette propriété fournit la base sur laquelle la propriété **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protège un message.</span><span class="sxs-lookup"><span data-stu-id="26c4f-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="26c4f-116">L’association avec le contenu du message est garantie par le jeton.</span><span class="sxs-lookup"><span data-stu-id="26c4f-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26c4f-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="26c4f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="26c4f-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="26c4f-118">Header files</span></span>

<span data-ttu-id="26c4f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26c4f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="26c4f-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="26c4f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="26c4f-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="26c4f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="26c4f-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="26c4f-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26c4f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c4f-123">See also</span></span>



[<span data-ttu-id="26c4f-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="26c4f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26c4f-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="26c4f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26c4f-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="26c4f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26c4f-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="26c4f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

