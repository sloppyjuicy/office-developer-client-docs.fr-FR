---
title: Propriété canonique PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435277"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="50bad-103">Propriété canonique PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="50bad-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="50bad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50bad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50bad-105">Contient la date et l’heure de livraison du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="50bad-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50bad-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="50bad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50bad-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="50bad-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="50bad-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="50bad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50bad-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="50bad-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="50bad-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="50bad-110">Data type:</span></span>  <br/> |<span data-ttu-id="50bad-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="50bad-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="50bad-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="50bad-112">Area:</span></span>  <br/> |<span data-ttu-id="50bad-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="50bad-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50bad-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="50bad-114">Remarks</span></span>

<span data-ttu-id="50bad-115">Cette propriété est une propriété par destinataire d’un état de remise qui indique l’heure à laquelle le message d’origine a été remis à l’utilisateur de messagerie pour lequel la rapport de remise est généré.</span><span class="sxs-lookup"><span data-stu-id="50bad-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50bad-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="50bad-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="50bad-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="50bad-117">Header files</span></span>

<span data-ttu-id="50bad-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50bad-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="50bad-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="50bad-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="50bad-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="50bad-120">Mapitags.h</span></span>
  
> <span data-ttu-id="50bad-121">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="50bad-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50bad-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50bad-122">See also</span></span>



[<span data-ttu-id="50bad-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="50bad-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="50bad-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="50bad-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50bad-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="50bad-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50bad-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="50bad-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50bad-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="50bad-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

