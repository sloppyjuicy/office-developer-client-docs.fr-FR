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
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332605"
---
# <a name="about-error-values"></a><span data-ttu-id="e0cde-103">À propos des valeurs d’erreur</span><span class="sxs-lookup"><span data-stu-id="e0cde-103">About Error Values</span></span>

<span data-ttu-id="e0cde-104">Des valeurs d'erreur s'affichent dans les cellules contenant une formule incorrecte.</span><span class="sxs-lookup"><span data-stu-id="e0cde-104">Error values are displayed in cells that have incorrect formulas for that cell.</span></span>
  
<span data-ttu-id="e0cde-p101">Si une formule fait référence à une cellule qui contient une valeur d'erreur, elle affiche également une valeur d'erreur. Utilisez les fonctions ISERR, ISERRNA, ISERROR ou ISERRVALUE pour déterminer le sens de ces valeurs d'erreur.</span><span class="sxs-lookup"><span data-stu-id="e0cde-p101">If a formula references a cell that contains an error value, that formula also displays an error value. You can use the function ISERR, ISERRNA, ISERROR, or ISERRVALUE to look for error values.</span></span>
  
<span data-ttu-id="e0cde-107">**Valeurs d'erreur**</span><span class="sxs-lookup"><span data-stu-id="e0cde-107">**Error values**</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="e0cde-108">**Si la cellule affiche**</span><span class="sxs-lookup"><span data-stu-id="e0cde-108">**If the cell displays**</span></span> <br/> |<span data-ttu-id="e0cde-109">**La formule contient**</span><span class="sxs-lookup"><span data-stu-id="e0cde-109">**The formula includes**</span></span> <br/> |<span data-ttu-id="e0cde-110">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e0cde-110">**Example**</span></span> <br/> |
| <span data-ttu-id="e0cde-111">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="e0cde-111">#DIV/0!</span></span>  <br/> |<span data-ttu-id="e0cde-112">Une division par 0</span><span class="sxs-lookup"><span data-stu-id="e0cde-112">Division by 0</span></span>  <br/> |<span data-ttu-id="e0cde-113">10/0</span><span class="sxs-lookup"><span data-stu-id="e0cde-113">10/0</span></span>  <br/> |
| <span data-ttu-id="e0cde-114">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="e0cde-114">#VALUE!</span></span>  <br/> | <span data-ttu-id="e0cde-115">Un argument ou un opérande de type incorrect</span><span class="sxs-lookup"><span data-stu-id="e0cde-115">An argument or operand of the wrong type</span></span>  <br/> | <span data-ttu-id="e0cde-116">5 + "Maison"</span><span class="sxs-lookup"><span data-stu-id="e0cde-116">5 + "House"</span></span>  <br/> |
| <span data-ttu-id="e0cde-117">#REF!</span><span class="sxs-lookup"><span data-stu-id="e0cde-117">#REF!</span></span>  <br/> | <span data-ttu-id="e0cde-118">Une référence à une cellule qui n'existe pas</span><span class="sxs-lookup"><span data-stu-id="e0cde-118">A reference to a cell that does not exist</span></span>  <br/> | <span data-ttu-id="e0cde-119">Une cellule faisant référence à une cellule qui n'existe plus</span><span class="sxs-lookup"><span data-stu-id="e0cde-119">A cell that refers to another cell that no longer exists</span></span>  <br/> |
| <span data-ttu-id="e0cde-120">#NUM!</span><span class="sxs-lookup"><span data-stu-id="e0cde-120">#NUM!</span></span>  <br/> | <span data-ttu-id="e0cde-121">Un nombre incorrect</span><span class="sxs-lookup"><span data-stu-id="e0cde-121">An invalid number</span></span>  <br/> | <span data-ttu-id="e0cde-122">La racine carrée d'un nombre négatif</span><span class="sxs-lookup"><span data-stu-id="e0cde-122">Square root of a negative number</span></span>  <br/> |
| <span data-ttu-id="e0cde-123">#N/A!</span><span class="sxs-lookup"><span data-stu-id="e0cde-123">#N/A!</span></span>  <br/> | <span data-ttu-id="e0cde-124">Pas une valeur disponible</span><span class="sxs-lookup"><span data-stu-id="e0cde-124">Not an available value</span></span>  <br/> | <span data-ttu-id="e0cde-125">Fonction NA( )</span><span class="sxs-lookup"><span data-stu-id="e0cde-125">NA( ) function</span></span>  <br/> |
| <span data-ttu-id="e0cde-126">#DIM!</span><span class="sxs-lookup"><span data-stu-id="e0cde-126">#DIM!</span></span>  <br/> | <span data-ttu-id="e0cde-127">Une valeur dimensionnelle qui dépasse la plage de dimensions (les puissances valides sont des \<entiers \<-128 = n = 127)</span><span class="sxs-lookup"><span data-stu-id="e0cde-127">A dimensional value that exceeds the dimension range (valid powers are integers -128 \<= n \<= 127)</span></span>  <br/> <span data-ttu-id="e0cde-128">Une valeur de cote utilisée dans une opération non appropriée</span><span class="sxs-lookup"><span data-stu-id="e0cde-128">A dimensional value used with an inappropriate operation</span></span>  <br/> |<span data-ttu-id="e0cde-129">1Dans ^ 100 \* cm ^ 100 (le résultat est 1 cm ^ 200, qui se trouve au-delà de la plage de dimensions)</span><span class="sxs-lookup"><span data-stu-id="e0cde-129">1in^100 \* 1in^100 (the result is 1in^200, which is beyond the dimension range)</span></span>  <br/> <span data-ttu-id="e0cde-130">5,2 cm^1,5 (la puissance n'est pas un entier)</span><span class="sxs-lookup"><span data-stu-id="e0cde-130">5.2cm^1.5 (not an integer power)</span></span>  <br/> |
   

