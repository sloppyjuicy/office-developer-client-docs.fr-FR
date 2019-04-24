---
title: Propriété canonique PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327867"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="f1e3d-103">Propriété canonique PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="f1e3d-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f1e3d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1e3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1e3d-105">Contient l'identificateur d'entrée de la racine de la sous-arborescence du dossier des messages interpersonnels dans l'arborescence des dossiers de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1e3d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f1e3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1e3d-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f1e3d-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f1e3d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f1e3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1e3d-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="f1e3d-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="f1e3d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f1e3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1e3d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f1e3d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f1e3d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f1e3d-112">Area:</span></span>  <br/> |<span data-ttu-id="f1e3d-113">Folder</span><span class="sxs-lookup"><span data-stu-id="f1e3d-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1e3d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1e3d-114">Remarks</span></span>

<span data-ttu-id="f1e3d-115">Cette propriété représente la racine de la hiérarchie IPM.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="f1e3d-116">Les clients IPM ne doivent pas afficher de dossiers qui ne sont pas des sous-dossiers du dossier représenté par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1e3d-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f1e3d-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1e3d-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f1e3d-118">Header files</span></span>

<span data-ttu-id="f1e3d-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f1e3d-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1e3d-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1e3d-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f1e3d-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f1e3d-122">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1e3d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1e3d-123">See also</span></span>



[<span data-ttu-id="f1e3d-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f1e3d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1e3d-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f1e3d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1e3d-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f1e3d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1e3d-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f1e3d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

