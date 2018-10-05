---
title: Propriété canonique PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395531"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="d658a-103">Propriété canonique PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="d658a-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="d658a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d658a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d658a-105">Spécifie le type de réponse à laquelle le destinataire de la demande de partage a répondu.</span><span class="sxs-lookup"><span data-stu-id="d658a-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="d658a-106">Il s’agit d’une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="d658a-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d658a-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d658a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d658a-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="d658a-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="d658a-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d658a-109">Property set:</span></span>  <br/> |<span data-ttu-id="d658a-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="d658a-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d658a-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="d658a-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d658a-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="d658a-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="d658a-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d658a-113">Data type:</span></span>  <br/> |<span data-ttu-id="d658a-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d658a-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d658a-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d658a-115">Area:</span></span>  <br/> |<span data-ttu-id="d658a-116">Partage</span><span class="sxs-lookup"><span data-stu-id="d658a-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d658a-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d658a-117">Remarks</span></span>

<span data-ttu-id="d658a-118">La valeur de cette propriété doit avoir une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d658a-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="d658a-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d658a-119">**Value**</span></span>|<span data-ttu-id="d658a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="d658a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d658a-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d658a-121">0x00000000</span></span>  <br/> |<span data-ttu-id="d658a-122">Aucune réponse</span><span class="sxs-lookup"><span data-stu-id="d658a-122">No response</span></span>  <br/> |
|<span data-ttu-id="d658a-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d658a-123">0x00000001</span></span>  <br/> |<span data-ttu-id="d658a-124">Acceptée</span><span class="sxs-lookup"><span data-stu-id="d658a-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="d658a-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d658a-125">0x00000002</span></span>  <br/> |<span data-ttu-id="d658a-126">Refusé</span><span class="sxs-lookup"><span data-stu-id="d658a-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d658a-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d658a-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d658a-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d658a-128">Protocol specifications</span></span>

<span data-ttu-id="d658a-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d658a-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d658a-130">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d658a-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d658a-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d658a-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d658a-132">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="d658a-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d658a-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d658a-133">Header files</span></span>

<span data-ttu-id="d658a-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d658a-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d658a-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d658a-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d658a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d658a-136">See also</span></span>



[<span data-ttu-id="d658a-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d658a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d658a-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d658a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d658a-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d658a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d658a-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d658a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

