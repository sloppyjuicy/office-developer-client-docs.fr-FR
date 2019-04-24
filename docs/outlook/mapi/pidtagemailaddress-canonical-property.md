---
title: Propriété canonique PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338639"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="39df9-103">Propriété canonique PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="39df9-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="39df9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39df9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39df9-105">Contient l'adresse de messagerie de l'utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="39df9-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39df9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="39df9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39df9-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="39df9-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="39df9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39df9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39df9-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="39df9-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="39df9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="39df9-110">Data type:</span></span>  <br/> |<span data-ttu-id="39df9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39df9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="39df9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="39df9-112">Area:</span></span>  <br/> |<span data-ttu-id="39df9-113">MAPI commun</span><span class="sxs-lookup"><span data-stu-id="39df9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39df9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="39df9-114">Remarks</span></span>

<span data-ttu-id="39df9-115">Ces propriétés sont des exemples de propriétés d'adresse de base pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="39df9-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="39df9-116">Il s'agit d'une chaîne terminée par un caractère null dont le format n'a de sens que pour le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="39df9-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="39df9-117">Ces propriétés sont utilisées conjointement avec les propriétés **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) et **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) dans Addressing messages.</span><span class="sxs-lookup"><span data-stu-id="39df9-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="39df9-118">Le format de chaîne est qualifié par **PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="39df9-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="39df9-119">Les valeurs valides pour cette propriété sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="39df9-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="39df9-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="39df9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39df9-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="39df9-121">Protocol specifications</span></span>

<span data-ttu-id="39df9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39df9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39df9-123">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="39df9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39df9-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39df9-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39df9-125">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="39df9-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="39df9-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39df9-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39df9-127">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="39df9-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39df9-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="39df9-128">Header files</span></span>

<span data-ttu-id="39df9-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="39df9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="39df9-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="39df9-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="39df9-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="39df9-131">Mapitags.h</span></span>
  
> <span data-ttu-id="39df9-132">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="39df9-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39df9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39df9-133">See also</span></span>



[<span data-ttu-id="39df9-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="39df9-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39df9-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="39df9-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39df9-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="39df9-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39df9-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="39df9-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

