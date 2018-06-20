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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7fcd358b2ada5137ed28f4439dcc9d4ebdc50305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786322"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="b2a7d-103">Propriété canonique PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="b2a7d-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="b2a7d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2a7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2a7d-105">Contient le type d’adresse de l’utilisateur de messagerie pour le compte duquel le message d’origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2a7d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b2a7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2a7d-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="b2a7d-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="b2a7d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b2a7d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2a7d-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="b2a7d-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="b2a7d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b2a7d-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2a7d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b2a7d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b2a7d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="b2a7d-112">Area:</span></span>  <br/> |<span data-ttu-id="b2a7d-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="b2a7d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2a7d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2a7d-114">Remarks</span></span>

<span data-ttu-id="b2a7d-115">Ces propriétés sont du type pour l’expéditeur représenté d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="b2a7d-116">Ils sont utilisés dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="b2a7d-117">Une application cliente envoie un message de la part d’un autre client doit définir ces propriétés à la valeur de la propriété **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) à la première soumission du message.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="b2a7d-118">Une fois définies, il doit jamais être modifié.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2a7d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b2a7d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2a7d-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b2a7d-120">Protocol specifications</span></span>

<span data-ttu-id="b2a7d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2a7d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2a7d-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2a7d-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2a7d-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2a7d-124">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2a7d-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b2a7d-125">Header files</span></span>

<span data-ttu-id="b2a7d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2a7d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2a7d-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2a7d-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b2a7d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b2a7d-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b2a7d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2a7d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2a7d-130">See also</span></span>



[<span data-ttu-id="b2a7d-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b2a7d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2a7d-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b2a7d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2a7d-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b2a7d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2a7d-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b2a7d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

