---
title: Propriété canonique PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e24ae5f56a043d810eb805720606fd5b44d60cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786314"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="5ab0b-103">Propriété canonique PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5ab0b-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="5ab0b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ab0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ab0b-105">Contient l’adresse de messagerie du destinataire prévu à l’origine d’un message transféré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5ab0b-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ab0b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5ab0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ab0b-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="5ab0b-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="5ab0b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5ab0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ab0b-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="5ab0b-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="5ab0b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5ab0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ab0b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5ab0b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5ab0b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="5ab0b-112">Area:</span></span>  <br/> |<span data-ttu-id="5ab0b-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="5ab0b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ab0b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ab0b-114">Remarks</span></span>

<span data-ttu-id="5ab0b-115">Ces propriétés sont des exemples de propriétés d’adresse pour le destinataire du message à l’origine.</span><span class="sxs-lookup"><span data-stu-id="5ab0b-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="5ab0b-116">Il doivent être définies par l’agent automatique qui a transféré le message.</span><span class="sxs-lookup"><span data-stu-id="5ab0b-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="5ab0b-117">Ces propriétés correspondent à l’attribut par destinataire du rapport X.400.</span><span class="sxs-lookup"><span data-stu-id="5ab0b-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ab0b-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5ab0b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5ab0b-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5ab0b-119">Header files</span></span>

<span data-ttu-id="5ab0b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ab0b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ab0b-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5ab0b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ab0b-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5ab0b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5ab0b-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5ab0b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ab0b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ab0b-124">See also</span></span>



[<span data-ttu-id="5ab0b-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab0b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ab0b-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab0b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ab0b-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab0b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ab0b-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="5ab0b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

