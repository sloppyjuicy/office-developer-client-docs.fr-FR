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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fed2b23680cd2654bbb6960e3c6be07074307a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786692"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="d08ee-103">Propriété canonique PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="d08ee-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="d08ee-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d08ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d08ee-105">Contient les noms des délégués.</span><span class="sxs-lookup"><span data-stu-id="d08ee-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d08ee-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d08ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d08ee-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="d08ee-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="d08ee-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d08ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d08ee-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="d08ee-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="d08ee-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d08ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="d08ee-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d08ee-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d08ee-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="d08ee-112">Area:</span></span>  <br/> |<span data-ttu-id="d08ee-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="d08ee-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d08ee-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d08ee-114">Remarks</span></span>

<span data-ttu-id="d08ee-115">Chaque entrée de ces propriétés doit contenir la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d’adresses de chaque délégué.</span><span class="sxs-lookup"><span data-stu-id="d08ee-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d08ee-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d08ee-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d08ee-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d08ee-117">Protocol specifications</span></span>

<span data-ttu-id="d08ee-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d08ee-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d08ee-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="d08ee-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d08ee-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d08ee-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d08ee-121">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d08ee-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d08ee-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d08ee-122">Header files</span></span>

<span data-ttu-id="d08ee-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d08ee-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d08ee-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d08ee-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d08ee-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d08ee-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d08ee-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d08ee-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d08ee-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d08ee-127">See also</span></span>



[<span data-ttu-id="d08ee-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d08ee-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d08ee-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d08ee-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d08ee-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d08ee-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d08ee-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d08ee-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

