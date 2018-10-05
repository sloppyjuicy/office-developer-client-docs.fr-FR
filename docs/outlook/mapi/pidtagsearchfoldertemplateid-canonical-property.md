---
title: Propriété canonique PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387201"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="e65a9-103">Propriété canonique PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="e65a9-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="e65a9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e65a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e65a9-105">Contient l’ID du modèle qui est utilisé pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="e65a9-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e65a9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e65a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e65a9-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="e65a9-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="e65a9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e65a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e65a9-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="e65a9-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="e65a9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e65a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="e65a9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e65a9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e65a9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e65a9-112">Area:</span></span>  <br/> |<span data-ttu-id="e65a9-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="e65a9-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e65a9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e65a9-114">Remarks</span></span>

<span data-ttu-id="e65a9-115">Critères du dossier de recherche est spécifiée par un modèle.</span><span class="sxs-lookup"><span data-stu-id="e65a9-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="e65a9-116">Cette propriété sur le message qui définit le dossier de recherche identifie le modèle correspondant.</span><span class="sxs-lookup"><span data-stu-id="e65a9-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="e65a9-117">Outre la définition des critères de recherche, un modèle également définit les dossiers à exclure de la recherche, définit des éléments à exclure de la recherche et spécifie la valeur de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e65a9-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="e65a9-118">Pour plus d’informations sur les modèles de dossier de recherche, voir [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e65a9-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e65a9-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e65a9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e65a9-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e65a9-120">Protocol specifications</span></span>

<span data-ttu-id="e65a9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e65a9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e65a9-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="e65a9-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e65a9-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e65a9-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e65a9-124">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="e65a9-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e65a9-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e65a9-125">Header files</span></span>

<span data-ttu-id="e65a9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e65a9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e65a9-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e65a9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e65a9-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e65a9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e65a9-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e65a9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e65a9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e65a9-130">See also</span></span>



[<span data-ttu-id="e65a9-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e65a9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e65a9-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e65a9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e65a9-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e65a9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e65a9-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e65a9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

