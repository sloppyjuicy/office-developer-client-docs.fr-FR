---
title: Propriété canonique PidTagReadReceiptEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82bc5fd99df115527f703eff7261d02d1bf4d3ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786480"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="3eb26-103">Propriété canonique PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="3eb26-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3eb26-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3eb26-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3eb26-105">Contient un identificateur d’entrée de l’utilisateur de messagerie où le système de messagerie doit diriger un rapport de lecture pour ce message.</span><span class="sxs-lookup"><span data-stu-id="3eb26-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3eb26-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3eb26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3eb26-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3eb26-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3eb26-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3eb26-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3eb26-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="3eb26-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="3eb26-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3eb26-110">Data type:</span></span>  <br/> |<span data-ttu-id="3eb26-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3eb26-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3eb26-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3eb26-112">Area:</span></span>  <br/> |<span data-ttu-id="3eb26-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb26-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eb26-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3eb26-114">Remarks</span></span>

<span data-ttu-id="3eb26-115">Cette propriété est ignorée sauf si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="3eb26-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="3eb26-116">Si une application cliente doit recevoir une lu reports lui-même, il peut laisser cette propriété non définie ou définissez-la sur l’identificateur d’entrée contenue dans la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) au moment d’envoi de message.</span><span class="sxs-lookup"><span data-stu-id="3eb26-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3eb26-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3eb26-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3eb26-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3eb26-118">Protocol specifications</span></span>

<span data-ttu-id="3eb26-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb26-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb26-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3eb26-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3eb26-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3eb26-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3eb26-122">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="3eb26-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3eb26-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3eb26-123">Header files</span></span>

<span data-ttu-id="3eb26-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3eb26-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3eb26-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3eb26-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3eb26-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3eb26-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3eb26-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3eb26-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3eb26-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eb26-128">See also</span></span>



[<span data-ttu-id="3eb26-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb26-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3eb26-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb26-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3eb26-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3eb26-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3eb26-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3eb26-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

