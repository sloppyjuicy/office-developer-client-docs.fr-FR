---
title: SETATREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Redirige les valeurs mises à jour résultant d'actions dans l'interface utilisateur (IU) ou l'automatisation vers une autre cellule.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326018"
---
# <a name="setatref-function"></a><span data-ttu-id="dec27-103">Fonction SETATREF</span><span class="sxs-lookup"><span data-stu-id="dec27-103">SETATREF Function</span></span>

<span data-ttu-id="dec27-104">Redirige les valeurs mises à jour résultant d'actions dans l'interface utilisateur (IU) ou l'automatisation vers une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="dec27-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dec27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dec27-105">Syntax</span></span>

<span data-ttu-id="dec27-106">SETATREF (\* \* *référence* \* \* [, \* \* *expression_données* \* \* [, \* \* *ignore_eval* \* \*]])</span><span class="sxs-lookup"><span data-stu-id="dec27-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dec27-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dec27-107">Parameters</span></span>

|<span data-ttu-id="dec27-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dec27-108">**Name**</span></span>|<span data-ttu-id="dec27-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="dec27-109">**Required/Optional**</span></span>|<span data-ttu-id="dec27-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="dec27-110">**Data Type**</span></span>|<span data-ttu-id="dec27-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="dec27-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dec27-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="dec27-112">_reference_</span></span> <br/> |<span data-ttu-id="dec27-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dec27-113">Required</span></span>  <br/> |<span data-ttu-id="dec27-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dec27-114">**String**</span></span> <br/> |<span data-ttu-id="dec27-115">Référence à une cellule vers laquelle les mises à jour sont redirigées.</span><span class="sxs-lookup"><span data-stu-id="dec27-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="dec27-116">_Set_Expression_</span><span class="sxs-lookup"><span data-stu-id="dec27-116">_set_expression_</span></span> <br/> |<span data-ttu-id="dec27-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dec27-117">Optional</span></span>  <br/> |<span data-ttu-id="dec27-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="dec27-118">**String**</span></span> <br/> |<span data-ttu-id="dec27-119">Expression assignée à _Reference_.</span><span class="sxs-lookup"><span data-stu-id="dec27-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="dec27-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="dec27-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="dec27-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dec27-121">Optional</span></span>  <br/> |<span data-ttu-id="dec27-122">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="dec27-122">**Boolean**</span></span> <br/> |<span data-ttu-id="dec27-123">Si la valeur est TRUE, la fonction SETATREF évalue à (0) zéro; Si la valeur est FALSe (valeur par défaut), la fonction SETATREF évalue la valeur de _Reference_.</span><span class="sxs-lookup"><span data-stu-id="dec27-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dec27-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="dec27-124">Remarks</span></span>

<span data-ttu-id="dec27-125">Lorsqu'une action utilisateur dans la fenêtre de dessin, ou une méthode Automation, entraîne la mise à jour par Microsoft Visio d'une cellule contenant une formule SETATREF, la valeur est redirigée vers la cellule référencée par la formule SETATREF ( _référence_).</span><span class="sxs-lookup"><span data-stu-id="dec27-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="dec27-126">La formule dans la cellule contenant la fonction SETATREF reste intacte.</span><span class="sxs-lookup"><span data-stu-id="dec27-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="dec27-127">Si _set_expression_ est omis, la valeur définie dans l'interface utilisateur ou à l'aide de l'automatisation est assignée à la cellule référencée; dans le cas contraire, le contenu de _set_expression_ est affecté à la cellule référencée.</span><span class="sxs-lookup"><span data-stu-id="dec27-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="dec27-128">Cela permet à la nouvelle valeur d’être modifiée ou transformée avant d’être attribuée à cette cellule.</span><span class="sxs-lookup"><span data-stu-id="dec27-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="dec27-129">La fonction SETATREF possède deux fonctions connexes :</span><span class="sxs-lookup"><span data-stu-id="dec27-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="dec27-130">La fonction SETATREFEXPR, que vous pouvez utiliser pour représenter la nouvelle valeur dans _set_expression_.</span><span class="sxs-lookup"><span data-stu-id="dec27-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="dec27-131">Par exemple, un _set_expression_ de SETATREFEXPR ()-2 dans.</span><span class="sxs-lookup"><span data-stu-id="dec27-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="dec27-132">peut être utilisé pour soustraire 2 pouces du résultat SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="dec27-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="dec27-133">La fonction SETATREFEVAL, que vous pouvez utiliser pour indiquer qu'une partie de _set_expression_ doit être évaluée et remplacée par son résultat.</span><span class="sxs-lookup"><span data-stu-id="dec27-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="dec27-134">La fonction SETATREF est conçue pour une utilisation dans les cellules qui peuvent être modifiées par les actions de l'utilisateur dans la fenêtre de dessin.</span><span class="sxs-lookup"><span data-stu-id="dec27-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="dec27-135">Les cellules suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="dec27-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="dec27-136">Section ShapeTransform — cellules Width, Height, Angle, PinX et PinY</span><span class="sxs-lookup"><span data-stu-id="dec27-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="dec27-137">Section Text Transform — cellules TxtWidth, TxtHeight, TxtAngle, TxtPinX et TxtPinY</span><span class="sxs-lookup"><span data-stu-id="dec27-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="dec27-138">Section 1-D Endpoints — cellules BeginX, BeginY, EndX et EndY</span><span class="sxs-lookup"><span data-stu-id="dec27-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="dec27-139">Section Controls — cellules Controls.X et Controls.Y</span><span class="sxs-lookup"><span data-stu-id="dec27-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="dec27-140">Section Shape Data</span><span class="sxs-lookup"><span data-stu-id="dec27-140">Shape Data section</span></span>
    
<span data-ttu-id="dec27-141">Étant donné que SETATREF modifie l’emplacement où les valeurs de cellules changent, cela affecte le déclenchement des événements.</span><span class="sxs-lookup"><span data-stu-id="dec27-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="dec27-142">Si une cellule contient SETATREF, les événements **FormulaChanged** et **CellChanged** s’appliquent à la cellule référencée par SETATREF et non à celle contenant SETATREF.</span><span class="sxs-lookup"><span data-stu-id="dec27-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="dec27-143">Si une cellule contenant SETATREF contient également SETATREFEXPR, l'événement **FormulaChanged** se déclenche également pour la cellule contenant SETATREF car un paramètre de fonction est modifié.</span><span class="sxs-lookup"><span data-stu-id="dec27-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="dec27-144">Autres informations importantes à connaître à propos de la fonction SETATREF :</span><span class="sxs-lookup"><span data-stu-id="dec27-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="dec27-145">Les fonctions SETATREF peuvent attacher jusqu’à 10 références à d’autres fonctions SETATREF.</span><span class="sxs-lookup"><span data-stu-id="dec27-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="dec27-146">Outre la fonction SETATREF, y compris plusieurs occurrences de SETATREF dans une cellule unique, les cellules peuvent contenir d’autres expressions.</span><span class="sxs-lookup"><span data-stu-id="dec27-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="dec27-147">Si des formes sont collées, Visio suit la chaîne de référence SETATREF dans la même feuille et place des formules de colle dans la cellule référencée.</span><span class="sxs-lookup"><span data-stu-id="dec27-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="dec27-148">Automation reconnaît la fonction SETATREF et suit la chaîne de cellules référencées.</span><span class="sxs-lookup"><span data-stu-id="dec27-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="dec27-149">À l’instar de GUARD, SETATREF ne protège pas les cellules des changements effectués à l’aide de la fonction SETF dans la feuille Shapesheet.</span><span class="sxs-lookup"><span data-stu-id="dec27-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="dec27-150">Exemple1</span><span class="sxs-lookup"><span data-stu-id="dec27-150">Example1</span></span>

<span data-ttu-id="dec27-151">Supposons qu’une forme dispose d’une propriété personnalisée appelée Width et que la cellule Width de la section Shape Transform contient la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="dec27-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="dec27-152">= SETATREF (Prop. Width)</span><span class="sxs-lookup"><span data-stu-id="dec27-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="dec27-153">Si un utilisateur modifie la largeur de la forme dans l'interface utilisateur, la nouvelle valeur est affectée à la cellule prop. Width, et non à la cellule Width de la section ShapeTransform; la formule dans la cellule Width reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="dec27-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="dec27-154">Vous pouvez également définir la largeur de la forme en utilisant des données de forme.</span><span class="sxs-lookup"><span data-stu-id="dec27-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="dec27-155">Example2</span><span class="sxs-lookup"><span data-stu-id="dec27-155">Example2</span></span>

<span data-ttu-id="dec27-p107">Les solutions Visio ont souvent des formes dotées de relations hiérarchiques, nécessitant que les formes enfant soient déplacées lorsqu’une forme parente l’est également. Voici un exemple indiquant comment vous pouvez gérer cette relation à l’aide de la fonction SETATREF dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="dec27-p107">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved. Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="dec27-p108">Les formules suivantes sont contenues dans la section Shape Transform de la forme enfant. Ainsi, nous définissons les cellules utilisateur appelées User.DeltaX et User.DeltaY qui assurent la dimension de décalage à partir de ParentShape. Cela permet à la forme enfant d’être déplacée en même temps que la forme parent mais aussi de préserver la relation hiérarchique si la forme enfant est déplacée.</span><span class="sxs-lookup"><span data-stu-id="dec27-p108">The following formulas are contained in the Shape Transform section of the child shape. Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape. This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="dec27-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span><span class="sxs-lookup"><span data-stu-id="dec27-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="dec27-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span><span class="sxs-lookup"><span data-stu-id="dec27-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="dec27-163">Lorsque la forme enfant est déplacée à l'aide de l'interface utilisateur, les nouvelles valeurs PinX et PinY sont définies en tant que paramètre dans la fonction SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="dec27-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="dec27-164">La fonction SETATREF évalue la formule incluse dans SETATREFEVAL et remplace PinX et PinY par leurs résultats, puis la formule résultante est affectée aux cellules utilisateur référencées dans la fonction SETATREF: User. DeltaX et User. deltaY.</span><span class="sxs-lookup"><span data-stu-id="dec27-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="dec27-165">Enfin, les valeurs retournées par SETATREF (User. DeltaX ou User. deltaY) sont ajoutées à l'emplacement du code confidentiel de ParentShape pour calculer l'emplacement du code confidentiel de la forme enfant.</span><span class="sxs-lookup"><span data-stu-id="dec27-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

