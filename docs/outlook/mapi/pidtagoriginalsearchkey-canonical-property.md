---
title: Propriété canonique PidTagOriginalSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 26854b640669bbc6479ce90ba9cad18cdf4d9264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786343"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="c991f-103">Propriété canonique PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="c991f-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="c991f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c991f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c991f-105">Contient la clé de recherche d’origine pour une entrée copiée à partir d’un carnet d’adresses à un carnet d’adresses personnel ou autre carnet d’adresses accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="c991f-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c991f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c991f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c991f-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="c991f-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="c991f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c991f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c991f-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="c991f-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="c991f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c991f-110">Data type:</span></span>  <br/> |<span data-ttu-id="c991f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c991f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c991f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c991f-112">Area:</span></span>  <br/> |<span data-ttu-id="c991f-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="c991f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c991f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c991f-114">Remarks</span></span>

<span data-ttu-id="c991f-115">Cette propriété est une des propriétés qui contiennent des informations sur la source d’origine d’une entrée copiée.</span><span class="sxs-lookup"><span data-stu-id="c991f-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="c991f-116">Pour un rapport nonread, cette propriété contient une copie de la clé de recherche du destinataire du message d’origine pour lequel le rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="c991f-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="c991f-117">Lorsque le destinataire d’origine fait partie d’une liste de distribution, la clé de recherche de la liste de distribution est conservée pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="c991f-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c991f-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c991f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c991f-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c991f-119">Protocol specifications</span></span>

<span data-ttu-id="c991f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c991f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c991f-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c991f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c991f-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c991f-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c991f-123">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="c991f-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c991f-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c991f-124">Header files</span></span>

<span data-ttu-id="c991f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c991f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c991f-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c991f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c991f-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c991f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c991f-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c991f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c991f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c991f-129">See also</span></span>



[<span data-ttu-id="c991f-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c991f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c991f-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c991f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c991f-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c991f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c991f-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c991f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

