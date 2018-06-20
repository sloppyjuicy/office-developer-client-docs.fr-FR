---
title: Propriété canonique PidTagControlStructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785875"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="c5a47-103">Propriété canonique PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="c5a47-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="c5a47-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5a47-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5a47-105">Contient un pointeur vers une structure d’un contrôle utilisé dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c5a47-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5a47-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c5a47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5a47-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="c5a47-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="c5a47-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c5a47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5a47-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="c5a47-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="c5a47-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c5a47-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5a47-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c5a47-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c5a47-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c5a47-112">Area:</span></span>  <br/> |<span data-ttu-id="c5a47-113">Afficher une table MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a47-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5a47-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5a47-114">Remarks</span></span>

<span data-ttu-id="c5a47-115">Cette propriété représente un pointeur de type long qui est converti à une des structures de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c5a47-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="c5a47-116">Les structures de contrôle sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5a47-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="c5a47-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="c5a47-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="c5a47-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="c5a47-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="c5a47-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="c5a47-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="c5a47-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="c5a47-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="c5a47-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="c5a47-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="c5a47-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="c5a47-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="c5a47-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="c5a47-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="c5a47-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="c5a47-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="c5a47-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="c5a47-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="c5a47-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="c5a47-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="c5a47-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="c5a47-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="c5a47-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="c5a47-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c5a47-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c5a47-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c5a47-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c5a47-130">Header files</span></span>

<span data-ttu-id="c5a47-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5a47-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5a47-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c5a47-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5a47-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c5a47-133">Mapitags.h</span></span>
  
> <span data-ttu-id="c5a47-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c5a47-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5a47-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5a47-135">See also</span></span>



[<span data-ttu-id="c5a47-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a47-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5a47-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a47-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5a47-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a47-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5a47-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c5a47-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

