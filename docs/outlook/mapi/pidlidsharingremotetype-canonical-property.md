---
title: Propriété canonique PidLidSharingRemoteType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8a9975090a8b90946482fa77fd2dafdb503c1f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785418"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="9b659-103">Propriété canonique PidLidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="9b659-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="9b659-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b659-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b659-105">Spécifie le type du dossier partagé à distance.</span><span class="sxs-lookup"><span data-stu-id="9b659-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="9b659-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="9b659-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b659-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9b659-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b659-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="9b659-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="9b659-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="9b659-109">Property set:</span></span>  <br/> |<span data-ttu-id="9b659-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="9b659-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="9b659-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="9b659-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9b659-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="9b659-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="9b659-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9b659-113">Data type:</span></span>  <br/> |<span data-ttu-id="9b659-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b659-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b659-115">Zone :</span><span class="sxs-lookup"><span data-stu-id="9b659-115">Area:</span></span>  <br/> |<span data-ttu-id="9b659-116">Partage</span><span class="sxs-lookup"><span data-stu-id="9b659-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b659-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9b659-117">Remarks</span></span>

<span data-ttu-id="9b659-118">Cette propriété doit avoir la même valeur que la propriété **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="9b659-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9b659-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9b659-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b659-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9b659-120">Protocol specifications</span></span>

<span data-ttu-id="9b659-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b659-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b659-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9b659-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b659-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b659-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b659-124">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="9b659-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b659-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9b659-125">Header files</span></span>

<span data-ttu-id="9b659-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b659-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b659-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9b659-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b659-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b659-128">See also</span></span>



[<span data-ttu-id="9b659-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9b659-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b659-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9b659-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b659-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9b659-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b659-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9b659-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

