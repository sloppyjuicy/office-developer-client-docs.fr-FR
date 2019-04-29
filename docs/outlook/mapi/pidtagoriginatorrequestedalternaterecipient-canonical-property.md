---
title: Propriété canonique PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437860"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="184ad-103">Propriété canonique PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="184ad-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="184ad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="184ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="184ad-105">Contient un identificateur d'entrée pour un autre destinataire désigné par l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="184ad-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="184ad-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="184ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="184ad-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="184ad-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="184ad-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="184ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="184ad-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="184ad-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="184ad-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="184ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="184ad-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="184ad-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="184ad-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="184ad-112">Area:</span></span>  <br/> |<span data-ttu-id="184ad-113">MIME</span><span class="sxs-lookup"><span data-stu-id="184ad-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="184ad-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="184ad-114">Remarks</span></span>

<span data-ttu-id="184ad-115">Cette propriété est utilisée dans les messages autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="184ad-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="184ad-116">Si le transfert d'autodirection n'est pas autorisé ou si aucun autre destinataire n'a été désigné, un rapport de non-remise doit être généré.</span><span class="sxs-lookup"><span data-stu-id="184ad-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="184ad-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="184ad-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="184ad-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="184ad-118">Header files</span></span>

<span data-ttu-id="184ad-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="184ad-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="184ad-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="184ad-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="184ad-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="184ad-121">Mapitags.h</span></span>
  
> <span data-ttu-id="184ad-122">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="184ad-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="184ad-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="184ad-123">See also</span></span>



[<span data-ttu-id="184ad-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="184ad-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="184ad-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="184ad-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="184ad-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="184ad-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="184ad-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="184ad-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

