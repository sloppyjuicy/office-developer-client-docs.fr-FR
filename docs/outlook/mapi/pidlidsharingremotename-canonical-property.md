---
title: Propriété canonique PidLidSharingRemoteName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3be288b606e197b350c1b053303077c1cb984e9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303093"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="8b244-103">Propriété canonique PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="8b244-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="8b244-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b244-105">Spécifie le nom du dossier distant qui est partagé.</span><span class="sxs-lookup"><span data-stu-id="8b244-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="8b244-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="8b244-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b244-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8b244-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b244-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="8b244-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="8b244-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="8b244-109">Property set:</span></span>  <br/> |<span data-ttu-id="8b244-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="8b244-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="8b244-111">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="8b244-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8b244-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="8b244-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="8b244-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8b244-113">Data type:</span></span>  <br/> |<span data-ttu-id="8b244-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8b244-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8b244-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8b244-115">Area:</span></span>  <br/> |<span data-ttu-id="8b244-116">Partage</span><span class="sxs-lookup"><span data-stu-id="8b244-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b244-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b244-117">Remarks</span></span>

<span data-ttu-id="8b244-118">Cette propriété doit être définie sur la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) sur le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="8b244-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b244-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8b244-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b244-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8b244-120">Protocol specifications</span></span>

<span data-ttu-id="8b244-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b244-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b244-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="8b244-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b244-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b244-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b244-124">Partage des dossiers de boîte aux lettres entre clients.</span><span class="sxs-lookup"><span data-stu-id="8b244-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b244-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8b244-125">Header files</span></span>

<span data-ttu-id="8b244-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b244-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b244-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8b244-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b244-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b244-128">See also</span></span>



[<span data-ttu-id="8b244-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8b244-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b244-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8b244-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b244-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8b244-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b244-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8b244-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

