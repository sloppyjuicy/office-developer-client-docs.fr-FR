---
title: Propriété canonique PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cbe1915df46010c5574065826ac1814f45c8c093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786898"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="266c1-103">Propriété canonique PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="266c1-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="266c1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="266c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="266c1-105">Détermine la nécessité pour transmettre des après le traitement d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="266c1-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="266c1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="266c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="266c1-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="266c1-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="266c1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="266c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="266c1-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="266c1-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="266c1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="266c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="266c1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="266c1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="266c1-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="266c1-112">Area:</span></span>  <br/> |<span data-ttu-id="266c1-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="266c1-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="266c1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="266c1-114">Remarks</span></span>

<span data-ttu-id="266c1-115">Si cette propriété est définie sur un brouillon de message, sa valeur doit être définie à la valeur de la propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="266c1-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="266c1-116">Pour plus d’informations, voir [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section » après la transmission d’un Message avec indicateur de traitement. »</span><span class="sxs-lookup"><span data-stu-id="266c1-116">For more information, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="266c1-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="266c1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="266c1-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="266c1-118">Protocol specifications</span></span>

<span data-ttu-id="266c1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="266c1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="266c1-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="266c1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="266c1-121">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="266c1-121">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="266c1-122">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="266c1-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="266c1-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="266c1-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="266c1-124">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="266c1-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="266c1-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="266c1-125">Header files</span></span>

<span data-ttu-id="266c1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="266c1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="266c1-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="266c1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="266c1-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="266c1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="266c1-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="266c1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="266c1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="266c1-130">See also</span></span>



[<span data-ttu-id="266c1-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="266c1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="266c1-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="266c1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="266c1-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="266c1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="266c1-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="266c1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

