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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342678"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="4816e-103">Propriété canonique PidTagOriginalSenderAddressType</span><span class="sxs-lookup"><span data-stu-id="4816e-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="4816e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4816e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4816e-105">Contient le type d’adresse de l’expéditeur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou de répondre.</span><span class="sxs-lookup"><span data-stu-id="4816e-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4816e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4816e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4816e-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="4816e-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="4816e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4816e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4816e-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="4816e-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="4816e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4816e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4816e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4816e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4816e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4816e-112">Area:</span></span>  <br/> |<span data-ttu-id="4816e-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="4816e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4816e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4816e-114">Remarks</span></span>

<span data-ttu-id="4816e-115">Ces propriétés sont des exemples des propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="4816e-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="4816e-116">Lors de la première soumission du message, l’application cliente doit définir ces propriétés sur la valeur **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4816e-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="4816e-117">Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.</span><span class="sxs-lookup"><span data-stu-id="4816e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4816e-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4816e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4816e-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4816e-119">Protocol specifications</span></span>

<span data-ttu-id="4816e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4816e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4816e-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="4816e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4816e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4816e-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4816e-123">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="4816e-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4816e-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4816e-124">Header files</span></span>

<span data-ttu-id="4816e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4816e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4816e-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4816e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4816e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4816e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4816e-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="4816e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4816e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4816e-129">See also</span></span>



[<span data-ttu-id="4816e-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4816e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4816e-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4816e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4816e-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4816e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4816e-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4816e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

