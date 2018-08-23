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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bac1d53b890df056ff15cd6d3ad665f50e3ce3f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580956"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="fa57f-103">Propriété canonique PidTagOriginalSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="fa57f-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="fa57f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa57f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa57f-105">Contient l’identificateur d’entrée de l’utilisateur de messagerie pour le compte duquel le message d’origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="fa57f-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa57f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fa57f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa57f-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fa57f-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="fa57f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fa57f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa57f-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="fa57f-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="fa57f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fa57f-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa57f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fa57f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fa57f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fa57f-112">Area:</span></span>  <br/> |<span data-ttu-id="fa57f-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="fa57f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa57f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa57f-114">Remarks</span></span>

<span data-ttu-id="fa57f-115">Cette propriété est une des propriétés d’adresse de l’expéditeur d’origine représenté d’un message.</span><span class="sxs-lookup"><span data-stu-id="fa57f-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="fa57f-116">Il est utilisé dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="fa57f-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="fa57f-117">Une application cliente envoie un message de la part d’un autre client doit définir cette propriété à la valeur de la propriété **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) à la première soumission du message.</span><span class="sxs-lookup"><span data-stu-id="fa57f-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="fa57f-118">Une fois définies, il doit jamais être modifié.</span><span class="sxs-lookup"><span data-stu-id="fa57f-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa57f-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fa57f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa57f-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="fa57f-120">Protocol specifications</span></span>

<span data-ttu-id="fa57f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa57f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa57f-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="fa57f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa57f-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa57f-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa57f-124">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="fa57f-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa57f-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fa57f-125">Header files</span></span>

<span data-ttu-id="fa57f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa57f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa57f-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fa57f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa57f-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="fa57f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="fa57f-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="fa57f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa57f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa57f-130">See also</span></span>



[<span data-ttu-id="fa57f-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fa57f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa57f-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fa57f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa57f-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fa57f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa57f-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fa57f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

