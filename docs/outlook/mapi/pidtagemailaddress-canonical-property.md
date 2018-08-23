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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f70d5fbe9a52c491d5db668f541ce317f2675c6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569042"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="8401e-103">Propriété canonique PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8401e-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8401e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8401e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8401e-105">Contient l’adresse de messagerie de l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8401e-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8401e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8401e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8401e-107">ADRESSE_EMAIL_PR, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="8401e-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="8401e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8401e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8401e-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="8401e-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="8401e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8401e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8401e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8401e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8401e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8401e-112">Area:</span></span>  <br/> |<span data-ttu-id="8401e-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="8401e-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8401e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8401e-114">Remarks</span></span>

<span data-ttu-id="8401e-115">Ces propriétés sont des exemples de propriétés d’adresse de base pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8401e-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="8401e-116">Il est une chaîne dont le format a de signification seulement pour le système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8401e-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="8401e-117">Ces propriétés sont utilisées conjointement avec les propriétés **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) dans les messages d’adressage **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8401e-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="8401e-118">Le format de chaîne est qualifié par **TYPEADR_PR**.</span><span class="sxs-lookup"><span data-stu-id="8401e-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="8401e-119">Les valeurs valides pour cette propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8401e-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="8401e-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8401e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8401e-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8401e-121">Protocol specifications</span></span>

<span data-ttu-id="8401e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8401e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8401e-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8401e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8401e-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8401e-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8401e-125">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="8401e-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="8401e-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8401e-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8401e-127">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="8401e-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8401e-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8401e-128">Header files</span></span>

<span data-ttu-id="8401e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8401e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="8401e-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8401e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="8401e-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8401e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="8401e-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8401e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8401e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8401e-133">See also</span></span>



[<span data-ttu-id="8401e-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8401e-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8401e-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8401e-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8401e-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8401e-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8401e-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8401e-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

