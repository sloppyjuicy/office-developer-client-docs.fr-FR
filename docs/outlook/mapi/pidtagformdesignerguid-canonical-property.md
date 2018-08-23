---
title: Propriété canonique PidTagFormDesignerGuid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 30c8f31c104be52da2900eb81c7b7c29dfa55015
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586528"
---
# <a name="pidtagformdesignerguid-canonical-property"></a><span data-ttu-id="107d7-103">Propriété canonique PidTagFormDesignerGuid</span><span class="sxs-lookup"><span data-stu-id="107d7-103">PidTagFormDesignerGuid Canonical Property</span></span>

  
  
<span data-ttu-id="107d7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="107d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="107d7-105">Contient l’identificateur unique de l’objet qui est utilisé pour créer un formulaire.</span><span class="sxs-lookup"><span data-stu-id="107d7-105">Contains the unique identifier for the object that is used to design a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="107d7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="107d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="107d7-107">PR_FORM_DESIGNER_GUID</span><span class="sxs-lookup"><span data-stu-id="107d7-107">PR_FORM_DESIGNER_GUID</span></span>  <br/> |
|<span data-ttu-id="107d7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="107d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="107d7-109">0x3309</span><span class="sxs-lookup"><span data-stu-id="107d7-109">0x3309</span></span>  <br/> |
|<span data-ttu-id="107d7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="107d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="107d7-111">PT_GUID</span><span class="sxs-lookup"><span data-stu-id="107d7-111">PT_GUID</span></span>  <br/> |
|<span data-ttu-id="107d7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="107d7-112">Area:</span></span>  <br/> |<span data-ttu-id="107d7-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="107d7-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="107d7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="107d7-114">Remarks</span></span>

<span data-ttu-id="107d7-115">Généralement, cette propriété contient l’identificateur global unique (GUID) du programme de conception qui est utilisé pour créer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="107d7-115">This property usually contains the globally unique identifier (GUID) of the design program that is used to create the form.</span></span> <span data-ttu-id="107d7-116">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="107d7-116">This property can be empty.</span></span> 
  
<span data-ttu-id="107d7-117">La structure [MAPIUID](mapiuid.md) contient la définition de l’identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="107d7-117">The [MAPIUID](mapiuid.md) structure contains the definition of the unique identifier.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="107d7-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="107d7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="107d7-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="107d7-119">Header files</span></span>

<span data-ttu-id="107d7-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="107d7-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="107d7-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="107d7-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="107d7-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="107d7-122">Mapitags.h</span></span>
  
> <span data-ttu-id="107d7-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="107d7-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="107d7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="107d7-124">See also</span></span>



[<span data-ttu-id="107d7-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="107d7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="107d7-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="107d7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="107d7-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="107d7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="107d7-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="107d7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

