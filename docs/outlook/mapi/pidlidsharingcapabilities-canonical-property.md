---
title: Propriété canonique PidLidSharingCapabilities
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d44851e1c863cb117eed3462eb98de87f8d1f0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358890"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="dedca-103">Propriété canonique PidLidSharingCapabilities</span><span class="sxs-lookup"><span data-stu-id="dedca-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="dedca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dedca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dedca-105">Désigne comme propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="dedca-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dedca-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="dedca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dedca-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="dedca-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="dedca-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="dedca-108">Property set:</span></span>  <br/> |<span data-ttu-id="dedca-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="dedca-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="dedca-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="dedca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dedca-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="dedca-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="dedca-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dedca-112">Data type:</span></span>  <br/> |<span data-ttu-id="dedca-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dedca-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dedca-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dedca-114">Area:</span></span>  <br/> |<span data-ttu-id="dedca-115">Partage</span><span class="sxs-lookup"><span data-stu-id="dedca-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dedca-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="dedca-116">Remarks</span></span>

<span data-ttu-id="dedca-117">Cette propriété doit être définie sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dedca-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="dedca-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dedca-118">**Value**</span></span>|<span data-ttu-id="dedca-119">**Scénario**</span><span class="sxs-lookup"><span data-stu-id="dedca-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dedca-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="dedca-120">0x00040290</span></span>  <br/> |<span data-ttu-id="dedca-121">Cet objet Message de partage est lié à un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="dedca-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="dedca-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="dedca-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="dedca-123">Cet objet Message de partage n’est pas lié à un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="dedca-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dedca-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dedca-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dedca-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="dedca-125">Protocol specifications</span></span>

<span data-ttu-id="dedca-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dedca-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dedca-127">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="dedca-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dedca-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dedca-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dedca-129">Partage des dossiers de boîte aux lettres entre clients.</span><span class="sxs-lookup"><span data-stu-id="dedca-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dedca-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dedca-130">Header files</span></span>

<span data-ttu-id="dedca-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dedca-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="dedca-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dedca-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dedca-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dedca-133">See also</span></span>



[<span data-ttu-id="dedca-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dedca-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dedca-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dedca-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dedca-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dedca-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dedca-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dedca-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

