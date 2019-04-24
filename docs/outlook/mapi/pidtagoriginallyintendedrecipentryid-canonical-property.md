---
title: Propriété canonique PidTagOriginallyIntendedRecipEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342524"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="febe1-103">Propriété canonique PidTagOriginallyIntendedRecipEntryId</span><span class="sxs-lookup"><span data-stu-id="febe1-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="febe1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="febe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="febe1-105">Contient l'identificateur d'entrée du destinataire initial d'un message transféré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="febe1-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="febe1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="febe1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="febe1-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="febe1-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="febe1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="febe1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="febe1-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="febe1-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="febe1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="febe1-110">Data type:</span></span>  <br/> |<span data-ttu-id="febe1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="febe1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="febe1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="febe1-112">Area:</span></span>  <br/> |<span data-ttu-id="febe1-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="febe1-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="febe1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="febe1-114">Remarks</span></span>

<span data-ttu-id="febe1-115">Cette propriété est l'une des propriétés d'adresse pour le destinataire du message initialement prévu.</span><span class="sxs-lookup"><span data-stu-id="febe1-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="febe1-116">Elle doit être définie par l'agent automatique qui a transféré le message.</span><span class="sxs-lookup"><span data-stu-id="febe1-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="febe1-117">Cette propriété correspond à l'attribut par destinataire du rapport X. 400.</span><span class="sxs-lookup"><span data-stu-id="febe1-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="febe1-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="febe1-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="febe1-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="febe1-119">Header files</span></span>

<span data-ttu-id="febe1-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="febe1-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="febe1-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="febe1-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="febe1-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="febe1-122">Mapitags.h</span></span>
  
> <span data-ttu-id="febe1-123">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="febe1-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="febe1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="febe1-124">See also</span></span>



[<span data-ttu-id="febe1-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="febe1-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="febe1-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="febe1-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="febe1-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="febe1-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="febe1-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="febe1-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

