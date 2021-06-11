---
title: Propriété canonique PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336427"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a><span data-ttu-id="88568-103">Propriété canonique PidTagSearchFolderEfpFlags</span><span class="sxs-lookup"><span data-stu-id="88568-103">PidTagSearchFolderEfpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="88568-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88568-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88568-105">Contient des indicateurs de dossier étendu qui s’appliquent au conteneur de dossiers de recherche pour le dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="88568-105">Contains extended folder flags that apply to the search folder container for the search folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88568-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="88568-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88568-107">PR_WB_SF_EFP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="88568-107">PR_WB_SF_EFP_FLAGS</span></span>  <br/> |
|<span data-ttu-id="88568-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="88568-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88568-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="88568-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="88568-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="88568-110">Data type:</span></span>  <br/> |<span data-ttu-id="88568-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="88568-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="88568-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="88568-112">Area:</span></span>  <br/> |<span data-ttu-id="88568-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="88568-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88568-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="88568-114">Remarks</span></span>

<span data-ttu-id="88568-115">Cette propriété doit contenir spécifiquement les indicateurs dans la propriété **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) et la sous-propriété **ExtendedFlags,** dans le champ b pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="88568-115">This property should specifically contain the flags in the **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) property, and the **ExtendedFlags** sub-property, in field b for the folder.</span></span> <span data-ttu-id="88568-116">Pour plus d’informations sur les indicateurs de dossier, [voir [MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="88568-116">For information about folder flags see the [[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88568-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="88568-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88568-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="88568-118">Protocol specifications</span></span>

<span data-ttu-id="88568-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88568-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88568-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="88568-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88568-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88568-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88568-122">Spécifie les propriétés et opérations de manipulation d’une configuration de liste de dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="88568-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
<span data-ttu-id="88568-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88568-123">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88568-124">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que les listes de catégories partagées et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="88568-124">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88568-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88568-125">Header files</span></span>

<span data-ttu-id="88568-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88568-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="88568-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="88568-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="88568-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="88568-128">Mapitags.h</span></span>
  
> <span data-ttu-id="88568-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="88568-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88568-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88568-130">See also</span></span>



[<span data-ttu-id="88568-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="88568-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88568-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="88568-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88568-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="88568-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88568-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="88568-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

