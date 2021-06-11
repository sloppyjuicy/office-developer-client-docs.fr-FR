---
title: Propriété canonique PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734202"
---
# <a name="pidtagcontroltype-canonical-property"></a><span data-ttu-id="67eb5-103">Propriété canonique PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="67eb5-103">PidTagControlType Canonical Property</span></span>

  
  
<span data-ttu-id="67eb5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67eb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67eb5-105">Contient une valeur indiquant un type de contrôle pour un contrôle utilisé dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-105">Contains a value indicating a control type for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67eb5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="67eb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67eb5-107">PR_CONTROL_TYPE</span><span class="sxs-lookup"><span data-stu-id="67eb5-107">PR_CONTROL_TYPE</span></span>  <br/> |
|<span data-ttu-id="67eb5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="67eb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67eb5-109">0x3F02</span><span class="sxs-lookup"><span data-stu-id="67eb5-109">0x3F02</span></span>  <br/> |
|<span data-ttu-id="67eb5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="67eb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="67eb5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="67eb5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="67eb5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="67eb5-112">Area:</span></span>  <br/> |<span data-ttu-id="67eb5-113">Tableau d’affichage MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb5-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67eb5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="67eb5-114">Remarks</span></span>

<span data-ttu-id="67eb5-115">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="67eb5-115">This property can have exactly one of the following values:</span></span>
    
<span data-ttu-id="67eb5-116">DTCT_LABEL (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="67eb5-116">DTCT_LABEL (0x00000000)</span></span>
  
> <span data-ttu-id="67eb5-117">Étiquette de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-117">A dialog label.</span></span>
   
<span data-ttu-id="67eb5-118">DTCT_EDIT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="67eb5-118">DTCT_EDIT (0x00000001)</span></span>
  
> <span data-ttu-id="67eb5-119">Boîte de dialogue de modification de texte.</span><span class="sxs-lookup"><span data-stu-id="67eb5-119">A dialog edit text box.</span></span>

<span data-ttu-id="67eb5-120">DTCT_LBX (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="67eb5-120">DTCT_LBX (0x00000002)</span></span>
  
> <span data-ttu-id="67eb5-121">Boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-121">A dialog list box.</span></span>
    
<span data-ttu-id="67eb5-122">DTCT_COMBOBOX (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="67eb5-122">DTCT_COMBOBOX (0x00000003)</span></span>
  
> <span data-ttu-id="67eb5-123">Zone de liste déroulante de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-123">A dialog combo box.</span></span>

<span data-ttu-id="67eb5-124">DTCT_DDLBX (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="67eb5-124">DTCT_DDLBX (0x00000004)</span></span>
  
> <span data-ttu-id="67eb5-125">Boîte de dialogue de listes.</span><span class="sxs-lookup"><span data-stu-id="67eb5-125">A dialog drop-down list box.</span></span>

<span data-ttu-id="67eb5-126">DTCT_CHECKBOX (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="67eb5-126">DTCT_CHECKBOX (0x00000005)</span></span>
  
> <span data-ttu-id="67eb5-127">Une case à cocher de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-127">A dialog check box.</span></span>

<span data-ttu-id="67eb5-128">DTCT_GROUPBOX (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="67eb5-128">DTCT_GROUPBOX (0x00000006)</span></span>
  
> <span data-ttu-id="67eb5-129">Boîte de dialogue de groupe.</span><span class="sxs-lookup"><span data-stu-id="67eb5-129">A dialog group box.</span></span>
  
<span data-ttu-id="67eb5-130">DTCT_BUTTON (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="67eb5-130">DTCT_BUTTON (0x00000007)</span></span>
  
> <span data-ttu-id="67eb5-131">Contrôle de bouton de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-131">A dialog button control.</span></span>
    
<span data-ttu-id="67eb5-132">DTCT_PAGE (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="67eb5-132">DTCT_PAGE (0x00000008)</span></span>
  
> <span data-ttu-id="67eb5-133">Page à onglets de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-133">A dialog tabbed page.</span></span>
    
<span data-ttu-id="67eb5-134">DTCT_RADIOBUTTON (0x00000009)</span><span class="sxs-lookup"><span data-stu-id="67eb5-134">DTCT_RADIOBUTTON (0x00000009)</span></span>
  
> <span data-ttu-id="67eb5-135">Une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="67eb5-135">A dialog radio button.</span></span>
    
<span data-ttu-id="67eb5-136">DTCT_MVLISTBOX (0x0000000B)</span><span class="sxs-lookup"><span data-stu-id="67eb5-136">DTCT_MVLISTBOX (0x0000000B)</span></span>
  
> <span data-ttu-id="67eb5-137">Zone de liste à valeurs multiples remplie par une propriété à valeurs multiples de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="67eb5-137">A multivalued list box populated by a multivalued property of type string.</span></span>
    
<span data-ttu-id="67eb5-138">DTCT_MVDDLBX (0x0000000C)</span><span class="sxs-lookup"><span data-stu-id="67eb5-138">DTCT_MVDDLBX (0x0000000C)</span></span>
  
> <span data-ttu-id="67eb5-139">Zone de liste de listes à valeurs multiples remplie par une propriété à valeurs multiples de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="67eb5-139">A multivalued drop-down list box populated by a multivalued property of type string.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="67eb5-140">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="67eb5-140">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="67eb5-141">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="67eb5-141">Header files</span></span>

<span data-ttu-id="67eb5-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67eb5-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="67eb5-143">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="67eb5-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="67eb5-144">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67eb5-144">mapitags.h</span></span>
  
> <span data-ttu-id="67eb5-145">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="67eb5-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67eb5-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67eb5-146">See also</span></span>



[<span data-ttu-id="67eb5-147">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb5-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67eb5-148">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb5-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67eb5-149">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb5-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67eb5-150">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="67eb5-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

