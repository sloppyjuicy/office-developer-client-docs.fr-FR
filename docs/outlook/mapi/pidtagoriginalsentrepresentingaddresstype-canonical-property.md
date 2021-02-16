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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bfb768b774b1fa3d4b65ad2122f49a8ffe11a7b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341222"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="bcad0-103">Propriété canonique PidTagOriginalSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="bcad0-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="bcad0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcad0-105">Contient le type d’adresse de l’utilisateur de messagerie au nom de qui le message d’origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="bcad0-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcad0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bcad0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcad0-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="bcad0-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="bcad0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bcad0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcad0-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="bcad0-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="bcad0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bcad0-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcad0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bcad0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bcad0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bcad0-112">Area:</span></span>  <br/> |<span data-ttu-id="bcad0-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="bcad0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcad0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bcad0-114">Remarks</span></span>

<span data-ttu-id="bcad0-115">Ces propriétés sont le type de l’expéditeur représenté d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="bcad0-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="bcad0-116">Ils sont utilisés dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="bcad0-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="bcad0-117">Une application cliente envoyant un message pour le compte d’un autre client doit définir ces propriétés sur la valeur de la propriété **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) lors de la première soumission du message.</span><span class="sxs-lookup"><span data-stu-id="bcad0-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="bcad0-118">Une fois définie, elle ne doit jamais être modifiée.</span><span class="sxs-lookup"><span data-stu-id="bcad0-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcad0-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bcad0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcad0-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="bcad0-120">Protocol specifications</span></span>

<span data-ttu-id="bcad0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcad0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcad0-122">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="bcad0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcad0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcad0-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcad0-124">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="bcad0-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcad0-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bcad0-125">Header files</span></span>

<span data-ttu-id="bcad0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcad0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcad0-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bcad0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcad0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bcad0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bcad0-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="bcad0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcad0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcad0-130">See also</span></span>



[<span data-ttu-id="bcad0-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bcad0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcad0-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bcad0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcad0-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bcad0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcad0-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bcad0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

