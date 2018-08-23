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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f7521d387fa45c191a67f2a20320fac700baed37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567215"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="6b2ef-103">Propriété canonique PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="6b2ef-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="6b2ef-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b2ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b2ef-105">Contient **identificateurs d’entrée** des délégués.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b2ef-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6b2ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b2ef-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="6b2ef-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="6b2ef-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6b2ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b2ef-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="6b2ef-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="6b2ef-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6b2ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b2ef-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="6b2ef-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="6b2ef-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6b2ef-112">Area:</span></span>  <br/> |<span data-ttu-id="6b2ef-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="6b2ef-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b2ef-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b2ef-114">Remarks</span></span>

<span data-ttu-id="6b2ef-115">Chaque entrée doit contenir la valeur de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d’entrée de carnet d’adresses de chaque délégué.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="6b2ef-116">Cette propriété doit être définie dans l’objet d’informations de délégué.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6b2ef-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6b2ef-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b2ef-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6b2ef-118">Protocol specifications</span></span>

<span data-ttu-id="6b2ef-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b2ef-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b2ef-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b2ef-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b2ef-121">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b2ef-122">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b2ef-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6b2ef-123">Header files</span></span>

<span data-ttu-id="6b2ef-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b2ef-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b2ef-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b2ef-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6b2ef-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6b2ef-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b2ef-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b2ef-128">See also</span></span>



[<span data-ttu-id="6b2ef-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6b2ef-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b2ef-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6b2ef-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b2ef-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6b2ef-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b2ef-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6b2ef-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

