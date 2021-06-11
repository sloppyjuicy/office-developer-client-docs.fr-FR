---
title: Propriété canonique PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320040"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="39d3a-103">Propriété canonique PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="39d3a-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="39d3a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39d3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39d3a-105">Contient une clé de recherche pour l’utilisateur de messagerie vers lequel le système de messagerie doit diriger un rapport de lecture pour un message.</span><span class="sxs-lookup"><span data-stu-id="39d3a-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39d3a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="39d3a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39d3a-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="39d3a-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="39d3a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39d3a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39d3a-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="39d3a-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="39d3a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="39d3a-110">Data type:</span></span>  <br/> |<span data-ttu-id="39d3a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39d3a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39d3a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="39d3a-112">Area:</span></span>  <br/> |<span data-ttu-id="39d3a-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="39d3a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39d3a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="39d3a-114">Remarks</span></span>

<span data-ttu-id="39d3a-115">Cette propriété est ignorée, sauf si **la propriété PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="39d3a-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="39d3a-116">Si une application cliente souhaite recevoir elle-même des rapports de lecture, elle peut laisser cette propriété non définie ou la définir sur la clé de recherche contenue dans la propriété **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) au moment de l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="39d3a-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="39d3a-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="39d3a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39d3a-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="39d3a-118">Protocol specifications</span></span>

<span data-ttu-id="39d3a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39d3a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39d3a-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="39d3a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39d3a-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39d3a-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39d3a-122">Spécifie les propriétés et opérations autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="39d3a-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39d3a-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="39d3a-123">Header files</span></span>

<span data-ttu-id="39d3a-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="39d3a-124">Mapidef.h</span></span>
  
> <span data-ttu-id="39d3a-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="39d3a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="39d3a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39d3a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="39d3a-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="39d3a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39d3a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39d3a-128">See also</span></span>



[<span data-ttu-id="39d3a-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="39d3a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39d3a-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="39d3a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39d3a-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="39d3a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39d3a-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="39d3a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

