---
title: Propriété canonique PidTagSearchFolderTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b7a88387-72ff-49e5-b73a-8bafab635658
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7d5f63a7a57a01096151b3b6992796381ebddbdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574516"
---
# <a name="pidtagsearchfoldertag-canonical-property"></a><span data-ttu-id="8b376-103">Propriété canonique PidTagSearchFolderTag</span><span class="sxs-lookup"><span data-stu-id="8b376-103">PidTagSearchFolderTag Canonical Property</span></span>

  
  
<span data-ttu-id="8b376-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b376-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b376-105">Contient la valeur utilisée pour synchroniser ce message définition avec le conteneur de dossiers de recherche correspondant.</span><span class="sxs-lookup"><span data-stu-id="8b376-105">Contains the value used to synchronize this definition message with the matching search folder container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b376-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8b376-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b376-107">PR_WB_SF_TAG</span><span class="sxs-lookup"><span data-stu-id="8b376-107">PR_WB_SF_TAG</span></span>  <br/> |
|<span data-ttu-id="8b376-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8b376-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b376-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="8b376-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="8b376-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8b376-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b376-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8b376-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8b376-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8b376-112">Area:</span></span>  <br/> |<span data-ttu-id="8b376-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="8b376-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b376-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b376-114">Remarks</span></span>

<span data-ttu-id="8b376-115">Cette propriété est modifiée lorsque le message de la définition est modifié.</span><span class="sxs-lookup"><span data-stu-id="8b376-115">This property is changed when the definition message is changed.</span></span> <span data-ttu-id="8b376-116">Il doit modifier chaque itération, mais il ne peut pas être unique.</span><span class="sxs-lookup"><span data-stu-id="8b376-116">It must change each iteration, but it may not be unique.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b376-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8b376-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b376-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8b376-118">Protocol specifications</span></span>

<span data-ttu-id="8b376-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b376-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b376-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8b376-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b376-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b376-121">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b376-122">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="8b376-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b376-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8b376-123">Header files</span></span>

<span data-ttu-id="8b376-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b376-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b376-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8b376-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b376-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8b376-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8b376-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8b376-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b376-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b376-128">See also</span></span>



[<span data-ttu-id="8b376-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8b376-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b376-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8b376-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b376-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8b376-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b376-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8b376-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

