---
title: Propriété canonique PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340977"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="39767-103">Propriété canonique PidTagOriginalSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="39767-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="39767-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39767-105">Contient la clé de recherche de l'utilisateur de messagerie au nom duquel le message d'origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="39767-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39767-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="39767-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39767-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="39767-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="39767-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39767-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39767-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="39767-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="39767-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="39767-110">Data type:</span></span>  <br/> |<span data-ttu-id="39767-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39767-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39767-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="39767-112">Area:</span></span>  <br/> |<span data-ttu-id="39767-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="39767-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39767-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="39767-114">Remarks</span></span>

<span data-ttu-id="39767-115">Cette propriété est l'une des propriétés d'adresse de l'expéditeur d'origine d'un message.</span><span class="sxs-lookup"><span data-stu-id="39767-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="39767-116">Il est utilisé dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="39767-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="39767-117">Une application client qui envoie un message au nom d'un autre client doit définir cette propriété sur la valeur de la propriété **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) lors du premier envoi du message.</span><span class="sxs-lookup"><span data-stu-id="39767-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="39767-118">Une fois défini, il ne doit jamais être modifié.</span><span class="sxs-lookup"><span data-stu-id="39767-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="39767-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="39767-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39767-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="39767-120">Protocol specifications</span></span>

<span data-ttu-id="39767-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39767-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39767-122">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="39767-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39767-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39767-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39767-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="39767-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39767-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="39767-125">Header files</span></span>

<span data-ttu-id="39767-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="39767-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="39767-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="39767-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="39767-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="39767-128">Mapitags.h</span></span>
  
> <span data-ttu-id="39767-129">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="39767-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39767-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39767-130">See also</span></span>



[<span data-ttu-id="39767-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="39767-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39767-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="39767-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39767-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="39767-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39767-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="39767-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

