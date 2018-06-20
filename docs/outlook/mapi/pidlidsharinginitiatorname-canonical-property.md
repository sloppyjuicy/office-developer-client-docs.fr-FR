---
title: Propriété canonique PidLidSharingInitiatorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1b20c2171f77451d9b7e85573260acff3243238f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785406"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="3fa4d-103">Propriété canonique PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="3fa4d-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="3fa4d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3fa4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3fa4d-105">Désigne comme une propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="3fa4d-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fa4d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3fa4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fa4d-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="3fa4d-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="3fa4d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3fa4d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3fa4d-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="3fa4d-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="3fa4d-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="3fa4d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3fa4d-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="3fa4d-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="3fa4d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3fa4d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3fa4d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3fa4d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3fa4d-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="3fa4d-114">Area:</span></span>  <br/> |<span data-ttu-id="3fa4d-115">Partage</span><span class="sxs-lookup"><span data-stu-id="3fa4d-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fa4d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fa4d-116">Remarks</span></span>

<span data-ttu-id="3fa4d-117">Cette propriété doit être définie à la valeur de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir du carnet d’adresses identifié par **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="3fa4d-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3fa4d-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3fa4d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3fa4d-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3fa4d-119">Protocol specifications</span></span>

<span data-ttu-id="3fa4d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fa4d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fa4d-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="3fa4d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3fa4d-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fa4d-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fa4d-123">Partage des dossiers de boîte aux lettres entre des clients.</span><span class="sxs-lookup"><span data-stu-id="3fa4d-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3fa4d-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3fa4d-124">Header files</span></span>

<span data-ttu-id="3fa4d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3fa4d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3fa4d-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3fa4d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3fa4d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fa4d-127">See also</span></span>



[<span data-ttu-id="3fa4d-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3fa4d-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3fa4d-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3fa4d-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3fa4d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

