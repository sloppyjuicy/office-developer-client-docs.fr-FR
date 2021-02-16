---
title: Propriété canonique PidTagOriginalSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eaf91472794c5188a63897bccaa900c4882407bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341754"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="30fe1-103">Propriété canonique PidTagOriginalSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="30fe1-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="30fe1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30fe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30fe1-105">Contient l’identificateur d’entrée de l’utilisateur de messagerie au nom de qui le message d’origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="30fe1-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30fe1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="30fe1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30fe1-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="30fe1-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="30fe1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="30fe1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30fe1-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="30fe1-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="30fe1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="30fe1-110">Data type:</span></span>  <br/> |<span data-ttu-id="30fe1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="30fe1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="30fe1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="30fe1-112">Area:</span></span>  <br/> |<span data-ttu-id="30fe1-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="30fe1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30fe1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="30fe1-114">Remarks</span></span>

<span data-ttu-id="30fe1-115">Cette propriété est l’une des propriétés d’adresse de l’expéditeur représenté d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="30fe1-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="30fe1-116">Il est utilisé dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="30fe1-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="30fe1-117">Une application cliente envoyant un message pour le compte d’un autre client doit définir cette propriété sur la valeur de la propriété **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) lors de la première soumission du message.</span><span class="sxs-lookup"><span data-stu-id="30fe1-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="30fe1-118">Une fois définie, elle ne doit jamais être modifiée.</span><span class="sxs-lookup"><span data-stu-id="30fe1-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="30fe1-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="30fe1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30fe1-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="30fe1-120">Protocol specifications</span></span>

<span data-ttu-id="30fe1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fe1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fe1-122">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="30fe1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30fe1-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fe1-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fe1-124">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="30fe1-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30fe1-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="30fe1-125">Header files</span></span>

<span data-ttu-id="30fe1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30fe1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="30fe1-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="30fe1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="30fe1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30fe1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="30fe1-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="30fe1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30fe1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30fe1-130">See also</span></span>



[<span data-ttu-id="30fe1-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="30fe1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30fe1-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="30fe1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30fe1-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="30fe1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30fe1-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="30fe1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

