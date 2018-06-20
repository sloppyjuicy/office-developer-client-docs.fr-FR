---
title: Propriété canonique PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cb8b4a7c71f3ad81949f3eac6cab230f40c6d487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785416"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="7608c-103">Propriété canonique PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="7608c-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="7608c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7608c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7608c-105">Spécifie l’identificateur d’entrée du dossier partagé distant.</span><span class="sxs-lookup"><span data-stu-id="7608c-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="7608c-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="7608c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7608c-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7608c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="7608c-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="7608c-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="7608c-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="7608c-109">Property set:</span></span>  <br/> |<span data-ttu-id="7608c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="7608c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="7608c-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="7608c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7608c-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="7608c-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="7608c-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7608c-113">Data type:</span></span>  <br/> |<span data-ttu-id="7608c-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7608c-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7608c-115">Zone :</span><span class="sxs-lookup"><span data-stu-id="7608c-115">Area:</span></span>  <br/> |<span data-ttu-id="7608c-116">Partage</span><span class="sxs-lookup"><span data-stu-id="7608c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7608c-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7608c-117">Remarks</span></span>

<span data-ttu-id="7608c-118">Cette propriété doit être définie pour la représentation sous forme de chaîne hexadécimale de la valeur de la propriété PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) sur le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="7608c-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="7608c-119">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="7608c-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7608c-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7608c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7608c-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7608c-121">Protocol specifications</span></span>

<span data-ttu-id="7608c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7608c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7608c-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="7608c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7608c-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7608c-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7608c-125">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="7608c-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7608c-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7608c-126">Header files</span></span>

<span data-ttu-id="7608c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7608c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7608c-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7608c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7608c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7608c-129">See also</span></span>



[<span data-ttu-id="7608c-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7608c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7608c-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7608c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7608c-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7608c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7608c-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="7608c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

