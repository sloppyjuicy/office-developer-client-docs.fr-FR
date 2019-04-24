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
ms.openlocfilehash: d106a216e8d72c126f3293f9d492db73992c3872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355292"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="80aad-103">Propriété canonique PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="80aad-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="80aad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80aad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80aad-105">Contient la clé de recherche d'origine pour une entrée copiée à partir d'un carnet d'adresses dans un carnet d'adresses personnel ou dans un autre carnet d'adresses accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="80aad-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80aad-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="80aad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80aad-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="80aad-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="80aad-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="80aad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80aad-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="80aad-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="80aad-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="80aad-110">Data type:</span></span>  <br/> |<span data-ttu-id="80aad-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="80aad-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="80aad-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="80aad-112">Area:</span></span>  <br/> |<span data-ttu-id="80aad-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="80aad-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80aad-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="80aad-114">Remarks</span></span>

<span data-ttu-id="80aad-115">Cette propriété est une des propriétés qui contiennent des informations sur la source d'origine d'une entrée copiée.</span><span class="sxs-lookup"><span data-stu-id="80aad-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="80aad-116">Pour un rapport non lu, cette propriété contient une copie de la clé de recherche du destinataire du message d'origine pour lequel le rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="80aad-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="80aad-117">Lorsque le destinataire d'origine fait partie d'une liste de distribution, la clé de recherche de la liste de distribution est préservée pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="80aad-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80aad-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="80aad-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80aad-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="80aad-119">Protocol specifications</span></span>

<span data-ttu-id="80aad-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80aad-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80aad-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="80aad-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80aad-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80aad-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80aad-123">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="80aad-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80aad-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="80aad-124">Header files</span></span>

<span data-ttu-id="80aad-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="80aad-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="80aad-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="80aad-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="80aad-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="80aad-127">Mapitags.h</span></span>
  
> <span data-ttu-id="80aad-128">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="80aad-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80aad-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80aad-129">See also</span></span>



[<span data-ttu-id="80aad-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="80aad-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80aad-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="80aad-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80aad-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="80aad-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80aad-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="80aad-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

