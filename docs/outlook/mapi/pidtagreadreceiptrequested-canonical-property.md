---
title: Propriété canonique PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c0263b905e01a8937e2472d6e8c165287e7ebc5d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588047"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="30362-103">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="30362-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="30362-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30362-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30362-105">Contient la valeur TRUE si un expéditeur du message souhaite que le système de messagerie pour générer un rapport de lecture lorsque le destinataire a lu dans un message.</span><span class="sxs-lookup"><span data-stu-id="30362-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30362-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="30362-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30362-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="30362-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="30362-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="30362-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30362-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="30362-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="30362-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="30362-110">Data type:</span></span>  <br/> |<span data-ttu-id="30362-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="30362-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="30362-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="30362-112">Area:</span></span>  <br/> |<span data-ttu-id="30362-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="30362-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30362-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="30362-114">Remarks</span></span>

<span data-ttu-id="30362-115">Cette propriété doit être définie sur TRUE pour valider les valeurs des propriétés **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="30362-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="30362-116">Si un message avec **PR_READ_RECEIPT_REQUESTED** set est supprimé ou expire avant que le système de messagerie peut générer un rapport de lecture, un rapport nonread est généré.</span><span class="sxs-lookup"><span data-stu-id="30362-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="30362-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="30362-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30362-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="30362-118">Protocol specifications</span></span>

<span data-ttu-id="30362-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30362-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30362-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="30362-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30362-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30362-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30362-122">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="30362-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30362-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="30362-123">Header files</span></span>

<span data-ttu-id="30362-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30362-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="30362-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="30362-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="30362-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="30362-126">Mapitags.h</span></span>
  
> <span data-ttu-id="30362-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="30362-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30362-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30362-128">See also</span></span>



[<span data-ttu-id="30362-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="30362-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30362-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="30362-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30362-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="30362-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30362-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="30362-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

