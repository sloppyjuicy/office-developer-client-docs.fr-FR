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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356468"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="7520f-103">Propriété canonique PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="7520f-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="7520f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7520f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7520f-105">Contient la valeur TRUE si un expéditeur de message veut que le système de messagerie génère un rapport de lecture lorsque le destinataire a lu un message.</span><span class="sxs-lookup"><span data-stu-id="7520f-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7520f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7520f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7520f-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="7520f-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="7520f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7520f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7520f-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="7520f-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="7520f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7520f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7520f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7520f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7520f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7520f-112">Area:</span></span>  <br/> |<span data-ttu-id="7520f-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="7520f-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7520f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7520f-114">Remarks</span></span>

<span data-ttu-id="7520f-115">Cette propriété doit avoir la valeur TRUE pour valider les valeurs des propriétés **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) et **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7520f-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="7520f-116">Si un message avec **PR_READ_RECEIPT_REQUESTED** défini est supprimé ou expire avant que le système de messagerie puisse générer un rapport de lecture, un rapport non lu est généré.</span><span class="sxs-lookup"><span data-stu-id="7520f-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7520f-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="7520f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7520f-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7520f-118">Protocol specifications</span></span>

<span data-ttu-id="7520f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7520f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7520f-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="7520f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7520f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7520f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7520f-122">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="7520f-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7520f-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="7520f-123">Header files</span></span>

<span data-ttu-id="7520f-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7520f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7520f-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7520f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7520f-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7520f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7520f-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="7520f-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7520f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7520f-128">See also</span></span>



[<span data-ttu-id="7520f-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7520f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7520f-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7520f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7520f-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7520f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7520f-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7520f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

