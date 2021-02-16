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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336847"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="f845b-103">Propriété canonique PidLidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="f845b-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="f845b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f845b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f845b-105">Désigne comme propriété d’un message de partage.</span><span class="sxs-lookup"><span data-stu-id="f845b-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f845b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f845b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f845b-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="f845b-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="f845b-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f845b-108">Property set:</span></span>  <br/> |<span data-ttu-id="f845b-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="f845b-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="f845b-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="f845b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f845b-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="f845b-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="f845b-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f845b-112">Data type:</span></span>  <br/> |<span data-ttu-id="f845b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f845b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f845b-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f845b-114">Area:</span></span>  <br/> |<span data-ttu-id="f845b-115">Partage</span><span class="sxs-lookup"><span data-stu-id="f845b-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f845b-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f845b-116">Remarks</span></span>

<span data-ttu-id="f845b-117">Cette propriété doit être définie sur la valeur **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir du carnet d’adresses identifié par **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) et doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="f845b-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f845b-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f845b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f845b-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f845b-119">Protocol specifications</span></span>

<span data-ttu-id="f845b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f845b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f845b-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f845b-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f845b-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f845b-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f845b-123">Partage des dossiers de boîte aux lettres entre clients.</span><span class="sxs-lookup"><span data-stu-id="f845b-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f845b-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f845b-124">Header files</span></span>

<span data-ttu-id="f845b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f845b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f845b-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f845b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f845b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f845b-127">See also</span></span>



[<span data-ttu-id="f845b-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f845b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f845b-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f845b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f845b-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f845b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f845b-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f845b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

