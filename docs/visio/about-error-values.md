---
title: À propos des valeurs d'erreur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Des valeurs d'erreur s'affichent dans les cellules contenant une formule incorrecte.
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787975"
---
# <a name="about-error-values"></a><span data-ttu-id="93830-103">À propos des valeurs d'erreur</span><span class="sxs-lookup"><span data-stu-id="93830-103">About Error Values</span></span>

<span data-ttu-id="93830-104">Des valeurs d'erreur s'affichent dans les cellules contenant une formule incorrecte.</span><span class="sxs-lookup"><span data-stu-id="93830-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="93830-p101">Si une formule fait référence à une cellule qui contient une valeur d'erreur, elle affiche également une valeur d'erreur. Utilisez les fonctions ISERR, ISERRNA, ISERROR ou ISERRVALUE pour déterminer le sens de ces valeurs d'erreur.</span><span class="sxs-lookup"><span data-stu-id="93830-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="93830-107">**Valeurs d’erreur**</span><span class="sxs-lookup"><span data-stu-id="93830-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="93830-108">**Si la cellule affiche**</span><span class="sxs-lookup"><span data-stu-id="93830-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="93830-109">**La formule contient**</span><span class="sxs-lookup"><span data-stu-id="93830-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="93830-110">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="93830-110">**Example**</span></span> <br/> |
| <span data-ttu-id="93830-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="93830-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="93830-112">Division par 0</span><span class="sxs-lookup"><span data-stu-id="93830-112">Division by 0</span></span>  <br/> |<span data-ttu-id="93830-113">10/0</span><span class="sxs-lookup"><span data-stu-id="93830-113">10/0</span></span>  <br/> |
| <span data-ttu-id="93830-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="93830-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="93830-115">Un argument ou un opérande de type incorrect</span><span class="sxs-lookup"><span data-stu-id="93830-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="93830-116">5 + « Maison »</span><span class="sxs-lookup"><span data-stu-id="93830-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="93830-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="93830-117">#REF!</span></span>  <br/> | <span data-ttu-id="93830-118">Une référence à une cellule qui n’existe pas</span><span class="sxs-lookup"><span data-stu-id="93830-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="93830-119">Une cellule qui fait référence à une cellule qui n’existe plus</span><span class="sxs-lookup"><span data-stu-id="93830-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="93830-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="93830-120">#NUM!</span></span>  <br/> | <span data-ttu-id="93830-121">Un nombre non valide</span><span class="sxs-lookup"><span data-stu-id="93830-121">An invalid number</span></span>  <br/> | <span data-ttu-id="93830-122">Racine carrée d’un nombre négatif</span><span class="sxs-lookup"><span data-stu-id="93830-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="93830-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="93830-123">#N/A!</span></span>  <br/> | <span data-ttu-id="93830-124">Pas une valeur disponible</span><span class="sxs-lookup"><span data-stu-id="93830-124">Not an available value</span></span>  <br/> | <span data-ttu-id="93830-125">Fonction NA)</span><span class="sxs-lookup"><span data-stu-id="93830-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="93830-126">#DIM !</span><span class="sxs-lookup"><span data-stu-id="93830-126">#DIM!</span></span>  <br/> | <span data-ttu-id="93830-127">Une valeur de cote qui dépasse la plage autorisée (les puissances correctes sont des entiers -128 \<= n \<= 127)</span><span class="sxs-lookup"><span data-stu-id="93830-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="93830-128">Une valeur de cote utilisée avec une opération non appropriée</span><span class="sxs-lookup"><span data-stu-id="93830-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="93830-129">1 en ^ 100 \* 1 en ^ 100 (le résultat est 1 dans ^ 200, qui dépasse la plage des cotes)</span><span class="sxs-lookup"><span data-stu-id="93830-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="93830-130">5,2 cm ^ 1,5 (pas une puissance entière)</span><span class="sxs-lookup"><span data-stu-id="93830-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

