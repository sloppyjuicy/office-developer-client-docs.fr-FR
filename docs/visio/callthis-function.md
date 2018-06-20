---
title: CALLTHIS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Appelle une procédure dans un Microsoft Visual Basic pour Applications (VBA) project.
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788186"
---
# <a name="callthis-function"></a><span data-ttu-id="d89df-103">CALLTHIS, fonction</span><span class="sxs-lookup"><span data-stu-id="d89df-103">CALLTHIS Function</span></span>

<span data-ttu-id="d89df-104">Appelle une procédure dans un Microsoft Visual Basic pour Applications (VBA) project.</span><span class="sxs-lookup"><span data-stu-id="d89df-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d89df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d89df-105">Syntax</span></span>

<span data-ttu-id="d89df-106">CALLTHIS (« ** *procédure* ** », [« ** *project* ** »], [** *arg1* **, ** *arg2* **,...])</span><span class="sxs-lookup"><span data-stu-id="d89df-106">CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d89df-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d89df-107">Parameters</span></span>

|<span data-ttu-id="d89df-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d89df-108">**Name**</span></span>|<span data-ttu-id="d89df-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d89df-109">**Required/Optional**</span></span>|<span data-ttu-id="d89df-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d89df-110">**Data Type**</span></span>|<span data-ttu-id="d89df-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d89df-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d89df-112">_procédure_</span><span class="sxs-lookup"><span data-stu-id="d89df-112">_procedure_</span></span> <br/> |<span data-ttu-id="d89df-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d89df-113">Required</span></span>  <br/> |<span data-ttu-id="d89df-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d89df-114">**String**</span></span> <br/> | <span data-ttu-id="d89df-115">Nom de la procédure à appeler.</span><span class="sxs-lookup"><span data-stu-id="d89df-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="d89df-116">_projet_</span><span class="sxs-lookup"><span data-stu-id="d89df-116">_project_</span></span> <br/> |<span data-ttu-id="d89df-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d89df-117">Optional</span></span>  <br/> |<span data-ttu-id="d89df-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d89df-118">**String**</span></span> <br/> |<span data-ttu-id="d89df-119">Projet qui contient la procédure.</span><span class="sxs-lookup"><span data-stu-id="d89df-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="d89df-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="d89df-120">_arg_</span></span> <br/> |<span data-ttu-id="d89df-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d89df-121">Optional</span></span>  <br/> |<span data-ttu-id="d89df-122">**Nombre, chaîne, Date ou Currency**</span><span class="sxs-lookup"><span data-stu-id="d89df-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="d89df-123">Transmis comme paramètres à la procédure.</span><span class="sxs-lookup"><span data-stu-id="d89df-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d89df-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="d89df-124">Remarks</span></span>

<span data-ttu-id="d89df-125">Dans le projet VBA, *procedure* est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="d89df-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="d89df-126">procédure (*vsoShape* en tant que Visio.Shape [arg1 que vous tapez, arg2 en tant que type...])</span><span class="sxs-lookup"><span data-stu-id="d89df-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="d89df-127">où *vsoShape* est une référence à l’objet **Shape** qui contient la formule CALLTHIS calculée et _arg1_, *arg2* ... sont les arguments indiqués dans cette formule.</span><span class="sxs-lookup"><span data-stu-id="d89df-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="d89df-128">Notez que *vsoShape* est très semblable à l’argument « this » transmis à une procédure C++ ; Par conséquent, le nom « CALLTHIS ».</span><span class="sxs-lookup"><span data-stu-id="d89df-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="d89df-129">En effet, une cellule contenant une formule qui inclut CALLTHIS peut se lire, « Appeler cette procédure et lui transmettre une référence à ma forme ».</span><span class="sxs-lookup"><span data-stu-id="d89df-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="d89df-130">Si le _projet_ est spécifié, Microsoft Visio recherche tous les documents ouverts pour l’un contenant _project_ et appelle la _procédure_ dans ce projet.</span><span class="sxs-lookup"><span data-stu-id="d89df-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="d89df-131">Si le _projet_ est omis ou nul (« »), Visio suppose que la _procédure_ se trouve dans le projet VBA du document contenant la formule CALLTHIS qui est évaluée.</span><span class="sxs-lookup"><span data-stu-id="d89df-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="d89df-132">Les nombres de _arg1_, _arg2..._ sont transmis en unités externes.</span><span class="sxs-lookup"><span data-stu-id="d89df-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="d89df-133">Par exemple, si vous transmettez la valeur de la cellule Height à partir d’une forme haute de 3 cm, 3 est transmise.</span><span class="sxs-lookup"><span data-stu-id="d89df-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="d89df-134">Pour transmettre différentes unités avec un nombre, utilisez la fonction FORMATEX ou définissez explicitement unités en ajoutant une paire nombre-unité nulle, par exemple, 0 ft + hauteur.</span><span class="sxs-lookup"><span data-stu-id="d89df-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="d89df-135">La deuxième virgule dans la fonction CALLTHIS est facultative.</span><span class="sxs-lookup"><span data-stu-id="d89df-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="d89df-136">Il correspond au nombre de paramètres supplémentaires ajoutés à votre procédure.</span><span class="sxs-lookup"><span data-stu-id="d89df-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="d89df-137">Si vous n’utilisez pas les paramètres supplémentaires, sauf `(vsoShape as Visio.Shape)` , n’ajoutez pas la deuxième virgule ; utilisez CALLTHIS("",).</span><span class="sxs-lookup"><span data-stu-id="d89df-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="d89df-138">Si vous ajoutez deux paramètres supplémentaires, par exemple, utilisez CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="d89df-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="d89df-139">La fonction CALLTHIS est toujours 0 et l’appel de _procédure_ se produit pendant la durée d’inactivité après le processus de recalcul.</span><span class="sxs-lookup"><span data-stu-id="d89df-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="d89df-140">_Procédure_ peut renvoyer une valeur, mais Visio l’ignore.</span><span class="sxs-lookup"><span data-stu-id="d89df-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="d89df-141">_Procédure_ renvoie une valeur que Visio peut reconnaître en définissant la formule ou le résultat d’une autre cellule dans le document, mais pas la cellule qui a appelé la _procédure_, sauf si vous souhaitez remplacer la formule CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="d89df-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="d89df-142">La fonction CALLTHIS est différente de la fonction RUNADDON ; en effet, un projet de document ne doit pas nécessairement faire référence à un autre projet pour appeler une procédure de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="d89df-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="d89df-143">Le code VBA appelé lorsque l’instance de Visio calcule une fonction CALLTHIS dans une formule ne doit pas fermer le document contenant la cellule qui utilise la fonction, sans quoi une erreur d’application se produit et Visio se ferme.</span><span class="sxs-lookup"><span data-stu-id="d89df-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="d89df-144">Si vous devez fermer le document contenant la cellule qui utilise la fonction CALLTHIS, utilisez l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d89df-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="d89df-145">fermez le document à partir de code non-VBA ;</span><span class="sxs-lookup"><span data-stu-id="d89df-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="d89df-146">Fermez le document à partir d’un projet différent de celui en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="d89df-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="d89df-147">Envoyez des messages de fenêtre dans le document pour fermer les fenêtres plutôt que de fermer le document.</span><span class="sxs-lookup"><span data-stu-id="d89df-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="d89df-148">Pour plus d’informations sur l’exécution de code dans Visio, voir [sur les paramètres de sécurité et l’exécution de Code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d89df-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d89df-149">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="d89df-149">Example 1</span></span>

<span data-ttu-id="d89df-150">CALLTHIS("p",,FORMATEX(Height,"#,00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="d89df-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="d89df-151">Appelle la procédure nommée p située dans un module et transmet la valeur de la cellule Height en centimètres, par exemple 7,62 cm.</span><span class="sxs-lookup"><span data-stu-id="d89df-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d89df-152">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="d89df-152">Example 2</span></span>

<span data-ttu-id="d89df-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="d89df-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="d89df-154">Appelle la procédure nommée q située dans un module et transmet la hauteur de la cellule en centimètres et la largeur en unités internes.</span><span class="sxs-lookup"><span data-stu-id="d89df-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d89df-155">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="d89df-155">Example 3</span></span>

<span data-ttu-id="d89df-156">Utilisez la procédure suivante dans le module de classe *ThisDocument* .</span><span class="sxs-lookup"><span data-stu-id="d89df-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="d89df-157">Utilisez l’une des syntaxes suivantes dans la cellule EventDblClick d’une forme avec les procédures qui précèdent.</span><span class="sxs-lookup"><span data-stu-id="d89df-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="d89df-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="d89df-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="d89df-159">CALLTHIS("ThisDocument.B",,"Click")</span><span class="sxs-lookup"><span data-stu-id="d89df-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="d89df-160">CALLTHIS("ThisDocument.C",,"Cliquez sur", " OK.")</span><span class="sxs-lookup"><span data-stu-id="d89df-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

