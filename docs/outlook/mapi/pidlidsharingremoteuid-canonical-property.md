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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394733"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="638ae-103">Propriété canonique PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="638ae-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="638ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="638ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="638ae-105">Spécifie l’identificateur d’entrée du dossier partagé distant.</span><span class="sxs-lookup"><span data-stu-id="638ae-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="638ae-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="638ae-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="638ae-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="638ae-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="638ae-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="638ae-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="638ae-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="638ae-109">Property set:</span></span>  <br/> |<span data-ttu-id="638ae-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="638ae-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="638ae-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="638ae-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="638ae-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="638ae-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="638ae-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="638ae-113">Data type:</span></span>  <br/> |<span data-ttu-id="638ae-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="638ae-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="638ae-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="638ae-115">Area:</span></span>  <br/> |<span data-ttu-id="638ae-116">Partage</span><span class="sxs-lookup"><span data-stu-id="638ae-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="638ae-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="638ae-117">Remarks</span></span>

<span data-ttu-id="638ae-118">Cette propriété doit être définie pour la représentation sous forme de chaîne hexadécimale de la valeur de la propriété PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) sur le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="638ae-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="638ae-119">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="638ae-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="638ae-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="638ae-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="638ae-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="638ae-121">Protocol specifications</span></span>

<span data-ttu-id="638ae-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="638ae-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="638ae-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="638ae-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="638ae-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="638ae-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="638ae-125">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="638ae-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="638ae-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="638ae-126">Header files</span></span>

<span data-ttu-id="638ae-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="638ae-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="638ae-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="638ae-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="638ae-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="638ae-129">See also</span></span>



[<span data-ttu-id="638ae-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="638ae-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="638ae-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="638ae-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="638ae-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="638ae-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="638ae-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="638ae-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

