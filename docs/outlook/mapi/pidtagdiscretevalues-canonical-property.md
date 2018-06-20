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
ms.openlocfilehash: 9911d6cee40637a69dfaf432be0e6d42bf38bccd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785954"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="26abe-103">Propriété canonique PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="26abe-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="26abe-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26abe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26abe-105">Contient la valeur TRUE si un rapport de non-remise s’applique uniquement à des membres d’une liste de distribution plutôt que l’intégralité de la liste.</span><span class="sxs-lookup"><span data-stu-id="26abe-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26abe-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="26abe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26abe-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="26abe-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="26abe-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="26abe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26abe-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="26abe-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="26abe-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="26abe-110">Data type:</span></span>  <br/> |<span data-ttu-id="26abe-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="26abe-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="26abe-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="26abe-112">Area:</span></span>  <br/> |<span data-ttu-id="26abe-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="26abe-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26abe-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="26abe-114">Remarks</span></span>

<span data-ttu-id="26abe-115">Cette propriété est utilisée dans un rapport de non-remise lorsque le message n’a pas pu être remis à un ou plusieurs membres d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="26abe-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="26abe-116">Son objectif est de limiter retransmission tente seuls les membres individuels et pas la liste de distribution dans sa globalité.</span><span class="sxs-lookup"><span data-stu-id="26abe-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="26abe-117">La table de destinataires d’un rapport de non-remise contient les entrées de tous les destinataires auxquels le message pas pu être remis, ainsi que pour les listes de distribution, le cas échéant, auxquels ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="26abe-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="26abe-118">Le fournisseur de transport doit définir cette propriété sur TRUE pour chaque entrée de liste de distribution, et il doit copier les **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **clé PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) à partir de la liste de distribution **PR_ORIGINAL_SEARCH_KEY** ([ , **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) et **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)) PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) Propriétés pour chaque membre de cette liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="26abe-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="26abe-119">**PR_DISCRETE_VALUES** ne doit pas être défini pour une entrée de destinataire de rapport de non-remise autre qu’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="26abe-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="26abe-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="26abe-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="26abe-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="26abe-121">Header files</span></span>

<span data-ttu-id="26abe-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26abe-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="26abe-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="26abe-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="26abe-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="26abe-124">Mapitags.h</span></span>
  
> <span data-ttu-id="26abe-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="26abe-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26abe-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26abe-126">See also</span></span>



[<span data-ttu-id="26abe-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="26abe-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26abe-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="26abe-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26abe-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="26abe-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26abe-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="26abe-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

