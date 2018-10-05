---
title: Propriété canonique PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385944"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="51f77-103">Propriété canonique PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="51f77-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="51f77-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51f77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51f77-105">Contient l’heure à laquelle le conteneur de dossiers de recherche sera obsolète et doit être mis à jour ou recréé.</span><span class="sxs-lookup"><span data-stu-id="51f77-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51f77-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="51f77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51f77-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="51f77-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="51f77-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="51f77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51f77-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="51f77-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="51f77-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="51f77-110">Data type:</span></span>  <br/> |<span data-ttu-id="51f77-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51f77-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51f77-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="51f77-112">Area:</span></span>  <br/> |<span data-ttu-id="51f77-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="51f77-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51f77-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="51f77-114">Remarks</span></span>

<span data-ttu-id="51f77-115">Cette propriété doit être mis en forme en tant que le nombre de minutes depuis minuit temps universel coordonné (UTC) le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="51f77-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51f77-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="51f77-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51f77-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="51f77-117">Protocol specifications</span></span>

<span data-ttu-id="51f77-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51f77-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51f77-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="51f77-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51f77-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51f77-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51f77-121">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="51f77-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51f77-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="51f77-122">Header files</span></span>

<span data-ttu-id="51f77-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51f77-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="51f77-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="51f77-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="51f77-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="51f77-125">Mapitags.h</span></span>
  
> <span data-ttu-id="51f77-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="51f77-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51f77-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51f77-127">See also</span></span>



[<span data-ttu-id="51f77-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="51f77-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51f77-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="51f77-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51f77-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="51f77-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51f77-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="51f77-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

