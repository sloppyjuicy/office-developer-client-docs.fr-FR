---
title: À propos des formules
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Les actions sur les formes sont commandées au moyen de formules que vous écrivez pour définir le comportement désiré. Vous pouvez modifier la formule d’une cellule pour en changer la valeur, et modifier ainsi le comportement d’une forme particulière. Par exemple, la cellule Height de la section Shape Transform contient une formule que vous pouvez modifier pour changer la hauteur de la forme.
ms.openlocfilehash: 7df5ffe4d3dc32bcd5209bde353c39a92c7d422b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787974"
---
# <a name="about-formulas"></a><span data-ttu-id="9ff86-105">À propos des formules</span><span class="sxs-lookup"><span data-stu-id="9ff86-105">About Formulas</span></span>

<span data-ttu-id="9ff86-p102">Les actions sur les formes sont commandées au moyen de formules que vous écrivez pour définir le comportement désiré. Vous pouvez modifier la formule d’une cellule pour en changer la valeur, et modifier ainsi le comportement d’une forme particulière. Par exemple, la cellule Height de la section Shape Transform contient une formule que vous pouvez modifier pour changer la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="9ff86-p102">The key to controlling shape actions is to write formulas that define the behavior you want. You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior. For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="9ff86-p103">Les formules Microsoft Visio ressemblent à de nombreux égards aux formules classiques des feuilles de calcul. Visio considère tout ce qui apparaît dans une cellule, même une valeur numérique ou une simple référence à une autre cellule, comme une formule.</span><span class="sxs-lookup"><span data-stu-id="9ff86-p103">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways. Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="9ff86-p104">La formule d’une cellule peut être héritée de la cellule équivalente d’une forme de base ou d’un style, ou être définie localement. Visio évalue la formule puis en convertit les résultats en la valeur appropriée dans l’unité adaptée pour la cellule. Dans une fenêtre Feuille ShapeSheet, vous pouvez afficher le contenu des cellules sous la forme de formules ou de valeurs.</span><span class="sxs-lookup"><span data-stu-id="9ff86-p104">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally. Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell. In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="9ff86-114">Éléments d’une formule</span><span class="sxs-lookup"><span data-stu-id="9ff86-114">Elements of a formula</span></span>

<span data-ttu-id="9ff86-p105">Une formule commence toujours par un signe égal qui est inséré automatiquement. Une formule peut comprendre un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9ff86-p105">A formula always starts with an equal sign, which is inserted automatically. A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="9ff86-117">Nombres</span><span class="sxs-lookup"><span data-stu-id="9ff86-117">Numbers</span></span>
    
- <span data-ttu-id="9ff86-118">Coordonnées</span><span class="sxs-lookup"><span data-stu-id="9ff86-118">Coordinates</span></span>
    
- <span data-ttu-id="9ff86-119">Valeurs booléennes</span><span class="sxs-lookup"><span data-stu-id="9ff86-119">Boolean values</span></span>
    
- <span data-ttu-id="9ff86-120">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="9ff86-120">Operators</span></span>
    
- <span data-ttu-id="9ff86-121">Fonctions</span><span class="sxs-lookup"><span data-stu-id="9ff86-121">Functions</span></span>
    
- <span data-ttu-id="9ff86-122">Chaînes</span><span class="sxs-lookup"><span data-stu-id="9ff86-122">Strings</span></span>
    
- <span data-ttu-id="9ff86-123">Références de cellule</span><span class="sxs-lookup"><span data-stu-id="9ff86-123">Cell references</span></span>
    
- <span data-ttu-id="9ff86-124">Unités de mesure</span><span class="sxs-lookup"><span data-stu-id="9ff86-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="9ff86-125">Formules par défaut</span><span class="sxs-lookup"><span data-stu-id="9ff86-125">Default formulas</span></span>

<span data-ttu-id="9ff86-126">Lorsque vous créez une forme, Visio crée pour celle-ci des formules par défaut.</span><span class="sxs-lookup"><span data-stu-id="9ff86-126">When you create a shape, Visio creates formulas for it by default.</span></span> <span data-ttu-id="9ff86-127">Pour voir quels sont les formules par défaut, dessine une forme simple (comme un rectangle, une ellipse ou une ligne droite) et ouvrez sa fenêtre feuille ShapeSheet (sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , cliquez sur **Afficher la feuille ShapeSheet**).</span><span class="sxs-lookup"><span data-stu-id="9ff86-127">To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="9ff86-128">Formules héritées</span><span class="sxs-lookup"><span data-stu-id="9ff86-128">Inherited formulas</span></span>

<span data-ttu-id="9ff86-p107">Visio applique l’héritage des formules chaque fois que possible. Au lieu de copier localement chaque formule de l’instance, cette instance hérite des formules de sa forme de base dans le gabarit du document et de sa mise en forme dans les définitions de style enregistrées avec le dessin. Cette méthode permet de réduire la taille des fichiers, mais aussi de propager à toutes les instances les modifications de formules de la forme de base ou de la définition de style.</span><span class="sxs-lookup"><span data-stu-id="9ff86-p107">Visio inherits formulas whenever possible. Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing. This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="9ff86-132">Du texte en noir dans une cellule indique une formule héritée.</span><span class="sxs-lookup"><span data-stu-id="9ff86-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="9ff86-133">Formules locales</span><span class="sxs-lookup"><span data-stu-id="9ff86-133">Local formulas</span></span>

<span data-ttu-id="9ff86-p108">Lorsque vous écrivez une formule locale pour une instance, vous remplacez la formule héritée par une formule locale dans la cellule. Les modifications apportées par la suite à cette cellule dans la forme de base ou dans le style n’affectent pas cette instance étant donné que la formule locale a annulé l’héritage.</span><span class="sxs-lookup"><span data-stu-id="9ff86-p108">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override. Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="9ff86-136">L’application d’un style supprime toutes les formules locales des cellules concernées sauf si vous utilisez la fonction GUARD pour les protéger.</span><span class="sxs-lookup"><span data-stu-id="9ff86-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="9ff86-137">Le texte en bleu indique une formule locale, résultat de la modification de la formule dans une fenêtre Feuille ShapeSheet ou de modifications de la forme ayant amené Visio à redéfinir la formule de cette cellule.</span><span class="sxs-lookup"><span data-stu-id="9ff86-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="9ff86-138">Mises à jour automatiques des formules</span><span class="sxs-lookup"><span data-stu-id="9ff86-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="9ff86-p109">Visio met automatiquement à jour certaines cellules à chaque modification d’une forme dans un dessin. Ainsi, dans certaines circonstances, les formules que vous avez entrées peuvent être remplacées. Par exemple, si vous faites glisser une poignée de coin pour redimensionner une forme, Visio redéfinit les formules des cellules PinX, PinY, Width et Height.</span><span class="sxs-lookup"><span data-stu-id="9ff86-p109">Visio automatically updates certain cells whenever you change a shape in a drawing. This means that under some circumstances formulas you enter can be replaced. For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="9ff86-142">Au besoin, vous pouvez protéger les formules locales à l’aide de la fonction GUARD.</span><span class="sxs-lookup"><span data-stu-id="9ff86-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

