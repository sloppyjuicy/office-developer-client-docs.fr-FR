---
title: Propriété canonique PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5cac96287db9638f699b75e0c387e003beb5e197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786330"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="59e8a-103">Propriété canonique PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="59e8a-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="59e8a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59e8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59e8a-105">Contient le type d’adresse de l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="59e8a-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59e8a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="59e8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59e8a-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="59e8a-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="59e8a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="59e8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59e8a-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="59e8a-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="59e8a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="59e8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="59e8a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59e8a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="59e8a-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="59e8a-112">Area:</span></span>  <br/> |<span data-ttu-id="59e8a-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="59e8a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59e8a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="59e8a-114">Remarks</span></span>

<span data-ttu-id="59e8a-115">Ces propriétés sont des exemples de propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="59e8a-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="59e8a-116">Au premier envoi du message, l’application cliente doit définir ces propriétés à la valeur de **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59e8a-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="59e8a-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="59e8a-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59e8a-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="59e8a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59e8a-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="59e8a-119">Protocol specifications</span></span>

<span data-ttu-id="59e8a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59e8a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59e8a-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="59e8a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59e8a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59e8a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59e8a-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="59e8a-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59e8a-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="59e8a-124">Header files</span></span>

<span data-ttu-id="59e8a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59e8a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="59e8a-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="59e8a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="59e8a-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="59e8a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="59e8a-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="59e8a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59e8a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59e8a-129">See also</span></span>



[<span data-ttu-id="59e8a-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="59e8a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59e8a-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="59e8a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59e8a-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="59e8a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59e8a-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="59e8a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

