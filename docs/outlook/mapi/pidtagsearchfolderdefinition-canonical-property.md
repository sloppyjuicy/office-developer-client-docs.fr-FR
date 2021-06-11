---
title: Propriété canonique PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336357"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="cbe17-103">Propriété canonique PidTagSearchFolderDefinition</span><span class="sxs-lookup"><span data-stu-id="cbe17-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="cbe17-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbe17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbe17-105">Contient des données qui spécifient les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="cbe17-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbe17-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cbe17-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbe17-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="cbe17-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="cbe17-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cbe17-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbe17-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="cbe17-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="cbe17-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cbe17-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbe17-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cbe17-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cbe17-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cbe17-112">Area:</span></span>  <br/> |<span data-ttu-id="cbe17-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="cbe17-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbe17-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbe17-114">Remarks</span></span>

<span data-ttu-id="cbe17-115">Le contenu spécifique de chaque champ de l’objet BLOB (Binary Large Object) contenu dans cette propriété dépend de l’ID de modèle spécifié dans la propriété **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId).](pidtagsearchfoldertemplateid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cbe17-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="cbe17-116">Pour plus d’informations sur la structure BLOB et les modèles de recherche, voir [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cbe17-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cbe17-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cbe17-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbe17-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="cbe17-118">Protocol specifications</span></span>

<span data-ttu-id="cbe17-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbe17-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbe17-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="cbe17-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cbe17-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbe17-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbe17-122">Spécifie les propriétés et opérations de manipulation d’une configuration de liste de dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="cbe17-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbe17-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cbe17-123">Header files</span></span>

<span data-ttu-id="cbe17-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbe17-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbe17-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cbe17-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cbe17-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cbe17-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cbe17-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="cbe17-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbe17-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbe17-128">See also</span></span>



[<span data-ttu-id="cbe17-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cbe17-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbe17-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cbe17-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbe17-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cbe17-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbe17-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cbe17-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

