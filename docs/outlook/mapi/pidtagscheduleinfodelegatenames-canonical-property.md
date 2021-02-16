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
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314937"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="d6b1f-103">Propriété canonique PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="d6b1f-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="d6b1f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6b1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6b1f-105">Contient les noms des délégués.</span><span class="sxs-lookup"><span data-stu-id="d6b1f-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6b1f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d6b1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6b1f-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="d6b1f-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="d6b1f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d6b1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6b1f-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="d6b1f-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="d6b1f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d6b1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6b1f-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6b1f-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d6b1f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d6b1f-112">Area:</span></span>  <br/> |<span data-ttu-id="d6b1f-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="d6b1f-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6b1f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6b1f-114">Remarks</span></span>

<span data-ttu-id="d6b1f-115">Chaque entrée de ces propriétés doit contenir la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d’adresses de chaque délégué.</span><span class="sxs-lookup"><span data-stu-id="d6b1f-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d6b1f-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d6b1f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6b1f-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d6b1f-117">Protocol specifications</span></span>

<span data-ttu-id="d6b1f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6b1f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6b1f-119">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="d6b1f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6b1f-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6b1f-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6b1f-121">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6b1f-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6b1f-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d6b1f-122">Header files</span></span>

<span data-ttu-id="d6b1f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6b1f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6b1f-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d6b1f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6b1f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6b1f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d6b1f-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d6b1f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6b1f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6b1f-127">See also</span></span>



[<span data-ttu-id="d6b1f-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b1f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6b1f-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b1f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6b1f-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b1f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6b1f-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d6b1f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

