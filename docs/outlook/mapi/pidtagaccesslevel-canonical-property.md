---
title: Propriété canonique PidTagAccessLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331996"
---
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="f695a-103">Propriété canonique PidTagAccessLevel</span><span class="sxs-lookup"><span data-stu-id="f695a-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="f695a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f695a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f695a-105">Indique le niveau d’accès du client à l’objet.</span><span class="sxs-lookup"><span data-stu-id="f695a-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f695a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f695a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f695a-107">PR_ACCESS_LEVEL</span><span class="sxs-lookup"><span data-stu-id="f695a-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="f695a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f695a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f695a-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="f695a-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="f695a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f695a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f695a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f695a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f695a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f695a-112">Area:</span></span>  <br/> |<span data-ttu-id="f695a-113">Propriétés du contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="f695a-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f695a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f695a-114">Remarks</span></span>

<span data-ttu-id="f695a-115">Cette propriété est en lecture seule pour le client.</span><span class="sxs-lookup"><span data-stu-id="f695a-115">This property is read-only for the client.</span></span> <span data-ttu-id="f695a-116">Elle doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f695a-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="f695a-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f695a-117">**Value**</span></span>|<span data-ttu-id="f695a-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="f695a-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f695a-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f695a-119">0x00000000</span></span>  <br/> |<span data-ttu-id="f695a-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f695a-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="f695a-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f695a-121">0x00000001</span></span>  <br/> |<span data-ttu-id="f695a-122">Modifier</span><span class="sxs-lookup"><span data-stu-id="f695a-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f695a-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f695a-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f695a-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f695a-124">Protocol specifications</span></span>

<span data-ttu-id="f695a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f695a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f695a-126">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f695a-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f695a-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f695a-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f695a-128">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f695a-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f695a-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f695a-129">Header files</span></span>

<span data-ttu-id="f695a-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f695a-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="f695a-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f695a-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="f695a-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f695a-132">Mapitags.h</span></span>
  
> <span data-ttu-id="f695a-133">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="f695a-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f695a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f695a-134">See also</span></span>



[<span data-ttu-id="f695a-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f695a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f695a-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f695a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f695a-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f695a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f695a-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f695a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

