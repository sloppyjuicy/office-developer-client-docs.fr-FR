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
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331261"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="20242-103">Propriété canonique PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="20242-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="20242-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20242-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20242-105">Spécifie l'ID d'entrée du dossier distant partagé.</span><span class="sxs-lookup"><span data-stu-id="20242-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="20242-106">Il s'agit d'une propriété d'un message de partage.</span><span class="sxs-lookup"><span data-stu-id="20242-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20242-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="20242-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="20242-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="20242-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="20242-109">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="20242-109">Property set:</span></span>  <br/> |<span data-ttu-id="20242-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="20242-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="20242-111">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="20242-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="20242-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="20242-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="20242-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="20242-113">Data type:</span></span>  <br/> |<span data-ttu-id="20242-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="20242-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="20242-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="20242-115">Area:</span></span>  <br/> |<span data-ttu-id="20242-116">Partage</span><span class="sxs-lookup"><span data-stu-id="20242-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20242-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="20242-117">Remarks</span></span>

<span data-ttu-id="20242-118">Cette propriété doit être définie sur la représentation sous forme de chaîne hexadécimale de la valeur de la propriété PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) sur le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="20242-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="20242-119">Il s'agit d'une propriété d'un message de partage.</span><span class="sxs-lookup"><span data-stu-id="20242-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20242-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="20242-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20242-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="20242-121">Protocol specifications</span></span>

<span data-ttu-id="20242-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20242-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20242-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="20242-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20242-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20242-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20242-125">Partage des dossiers de boîtes aux lettres entre les clients.</span><span class="sxs-lookup"><span data-stu-id="20242-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20242-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="20242-126">Header files</span></span>

<span data-ttu-id="20242-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="20242-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="20242-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="20242-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20242-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20242-129">See also</span></span>



[<span data-ttu-id="20242-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="20242-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20242-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="20242-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20242-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="20242-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20242-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="20242-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

