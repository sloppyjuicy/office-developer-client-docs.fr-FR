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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 463f2eb6e730c9250861ce50515a7f662bb75d23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588866"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="84bfe-103">Propriété canonique PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="84bfe-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="84bfe-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84bfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84bfe-105">Contient un identificateur d’entrée pour un autre destinataire désigné par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="84bfe-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84bfe-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="84bfe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84bfe-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="84bfe-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="84bfe-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="84bfe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84bfe-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="84bfe-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="84bfe-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="84bfe-110">Data type:</span></span>  <br/> |<span data-ttu-id="84bfe-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="84bfe-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="84bfe-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="84bfe-112">Area:</span></span>  <br/> |<span data-ttu-id="84bfe-113">MIME</span><span class="sxs-lookup"><span data-stu-id="84bfe-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84bfe-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="84bfe-114">Remarks</span></span>

<span data-ttu-id="84bfe-115">Cette propriété est utilisée dans les messages transféré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="84bfe-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="84bfe-116">Si le transfert automatique n’est pas autorisée ou si aucune autre destinataire n’a été désigné, un rapport de non-remise doit être généré.</span><span class="sxs-lookup"><span data-stu-id="84bfe-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84bfe-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="84bfe-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="84bfe-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="84bfe-118">Header files</span></span>

<span data-ttu-id="84bfe-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84bfe-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="84bfe-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="84bfe-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="84bfe-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="84bfe-121">Mapitags.h</span></span>
  
> <span data-ttu-id="84bfe-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="84bfe-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84bfe-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84bfe-123">See also</span></span>



[<span data-ttu-id="84bfe-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="84bfe-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84bfe-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="84bfe-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84bfe-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="84bfe-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84bfe-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="84bfe-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

