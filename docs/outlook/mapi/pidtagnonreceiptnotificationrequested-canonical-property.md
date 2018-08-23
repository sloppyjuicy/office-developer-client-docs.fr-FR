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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 896cfa2bf8a1b33fd6dee09649853b71618f31be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582783"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="5e438-103">Propriété canonique PidTagNonReceiptNotificationRequested</span><span class="sxs-lookup"><span data-stu-id="5e438-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="5e438-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e438-105">Contient la valeur TRUE si un expéditeur du message veut notification de non-réception pour un destinataire spécifié.</span><span class="sxs-lookup"><span data-stu-id="5e438-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e438-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5e438-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e438-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="5e438-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="5e438-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5e438-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e438-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="5e438-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="5e438-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5e438-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e438-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5e438-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5e438-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5e438-112">Area:</span></span>  <br/> |<span data-ttu-id="5e438-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="5e438-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e438-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e438-114">Remarks</span></span>

<span data-ttu-id="5e438-115">Si cette propriété contient la valeur FALSE et la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) contient la valeur TRUE, le fournisseur de services peut remplacer la propriété **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** et générer un rapport de non-remise.</span><span class="sxs-lookup"><span data-stu-id="5e438-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e438-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5e438-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5e438-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5e438-117">Header files</span></span>

<span data-ttu-id="5e438-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e438-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e438-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5e438-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e438-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5e438-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5e438-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5e438-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e438-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e438-122">See also</span></span>



[<span data-ttu-id="5e438-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5e438-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e438-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5e438-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e438-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5e438-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e438-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5e438-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

