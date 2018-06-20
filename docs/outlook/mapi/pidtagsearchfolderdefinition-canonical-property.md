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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d19904b65b95468bd38df75aa8e05afdf0075961
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786727"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="bf188-103">Propriété canonique PidTagSearchFolderDefinition</span><span class="sxs-lookup"><span data-stu-id="bf188-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="bf188-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf188-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf188-105">Contient des données qui spécifie les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="bf188-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf188-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bf188-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf188-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="bf188-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="bf188-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bf188-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf188-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="bf188-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="bf188-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bf188-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf188-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bf188-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bf188-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="bf188-112">Area:</span></span>  <br/> |<span data-ttu-id="bf188-113">Search</span><span class="sxs-lookup"><span data-stu-id="bf188-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf188-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf188-114">Remarks</span></span>

<span data-ttu-id="bf188-115">Le contenu spécifique de chaque champ de l’objet binaire volumineux (BLOB) contenue dans cette propriété dépend de l’ID du modèle spécifié dans la propriété **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bf188-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="bf188-116">Pour plus d’informations sur les modèles de structure et la recherche des objets BLOB, voir [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf188-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bf188-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bf188-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf188-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bf188-118">Protocol specifications</span></span>

<span data-ttu-id="bf188-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf188-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf188-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="bf188-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf188-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf188-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf188-122">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="bf188-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf188-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bf188-123">Header files</span></span>

<span data-ttu-id="bf188-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf188-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf188-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bf188-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf188-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="bf188-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bf188-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="bf188-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf188-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf188-128">See also</span></span>



[<span data-ttu-id="bf188-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bf188-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf188-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bf188-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf188-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bf188-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf188-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="bf188-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

