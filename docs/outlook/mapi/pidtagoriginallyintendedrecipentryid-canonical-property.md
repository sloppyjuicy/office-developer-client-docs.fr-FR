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
ms.openlocfilehash: 4745318d5666cc3c138f424c94bc2c5e430a61d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786312"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="c9636-103">Propriété canonique PidTagOriginallyIntendedRecipEntryId</span><span class="sxs-lookup"><span data-stu-id="c9636-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c9636-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9636-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9636-105">Contient l’identificateur d’entrée du destinataire prévu à l’origine d’un message envoyé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c9636-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9636-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c9636-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9636-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c9636-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c9636-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c9636-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9636-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="c9636-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="c9636-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c9636-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9636-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9636-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c9636-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c9636-112">Area:</span></span>  <br/> |<span data-ttu-id="c9636-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="c9636-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9636-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9636-114">Remarks</span></span>

<span data-ttu-id="c9636-115">Cette propriété est une des propriétés d’adresse pour le destinataire du message à l’origine.</span><span class="sxs-lookup"><span data-stu-id="c9636-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="c9636-116">Elle doit être définie par l’agent automatique qui a transféré le message.</span><span class="sxs-lookup"><span data-stu-id="c9636-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="c9636-117">Cette propriété correspond à l’attribut par destinataire du rapport X.400.</span><span class="sxs-lookup"><span data-stu-id="c9636-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9636-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c9636-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9636-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c9636-119">Header files</span></span>

<span data-ttu-id="c9636-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9636-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9636-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c9636-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9636-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c9636-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c9636-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="c9636-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9636-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9636-124">See also</span></span>



[<span data-ttu-id="c9636-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c9636-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9636-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c9636-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9636-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c9636-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9636-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c9636-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

