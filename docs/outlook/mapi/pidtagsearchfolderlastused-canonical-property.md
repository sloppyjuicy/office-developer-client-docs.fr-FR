---
title: Propriété canonique PidTagSearchFolderLastUsed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderLastUsed
api_type:
- COM
ms.assetid: e4071307-6205-4079-ab65-7499d14f145c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ff6df6eddc8e610341cb09ccb152f4ad748a984
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336532"
---
# <a name="pidtagsearchfolderlastused-canonical-property"></a><span data-ttu-id="2d94a-103">Propriété canonique PidTagSearchFolderLastUsed</span><span class="sxs-lookup"><span data-stu-id="2d94a-103">PidTagSearchFolderLastUsed Canonical Property</span></span>

  
  
<span data-ttu-id="2d94a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d94a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d94a-105">Représente la dernière fois que le dossier a été accédé.</span><span class="sxs-lookup"><span data-stu-id="2d94a-105">Represents the last time the folder was accessed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d94a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2d94a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d94a-107">PR_WB_SF_LAST_USED</span><span class="sxs-lookup"><span data-stu-id="2d94a-107">PR_WB_SF_LAST_USED</span></span>  <br/> |
|<span data-ttu-id="2d94a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2d94a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d94a-109">0x6834</span><span class="sxs-lookup"><span data-stu-id="2d94a-109">0x6834</span></span>  <br/> |
|<span data-ttu-id="2d94a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2d94a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2d94a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2d94a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2d94a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2d94a-112">Area:</span></span>  <br/> |<span data-ttu-id="2d94a-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="2d94a-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d94a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d94a-114">Remarks</span></span>

<span data-ttu-id="2d94a-115">Cette propriété doit être mise en forme comme le nombre de minutes depuis le 1er janvier 1601 à minuit ( UTC).</span><span class="sxs-lookup"><span data-stu-id="2d94a-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2d94a-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2d94a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d94a-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="2d94a-117">Protocol specifications</span></span>

<span data-ttu-id="2d94a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d94a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d94a-119">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="2d94a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d94a-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d94a-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d94a-121">Spécifie les propriétés et opérations de manipulation d’une configuration de liste de dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="2d94a-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d94a-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2d94a-122">Header files</span></span>

<span data-ttu-id="2d94a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d94a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d94a-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2d94a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d94a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2d94a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2d94a-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="2d94a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d94a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d94a-127">See also</span></span>



[<span data-ttu-id="2d94a-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2d94a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d94a-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2d94a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d94a-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2d94a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d94a-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2d94a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

