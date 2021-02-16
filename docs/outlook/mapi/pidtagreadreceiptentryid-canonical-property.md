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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356507"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="4ef2f-103">Propriété canonique PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="4ef2f-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4ef2f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ef2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ef2f-105">Contient un identificateur d’entrée pour l’utilisateur de messagerie où le système de messagerie doit diriger un rapport de lecture pour ce message.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ef2f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4ef2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ef2f-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4ef2f-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4ef2f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4ef2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ef2f-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="4ef2f-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="4ef2f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4ef2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ef2f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ef2f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ef2f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4ef2f-112">Area:</span></span>  <br/> |<span data-ttu-id="4ef2f-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef2f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ef2f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4ef2f-114">Remarks</span></span>

<span data-ttu-id="4ef2f-115">Cette propriété est ignorée, sauf si **la propriété PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="4ef2f-116">Si une application cliente souhaite recevoir des rapports de lecture elle-même, elle peut laisser cette propriété non définie ou la définir sur l’identificateur d’entrée contenu dans la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) au moment de la soumission du message.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ef2f-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4ef2f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ef2f-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4ef2f-118">Protocol specifications</span></span>

<span data-ttu-id="4ef2f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ef2f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ef2f-120">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ef2f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ef2f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ef2f-122">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ef2f-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4ef2f-123">Header files</span></span>

<span data-ttu-id="4ef2f-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ef2f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ef2f-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ef2f-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ef2f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4ef2f-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ef2f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ef2f-128">See also</span></span>



[<span data-ttu-id="4ef2f-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef2f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ef2f-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef2f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ef2f-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef2f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ef2f-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4ef2f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

