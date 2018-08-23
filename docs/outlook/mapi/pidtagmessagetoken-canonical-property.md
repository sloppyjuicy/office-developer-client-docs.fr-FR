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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6b5def94096f7664169935a062d3b28171fb2919
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578429"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="0c0e7-103">Propriété canonique PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="0c0e7-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="0c0e7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c0e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c0e7-105">Contient un jeton de sécurité ASN.1 pour un message.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c0e7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0c0e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c0e7-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="0c0e7-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="0c0e7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0c0e7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c0e7-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="0c0e7-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="0c0e7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0c0e7-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c0e7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0c0e7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0c0e7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0c0e7-112">Area:</span></span>  <br/> |<span data-ttu-id="0c0e7-113">Sécuriser les propriétés de messagerie</span><span class="sxs-lookup"><span data-stu-id="0c0e7-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c0e7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c0e7-114">Remarks</span></span>

<span data-ttu-id="0c0e7-115">Cette propriété véhicule protégées informations liées à la sécurité de son créateur à son destinataire.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="0c0e7-116">Conjointement avec la propriété **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), elle garantit association l’étiquette avec le contenu du message.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="0c0e7-117">Conjointement avec la propriété **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), il vérifie que le contenu du message est inchangé.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c0e7-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0c0e7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0c0e7-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0c0e7-119">Header files</span></span>

<span data-ttu-id="0c0e7-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c0e7-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c0e7-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c0e7-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0c0e7-122">Mapitags.h</span></span>
  
> <span data-ttu-id="0c0e7-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c0e7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c0e7-124">See also</span></span>



[<span data-ttu-id="0c0e7-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0c0e7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c0e7-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0c0e7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c0e7-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0c0e7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c0e7-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0c0e7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

