---
title: Propriété canonique PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 06462f992ec640992b95b89a618e7d82290eeeef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574502"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="973d3-103">Propriété canonique PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="973d3-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="973d3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="973d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="973d3-105">Contient les noms des délégués.</span><span class="sxs-lookup"><span data-stu-id="973d3-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="973d3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="973d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="973d3-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="973d3-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="973d3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="973d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="973d3-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="973d3-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="973d3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="973d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="973d3-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="973d3-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="973d3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="973d3-112">Area:</span></span>  <br/> |<span data-ttu-id="973d3-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="973d3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="973d3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="973d3-114">Remarks</span></span>

<span data-ttu-id="973d3-115">Chaque entrée de ces propriétés doit contenir la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d’adresses de chaque délégué.</span><span class="sxs-lookup"><span data-stu-id="973d3-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="973d3-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="973d3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="973d3-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="973d3-117">Protocol specifications</span></span>

<span data-ttu-id="973d3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="973d3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="973d3-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="973d3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="973d3-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="973d3-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="973d3-121">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="973d3-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="973d3-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="973d3-122">Header files</span></span>

<span data-ttu-id="973d3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="973d3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="973d3-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="973d3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="973d3-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="973d3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="973d3-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="973d3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="973d3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="973d3-127">See also</span></span>



[<span data-ttu-id="973d3-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="973d3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="973d3-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="973d3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="973d3-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="973d3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="973d3-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="973d3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

