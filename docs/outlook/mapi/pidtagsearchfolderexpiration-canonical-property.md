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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336469"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="b6023-103">Propriété canonique PidTagSearchFolderExpiration</span><span class="sxs-lookup"><span data-stu-id="b6023-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="b6023-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6023-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6023-105">Contient l'heure à laquelle le conteneur du dossier de recherche sera périmé et doit être mis à jour ou recréé.</span><span class="sxs-lookup"><span data-stu-id="b6023-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6023-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b6023-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6023-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="b6023-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="b6023-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b6023-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6023-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="b6023-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="b6023-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b6023-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6023-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b6023-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b6023-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b6023-112">Area:</span></span>  <br/> |<span data-ttu-id="b6023-113">Rechercher</span><span class="sxs-lookup"><span data-stu-id="b6023-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6023-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6023-114">Remarks</span></span>

<span data-ttu-id="b6023-115">Cette propriété doit être mise en forme en tant que nombre de minutes écoulées depuis minuit UTC (temps universel coordonné) le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="b6023-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6023-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="b6023-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6023-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b6023-117">Protocol specifications</span></span>

<span data-ttu-id="b6023-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6023-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6023-119">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b6023-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6023-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6023-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6023-121">Spécifie les propriétés et les opérations pour la manipulation d'une configuration de liste des dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="b6023-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6023-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="b6023-122">Header files</span></span>

<span data-ttu-id="b6023-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b6023-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6023-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b6023-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6023-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b6023-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b6023-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="b6023-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6023-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6023-127">See also</span></span>



[<span data-ttu-id="b6023-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b6023-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6023-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b6023-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6023-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b6023-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6023-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b6023-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

