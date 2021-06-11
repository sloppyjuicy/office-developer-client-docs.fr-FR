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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434598"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="4bdd6-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="4bdd6-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="4bdd6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bdd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bdd6-105">Décrit une seule bouton d’radio qui fera partie d’un groupe de boutons d’radio.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="4bdd6-106">Le groupe de boutons d’radio sera utilisé dans une boîte de dialogue qui est conçue à partir d’une table d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4bdd6-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4bdd6-107">Header file:</span></span>  <br/> |<span data-ttu-id="4bdd6-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4bdd6-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="4bdd6-109">Members</span><span class="sxs-lookup"><span data-stu-id="4bdd6-109">Members</span></span>

 <span data-ttu-id="4bdd6-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="4bdd6-111">Position en mémoire de l’étiquette de chaîne de caractères de la bouton d’radio.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="4bdd6-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-112">**ulFlags**</span></span>
  
> <span data-ttu-id="4bdd6-113">Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="4bdd6-114">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="4bdd6-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="4bdd6-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4bdd6-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4bdd6-116">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-116">The label is in Unicode format.</span></span> <span data-ttu-id="4bdd6-117">Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="4bdd6-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="4bdd6-119">Nombre de boutons dans le groupe de boutons d’radio.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="4bdd6-120">Les structures **DTBLRADIOBUTTON pour** les autres boutons du groupe doivent être contenues dans des lignes successives du tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="4bdd6-121">Chacune de ces lignes doit contenir la même valeur pour le **membre ulcButtons.**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="4bdd6-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="4bdd6-123">Balise de propriété pour une propriété de type PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="4bdd6-124">La sélection initiale dans le groupe de boutons d’radio est basée sur la valeur initiale de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="4bdd6-125">Chaque bouton du groupe doit avoir **ulPropTag** définie sur la même propriété.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="4bdd6-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="4bdd6-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="4bdd6-127">Numéro unique qui identifie le bouton sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bdd6-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="4bdd6-128">Remarks</span></span>

<span data-ttu-id="4bdd6-129">Une structure **DTBLRADIOBUTTON** décrit une bouton d’radio un contrôle de bouton associé à un groupe de boutons.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="4bdd6-130">Un seul bouton du groupe peut être vérifié . la définition d’un bouton entraîne l’insé« unset » des autres boutons du groupe.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="4bdd6-131">Le nombre de boutons est le nombre de boutons d’radio dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="4bdd6-132">Les structures des autres boutons d’radio du groupe doivent se trouver dans les lignes suivantes du tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="4bdd6-133">Chacune de ces structures doit avoir la même valeur pour son nombre de boutons.</span><span class="sxs-lookup"><span data-stu-id="4bdd6-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="4bdd6-134">Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="4bdd6-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="4bdd6-135">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="4bdd6-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4bdd6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bdd6-136">See also</span></span>



[<span data-ttu-id="4bdd6-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="4bdd6-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="4bdd6-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="4bdd6-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="4bdd6-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="4bdd6-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="4bdd6-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="4bdd6-140">MAPI Structures</span></span>](mapi-structures.md)

