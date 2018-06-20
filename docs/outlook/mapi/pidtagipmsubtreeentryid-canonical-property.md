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
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786143"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="1b82f-103">Propriété canonique PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="1b82f-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1b82f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b82f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b82f-105">Contient l’identificateur d’entrée de la racine de la sous-arborescence de dossier message interpersonnel (IPM) dans l’arborescence de dossiers de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1b82f-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b82f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1b82f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b82f-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1b82f-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1b82f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1b82f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b82f-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="1b82f-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="1b82f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1b82f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b82f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b82f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b82f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="1b82f-112">Area:</span></span>  <br/> |<span data-ttu-id="1b82f-113">Folder</span><span class="sxs-lookup"><span data-stu-id="1b82f-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b82f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b82f-114">Remarks</span></span>

<span data-ttu-id="1b82f-115">Cette propriété représente la racine de la hiérarchie IPM.</span><span class="sxs-lookup"><span data-stu-id="1b82f-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="1b82f-116">Clients IPM ne doivent pas afficher tous les dossiers qui ne sont pas des sous-dossiers du dossier représenté par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1b82f-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b82f-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1b82f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b82f-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1b82f-118">Header files</span></span>

<span data-ttu-id="1b82f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b82f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b82f-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1b82f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b82f-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1b82f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1b82f-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1b82f-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b82f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b82f-123">See also</span></span>



[<span data-ttu-id="1b82f-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1b82f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b82f-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1b82f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b82f-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1b82f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b82f-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="1b82f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

