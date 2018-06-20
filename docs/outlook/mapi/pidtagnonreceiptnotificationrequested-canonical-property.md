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
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786267"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="ed244-103">Propriété canonique PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="ed244-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="ed244-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed244-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed244-105">Contient la valeur TRUE si un expéditeur du message veut notification de non-réception pour un destinataire spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed244-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed244-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ed244-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed244-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="ed244-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="ed244-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ed244-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed244-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="ed244-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="ed244-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ed244-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed244-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ed244-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ed244-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ed244-112">Area:</span></span>  <br/> |<span data-ttu-id="ed244-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="ed244-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed244-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed244-114">Remarks</span></span>

<span data-ttu-id="ed244-115">Si cette propriété contient la valeur FALSE et la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contient la valeur TRUE, le fournisseur de services peut remplacer la propriété **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** et générer un rapport de non-remise.</span><span class="sxs-lookup"><span data-stu-id="ed244-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed244-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ed244-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ed244-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ed244-117">Header files</span></span>

<span data-ttu-id="ed244-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed244-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed244-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ed244-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed244-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ed244-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ed244-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ed244-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed244-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed244-122">See also</span></span>



[<span data-ttu-id="ed244-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ed244-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed244-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ed244-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed244-125">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ed244-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed244-126">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ed244-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

