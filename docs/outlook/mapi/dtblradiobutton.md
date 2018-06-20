---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783235"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="c84bc-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="c84bc-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="c84bc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c84bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c84bc-105">Décrit une case d’option doit faire partie d’un groupe de boutons radio.</span><span class="sxs-lookup"><span data-stu-id="c84bc-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="c84bc-106">Le groupe de boutons radio permettra dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c84bc-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c84bc-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c84bc-107">Header file:</span></span>  <br/> |<span data-ttu-id="c84bc-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c84bc-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a><span data-ttu-id="c84bc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c84bc-109">Members</span></span>

 <span data-ttu-id="c84bc-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="c84bc-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="c84bc-111">Position dans la mémoire de l’étiquette de chaîne de caractères pour le bouton d’option.</span><span class="sxs-lookup"><span data-stu-id="c84bc-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="c84bc-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c84bc-112">**ulFlags**</span></span>
  
> <span data-ttu-id="c84bc-113">Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="c84bc-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="c84bc-114">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="c84bc-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="c84bc-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c84bc-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c84bc-116">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c84bc-116">The label is in Unicode format.</span></span> <span data-ttu-id="c84bc-117">Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c84bc-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="c84bc-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="c84bc-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="c84bc-119">Nombre de boutons dans le groupe de boutons radio.</span><span class="sxs-lookup"><span data-stu-id="c84bc-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="c84bc-120">Les structures **DTBLRADIOBUTTON** pour les autres boutons dans le groupe doivent être contenues dans les lignes de la table d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c84bc-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="c84bc-121">Chacune de ces lignes doit contenir la même valeur pour le membre **ulcButtons** .</span><span class="sxs-lookup"><span data-stu-id="c84bc-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="c84bc-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c84bc-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="c84bc-123">Balise de propriété pour une propriété de type PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="c84bc-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="c84bc-124">La sélection dans le groupe de bouton radio initiale est basée sur la valeur initiale de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c84bc-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="c84bc-125">Chaque bouton dans le groupe doit avoir **ulPropTag** à la même propriété.</span><span class="sxs-lookup"><span data-stu-id="c84bc-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="c84bc-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="c84bc-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="c84bc-127">Numéro unique qui identifie le bouton sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c84bc-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c84bc-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="c84bc-128">Remarks</span></span>

<span data-ttu-id="c84bc-129">Une structure **DTBLRADIOBUTTON** décrit une case d’option un contrôle bouton qui est associé à un groupe de boutons.</span><span class="sxs-lookup"><span data-stu-id="c84bc-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="c84bc-130">Seul le bouton dans le groupe peut être archivé ; un bouton provoque les autres boutons dans le groupe est annulée.</span><span class="sxs-lookup"><span data-stu-id="c84bc-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="c84bc-131">Le nombre de bouton est le nombre de cases d’option dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="c84bc-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="c84bc-132">Les structures pour les autres cases dans le groupe doivent être dans les lignes suivantes dans le tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c84bc-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="c84bc-133">Chacun de ces structures doit avoir la même valeur pour le nombre de boutons.</span><span class="sxs-lookup"><span data-stu-id="c84bc-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="c84bc-134">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c84bc-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c84bc-135">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c84bc-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c84bc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c84bc-136">See also</span></span>



[<span data-ttu-id="c84bc-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="c84bc-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="c84bc-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c84bc-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="c84bc-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="c84bc-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="c84bc-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c84bc-140">MAPI Structures</span></span>](mapi-structures.md)

