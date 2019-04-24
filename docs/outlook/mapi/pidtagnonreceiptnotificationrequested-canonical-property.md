---
title: Propriété canonique PidTagNonReceiptNotificationRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329308"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="678db-103">Propriété canonique PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="678db-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="678db-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="678db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="678db-105">Contient la valeur TRUE si l'expéditeur d'un message souhaite être averti de la non-réception d'un destinataire spécifié.</span><span class="sxs-lookup"><span data-stu-id="678db-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="678db-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="678db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="678db-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="678db-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="678db-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="678db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="678db-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="678db-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="678db-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="678db-110">Data type:</span></span>  <br/> |<span data-ttu-id="678db-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="678db-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="678db-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="678db-112">Area:</span></span>  <br/> |<span data-ttu-id="678db-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="678db-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="678db-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="678db-114">Remarks</span></span>

<span data-ttu-id="678db-115">Si cette propriété contient la valeur FALSe et que la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contient la valeur true, le fournisseur de services peut remplacer la propriété **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** et générer une notification d'échec de remise.</span><span class="sxs-lookup"><span data-stu-id="678db-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="678db-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="678db-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="678db-117">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="678db-117">Header files</span></span>

<span data-ttu-id="678db-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="678db-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="678db-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="678db-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="678db-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="678db-120">Mapitags.h</span></span>
  
> <span data-ttu-id="678db-121">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="678db-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="678db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="678db-122">See also</span></span>



[<span data-ttu-id="678db-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="678db-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="678db-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="678db-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="678db-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="678db-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="678db-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="678db-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

