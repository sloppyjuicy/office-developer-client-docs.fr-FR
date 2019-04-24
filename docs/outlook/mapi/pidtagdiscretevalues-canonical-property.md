---
title: Propriété canonique PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360822"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="0b4e8-103">Propriété canonique PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="0b4e8-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="0b4e8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b4e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b4e8-105">Contient la valeur TRUE si un rapport de non-remise s'applique uniquement aux membres discrets d'une liste de distribution plutôt qu'à la liste entière.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b4e8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0b4e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b4e8-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="0b4e8-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="0b4e8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0b4e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b4e8-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="0b4e8-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="0b4e8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0b4e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b4e8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0b4e8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0b4e8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0b4e8-112">Area:</span></span>  <br/> |<span data-ttu-id="0b4e8-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="0b4e8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b4e8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0b4e8-114">Remarks</span></span>

<span data-ttu-id="0b4e8-115">Cette propriété est utilisée dans un rapport de non-remise lorsque le message n'a pas pu être remis à un ou plusieurs membres d'une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="0b4e8-116">Son objectif est de limiter les tentatives de retransmission aux seuls membres individuels et non à la liste de distribution dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="0b4e8-117">Le tableau de destinataires d'un rapport de non-remise contient les entrées de tous les destinataires auxquels le message n'a pas pu être remis, ainsi que les listes de distribution, le cas échéant, auxquelles ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="0b4e8-118">Le fournisseur de transport doit affecter la valeur TRUE à cette propriété pour chaque entrée de liste de distribution, et il doit copier **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de la liste de distribution vers **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) et **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) pour chaque membre de cette liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="0b4e8-119">**PR_DISCRETE_VALUES** ne doit pas être défini pour toute entrée de destinataire de rapport de non-remise autre qu'une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0b4e8-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="0b4e8-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0b4e8-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="0b4e8-121">Header files</span></span>

<span data-ttu-id="0b4e8-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0b4e8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b4e8-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b4e8-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0b4e8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0b4e8-125">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0b4e8-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b4e8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b4e8-126">See also</span></span>



[<span data-ttu-id="0b4e8-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0b4e8-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b4e8-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0b4e8-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b4e8-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0b4e8-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b4e8-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0b4e8-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

