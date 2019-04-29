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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411371"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="79864-103">Propriété canonique PidTagOriginallyIntendedRecipEmailAddress</span><span class="sxs-lookup"><span data-stu-id="79864-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="79864-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79864-105">Contient l'adresse de messagerie du destinataire initial d'un message autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="79864-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79864-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="79864-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79864-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="79864-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="79864-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="79864-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79864-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="79864-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="79864-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="79864-110">Data type:</span></span>  <br/> |<span data-ttu-id="79864-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="79864-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="79864-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="79864-112">Area:</span></span>  <br/> |<span data-ttu-id="79864-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="79864-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79864-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="79864-114">Remarks</span></span>

<span data-ttu-id="79864-115">Ces propriétés sont des exemples de propriétés d'adresse pour le destinataire du message initialement prévu.</span><span class="sxs-lookup"><span data-stu-id="79864-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="79864-116">Elles doivent être définies par l'agent automatique qui a transféré le message.</span><span class="sxs-lookup"><span data-stu-id="79864-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="79864-117">Ces propriétés correspondent à l'attribut par destinataire du rapport X. 400.</span><span class="sxs-lookup"><span data-stu-id="79864-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="79864-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="79864-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="79864-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="79864-119">Header files</span></span>

<span data-ttu-id="79864-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="79864-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="79864-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="79864-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="79864-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="79864-122">Mapitags.h</span></span>
  
> <span data-ttu-id="79864-123">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="79864-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79864-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79864-124">See also</span></span>



[<span data-ttu-id="79864-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="79864-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79864-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="79864-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79864-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="79864-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79864-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="79864-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

