---
title: Propriété canonique PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6b71feb6d5967eab3aa490a256825a2803381f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569091"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="0b8ab-103">Propriété canonique PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="0b8ab-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="0b8ab-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b8ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b8ab-105">Fournit le nom de table (fichier .pst) stockage personnel, l’utilisateur peut modifier, pour la boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="0b8ab-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b8ab-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0b8ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b8ab-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="0b8ab-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="0b8ab-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0b8ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b8ab-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="0b8ab-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="0b8ab-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0b8ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b8ab-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b8ab-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0b8ab-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0b8ab-112">Area:</span></span>  <br/> |<span data-ttu-id="0b8ab-113">Tableau de stockage personnel (.pst) interne</span><span class="sxs-lookup"><span data-stu-id="0b8ab-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b8ab-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0b8ab-114">Remarks</span></span>

<span data-ttu-id="0b8ab-115">Si la propriété **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) est utilisée au lieu de cela, la boîte de dialogue configuration s’ouvre, mais l’utilisateur n’est pas être autorisé pour modifier le chemin d’accès et de nombreuses autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="0b8ab-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b8ab-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0b8ab-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b8ab-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0b8ab-117">Protocol specifications</span></span>

<span data-ttu-id="0b8ab-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="0b8ab-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="0b8ab-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0b8ab-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b8ab-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0b8ab-120">Header files</span></span>

<span data-ttu-id="0b8ab-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b8ab-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b8ab-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0b8ab-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b8ab-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0b8ab-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0b8ab-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0b8ab-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b8ab-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b8ab-125">See also</span></span>



[<span data-ttu-id="0b8ab-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0b8ab-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b8ab-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0b8ab-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b8ab-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0b8ab-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b8ab-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0b8ab-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

