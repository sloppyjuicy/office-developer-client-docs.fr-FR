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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357721"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="ea3db-103">Propriété canonique PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="ea3db-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="ea3db-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea3db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea3db-105">Contient la date et l'heure auxquelles le message d'origine a été remis.</span><span class="sxs-lookup"><span data-stu-id="ea3db-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea3db-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ea3db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea3db-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="ea3db-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="ea3db-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ea3db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea3db-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="ea3db-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="ea3db-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ea3db-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea3db-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ea3db-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ea3db-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ea3db-112">Area:</span></span>  <br/> |<span data-ttu-id="ea3db-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="ea3db-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea3db-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea3db-114">Remarks</span></span>

<span data-ttu-id="ea3db-115">Cette propriété est une propriété par destinataire dans un rapport de remise qui indique l'heure à laquelle le message d'origine a été remis à l'utilisateur de messagerie pour lequel le rapport de remise est généré.</span><span class="sxs-lookup"><span data-stu-id="ea3db-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea3db-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="ea3db-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ea3db-117">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="ea3db-117">Header files</span></span>

<span data-ttu-id="ea3db-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ea3db-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea3db-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ea3db-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea3db-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ea3db-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ea3db-121">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="ea3db-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea3db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea3db-122">See also</span></span>



[<span data-ttu-id="ea3db-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="ea3db-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="ea3db-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ea3db-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea3db-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ea3db-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea3db-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ea3db-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea3db-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ea3db-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

