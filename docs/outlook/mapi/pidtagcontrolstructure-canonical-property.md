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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b517888d562ee5b178dbd011fa1ce6ab218c6b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594354"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="1ae05-103">Propriété canonique PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="1ae05-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="1ae05-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ae05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ae05-105">Contient un pointeur vers une structure d’un contrôle utilisé dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1ae05-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ae05-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1ae05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ae05-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="1ae05-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="1ae05-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1ae05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ae05-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="1ae05-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="1ae05-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1ae05-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ae05-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ae05-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1ae05-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1ae05-112">Area:</span></span>  <br/> |<span data-ttu-id="1ae05-113">Afficher une table MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae05-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ae05-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1ae05-114">Remarks</span></span>

<span data-ttu-id="1ae05-115">Cette propriété représente un pointeur de type long qui est converti à une des structures de contrôle.</span><span class="sxs-lookup"><span data-stu-id="1ae05-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="1ae05-116">Les structures de contrôle sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ae05-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="1ae05-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ae05-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="1ae05-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="1ae05-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="1ae05-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="1ae05-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="1ae05-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="1ae05-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="1ae05-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="1ae05-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="1ae05-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="1ae05-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="1ae05-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="1ae05-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="1ae05-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="1ae05-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="1ae05-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="1ae05-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="1ae05-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="1ae05-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="1ae05-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="1ae05-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="1ae05-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ae05-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1ae05-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1ae05-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1ae05-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1ae05-130">Header files</span></span>

<span data-ttu-id="1ae05-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ae05-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ae05-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1ae05-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ae05-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1ae05-133">Mapitags.h</span></span>
  
> <span data-ttu-id="1ae05-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1ae05-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ae05-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae05-135">See also</span></span>



[<span data-ttu-id="1ae05-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae05-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ae05-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae05-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ae05-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae05-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ae05-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1ae05-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

