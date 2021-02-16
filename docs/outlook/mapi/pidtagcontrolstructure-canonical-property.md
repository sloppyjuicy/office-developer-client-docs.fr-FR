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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cf91620042f916d51f27be50d15f72db537ad5f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412946"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="39e29-103">Propriété canonique PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="39e29-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="39e29-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39e29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39e29-105">Contient un pointeur vers une structure pour un contrôle utilisé dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="39e29-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39e29-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="39e29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39e29-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="39e29-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="39e29-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39e29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39e29-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="39e29-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="39e29-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="39e29-110">Data type:</span></span>  <br/> |<span data-ttu-id="39e29-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39e29-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39e29-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="39e29-112">Area:</span></span>  <br/> |<span data-ttu-id="39e29-113">Tableau d’affichage MAPI</span><span class="sxs-lookup"><span data-stu-id="39e29-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39e29-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="39e29-114">Remarks</span></span>

<span data-ttu-id="39e29-115">Cette propriété représente un pointeur long qui est casté vers l’une des structures de contrôle.</span><span class="sxs-lookup"><span data-stu-id="39e29-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="39e29-116">Les structures de contrôle sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="39e29-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="39e29-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="39e29-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="39e29-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="39e29-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="39e29-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="39e29-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="39e29-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="39e29-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="39e29-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="39e29-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="39e29-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="39e29-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="39e29-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="39e29-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="39e29-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="39e29-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="39e29-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="39e29-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="39e29-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="39e29-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="39e29-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="39e29-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="39e29-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="39e29-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="39e29-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="39e29-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="39e29-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="39e29-130">Header files</span></span>

<span data-ttu-id="39e29-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39e29-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="39e29-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="39e29-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="39e29-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39e29-133">Mapitags.h</span></span>
  
> <span data-ttu-id="39e29-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="39e29-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39e29-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39e29-135">See also</span></span>



[<span data-ttu-id="39e29-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="39e29-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39e29-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="39e29-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39e29-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="39e29-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39e29-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="39e29-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

