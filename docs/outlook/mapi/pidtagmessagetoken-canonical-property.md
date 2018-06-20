---
title: Propriété canonique PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786246"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="3a784-103">Propriété canonique PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="3a784-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="3a784-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a784-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a784-105">Contient un jeton de sécurité ASN.1 pour un message.</span><span class="sxs-lookup"><span data-stu-id="3a784-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a784-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3a784-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a784-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="3a784-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="3a784-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3a784-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3a784-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="3a784-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="3a784-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3a784-110">Data type:</span></span>  <br/> |<span data-ttu-id="3a784-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3a784-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3a784-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3a784-112">Area:</span></span>  <br/> |<span data-ttu-id="3a784-113">Sécuriser les propriétés de messagerie</span><span class="sxs-lookup"><span data-stu-id="3a784-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a784-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a784-114">Remarks</span></span>

<span data-ttu-id="3a784-115">Cette propriété véhicule protégées informations liées à la sécurité de son créateur à son destinataire.</span><span class="sxs-lookup"><span data-stu-id="3a784-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="3a784-116">Conjointement avec la propriété **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), elle garantit association l’étiquette avec le contenu du message.</span><span class="sxs-lookup"><span data-stu-id="3a784-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="3a784-117">Conjointement avec la propriété **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), il vérifie que le contenu du message est inchangé.</span><span class="sxs-lookup"><span data-stu-id="3a784-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3a784-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3a784-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3a784-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3a784-119">Header files</span></span>

<span data-ttu-id="3a784-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a784-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a784-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3a784-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="3a784-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3a784-122">Mapitags.h</span></span>
  
> <span data-ttu-id="3a784-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3a784-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a784-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a784-124">See also</span></span>



[<span data-ttu-id="3a784-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3a784-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a784-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3a784-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a784-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3a784-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a784-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3a784-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

