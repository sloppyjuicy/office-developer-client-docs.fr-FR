---
title: Propriété canonique PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4a43bc33f13d8325a55d09b5ef3031dc632cf587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786305"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="0841b-103">Propriété canonique PidTagOriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="0841b-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="0841b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0841b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0841b-105">Contient le nom complet d’origine pour une entrée copié à partir d’un carnet d’adresses dans un carnet d’adresses personnel ou autre carnet d’adresses accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="0841b-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0841b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0841b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0841b-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="0841b-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="0841b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0841b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0841b-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="0841b-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="0841b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0841b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0841b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0841b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0841b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="0841b-112">Area:</span></span>  <br/> |<span data-ttu-id="0841b-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="0841b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0841b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0841b-114">Remarks</span></span>

<span data-ttu-id="0841b-115">Ces propriétés contiennent des informations sur la source d’origine d’une entrée copiée.</span><span class="sxs-lookup"><span data-stu-id="0841b-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="0841b-116">Pour un rapport nonread, ces propriétés contiennent une copie du nom complet du destinataire du message d’origine pour lequel le rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="0841b-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="0841b-117">Lorsque le destinataire d’origine fait partie d’une liste de distribution, le nom complet de la liste de distribution est conservé pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="0841b-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="0841b-118">Une application cliente peut utiliser ces propriétés pour éviter toute altération ou « usurpation d’identité » des entrées, en donnant une copie intacte du nom complet à comparer.</span><span class="sxs-lookup"><span data-stu-id="0841b-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0841b-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0841b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0841b-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0841b-120">Protocol specifications</span></span>

<span data-ttu-id="0841b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0841b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0841b-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0841b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0841b-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0841b-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0841b-124">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="0841b-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0841b-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0841b-125">Header files</span></span>

<span data-ttu-id="0841b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0841b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0841b-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0841b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0841b-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0841b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0841b-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0841b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0841b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0841b-130">See also</span></span>



[<span data-ttu-id="0841b-131">Propriété canonique PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="0841b-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="0841b-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0841b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0841b-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0841b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0841b-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0841b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0841b-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0841b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

