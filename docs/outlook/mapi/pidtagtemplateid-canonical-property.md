---
title: Propriété canonique PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358820"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="ac8f0-103">Propriété canonique PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="ac8f0-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="ac8f0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac8f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac8f0-105">Contient le **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), exprimé sous la forme d’un format d’ID d’entrée permanent.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac8f0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ac8f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac8f0-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="ac8f0-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="ac8f0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ac8f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac8f0-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="ac8f0-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="ac8f0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ac8f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac8f0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac8f0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac8f0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ac8f0-112">Area:</span></span>  <br/> |<span data-ttu-id="ac8f0-113">Carnet d'adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8f0-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac8f0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac8f0-114">Remarks</span></span>

<span data-ttu-id="ac8f0-115">Cette valeur doit être présente pour tous les objets de carnet d’adresses sur un serveur NSPI (Name Service Provider Interface), son nom unique (DN) doit correspondre à la valeur de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), et son nom unique doit respecter la spécification de format DN spécifique au type d’objet.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="ac8f0-116">Cette propriété n’est pas présente sur les objets d’un carnet d’adresses en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac8f0-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ac8f0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac8f0-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ac8f0-118">Protocol specifications</span></span>

<span data-ttu-id="ac8f0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac8f0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac8f0-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac8f0-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac8f0-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac8f0-122">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac8f0-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ac8f0-123">Header files</span></span>

<span data-ttu-id="ac8f0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac8f0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac8f0-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac8f0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac8f0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ac8f0-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ac8f0-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac8f0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac8f0-128">See also</span></span>



[<span data-ttu-id="ac8f0-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8f0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac8f0-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8f0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac8f0-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8f0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac8f0-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ac8f0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

