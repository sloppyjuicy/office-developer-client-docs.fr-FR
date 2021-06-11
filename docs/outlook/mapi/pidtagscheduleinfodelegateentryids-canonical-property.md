---
title: Propriété canonique PidTagScheduleInfoDelegateEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321293"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="04e3a-103">Propriété canonique PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="04e3a-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="04e3a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04e3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04e3a-105">Contient les **EntryIDs** des délégués.</span><span class="sxs-lookup"><span data-stu-id="04e3a-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04e3a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="04e3a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04e3a-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="04e3a-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="04e3a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="04e3a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04e3a-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="04e3a-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="04e3a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="04e3a-110">Data type:</span></span>  <br/> |<span data-ttu-id="04e3a-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="04e3a-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="04e3a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="04e3a-112">Area:</span></span>  <br/> |<span data-ttu-id="04e3a-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="04e3a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04e3a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="04e3a-114">Remarks</span></span>

<span data-ttu-id="04e3a-115">Chaque entrée doit contenir la valeur de la **propriété PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de l’entrée de carnet d’adresses de chaque délégué.</span><span class="sxs-lookup"><span data-stu-id="04e3a-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="04e3a-116">Cette propriété doit être définie dans l’objet d’informations du délégué.</span><span class="sxs-lookup"><span data-stu-id="04e3a-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04e3a-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="04e3a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04e3a-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="04e3a-118">Protocol specifications</span></span>

<span data-ttu-id="04e3a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04e3a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04e3a-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="04e3a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04e3a-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04e3a-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04e3a-122">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04e3a-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04e3a-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="04e3a-123">Header files</span></span>

<span data-ttu-id="04e3a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04e3a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="04e3a-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="04e3a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="04e3a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="04e3a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="04e3a-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="04e3a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04e3a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e3a-128">See also</span></span>



[<span data-ttu-id="04e3a-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="04e3a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04e3a-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="04e3a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04e3a-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="04e3a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04e3a-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="04e3a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

