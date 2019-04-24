---
title: Propriété canonique PidTagOriginalSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342615"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="313bd-103">Propriété canonique PidTagOriginalSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="313bd-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="313bd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="313bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="313bd-105">Contient l'identificateur d'entrée de l'expéditeur de la première version d'un message, c'est-à-dire le message avant son transfert ou sa réponse.</span><span class="sxs-lookup"><span data-stu-id="313bd-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="313bd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="313bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="313bd-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="313bd-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="313bd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="313bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="313bd-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="313bd-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="313bd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="313bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="313bd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="313bd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="313bd-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="313bd-112">Area:</span></span>  <br/> |<span data-ttu-id="313bd-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="313bd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="313bd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="313bd-114">Remarks</span></span>

<span data-ttu-id="313bd-115">Cette propriété est l'une des propriétés d'adresse de l'expéditeur d'origine d'un message.</span><span class="sxs-lookup"><span data-stu-id="313bd-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="313bd-116">Lors de la première soumission du message, une application cliente doit définir cette propriété sur la valeur de la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="313bd-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="313bd-117">Il n'est jamais modifié lorsque le message est transféré ou renvoyé.</span><span class="sxs-lookup"><span data-stu-id="313bd-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="313bd-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="313bd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="313bd-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="313bd-119">Protocol specifications</span></span>

<span data-ttu-id="313bd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313bd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313bd-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="313bd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="313bd-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="313bd-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="313bd-123">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="313bd-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="313bd-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="313bd-124">Header files</span></span>

<span data-ttu-id="313bd-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="313bd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="313bd-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="313bd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="313bd-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="313bd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="313bd-128">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="313bd-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="313bd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="313bd-129">See also</span></span>



[<span data-ttu-id="313bd-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="313bd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="313bd-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="313bd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="313bd-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="313bd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="313bd-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="313bd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

