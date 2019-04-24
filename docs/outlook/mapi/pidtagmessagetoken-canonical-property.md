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
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355803"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="3c04d-103">Propriété canonique PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="3c04d-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="3c04d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c04d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c04d-105">Contient un jeton de sécurité ASN. 1 pour un message.</span><span class="sxs-lookup"><span data-stu-id="3c04d-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c04d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3c04d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c04d-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="3c04d-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="3c04d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3c04d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c04d-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="3c04d-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="3c04d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3c04d-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c04d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c04d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3c04d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3c04d-112">Area:</span></span>  <br/> |<span data-ttu-id="3c04d-113">Propriétés de la messagerie sécurisée</span><span class="sxs-lookup"><span data-stu-id="3c04d-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c04d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c04d-114">Remarks</span></span>

<span data-ttu-id="3c04d-115">Cette propriété transmet les informations de sécurité protégées de son expéditeur à son destinataire.</span><span class="sxs-lookup"><span data-stu-id="3c04d-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="3c04d-116">En association avec la propriété **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), elle garantit l'Association de l'étiquette au contenu du message.</span><span class="sxs-lookup"><span data-stu-id="3c04d-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="3c04d-117">En combinaison avec la propriété **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), il vérifie que le contenu du message n'est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="3c04d-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c04d-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="3c04d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3c04d-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="3c04d-119">Header files</span></span>

<span data-ttu-id="3c04d-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3c04d-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c04d-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3c04d-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c04d-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3c04d-122">Mapitags.h</span></span>
  
> <span data-ttu-id="3c04d-123">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3c04d-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c04d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c04d-124">See also</span></span>



[<span data-ttu-id="3c04d-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3c04d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c04d-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3c04d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c04d-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3c04d-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c04d-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3c04d-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

