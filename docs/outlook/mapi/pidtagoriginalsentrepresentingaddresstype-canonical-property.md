---
title: Propriété canonique PidTagOriginalSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ce3678c5137caec2e9f80c7fc15cde0ae99441ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572528"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="840ff-103">Propriété canonique PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="840ff-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="840ff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="840ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="840ff-105">Contient le type d’adresse de l’utilisateur de messagerie pour le compte duquel le message d’origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="840ff-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="840ff-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="840ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="840ff-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="840ff-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="840ff-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="840ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="840ff-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="840ff-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="840ff-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="840ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="840ff-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="840ff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="840ff-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="840ff-112">Area:</span></span>  <br/> |<span data-ttu-id="840ff-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="840ff-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="840ff-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="840ff-114">Remarks</span></span>

<span data-ttu-id="840ff-115">Ces propriétés sont du type pour l’expéditeur représenté d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="840ff-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="840ff-116">Ils sont utilisés dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="840ff-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="840ff-117">Une application cliente envoie un message de la part d’un autre client doit définir ces propriétés à la valeur de la propriété **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) à la première soumission du message.</span><span class="sxs-lookup"><span data-stu-id="840ff-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="840ff-118">Une fois définies, il doit jamais être modifié.</span><span class="sxs-lookup"><span data-stu-id="840ff-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="840ff-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="840ff-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="840ff-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="840ff-120">Protocol specifications</span></span>

<span data-ttu-id="840ff-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="840ff-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="840ff-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="840ff-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="840ff-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="840ff-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="840ff-124">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="840ff-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="840ff-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="840ff-125">Header files</span></span>

<span data-ttu-id="840ff-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="840ff-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="840ff-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="840ff-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="840ff-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="840ff-128">Mapitags.h</span></span>
  
> <span data-ttu-id="840ff-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="840ff-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="840ff-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="840ff-130">See also</span></span>



[<span data-ttu-id="840ff-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="840ff-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="840ff-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="840ff-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="840ff-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="840ff-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="840ff-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="840ff-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

