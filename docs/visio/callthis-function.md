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
description: Appelle une procédure dans un projet Microsoft Visual Basic pour Applications (VBA).
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413814"
---
# <a name="callthis-function"></a><span data-ttu-id="73e5c-103">Fonction CALLTHIS</span><span class="sxs-lookup"><span data-stu-id="73e5c-103">CALLTHIS Function</span></span>

<span data-ttu-id="73e5c-104">Appelle une procédure dans un projet Microsoft Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="73e5c-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="73e5c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73e5c-105">Syntax</span></span>

<span data-ttu-id="73e5c-106">CALLTHIS( » \*\* *procedure* \*\* « ,[ » \*\* *project* \*\* « ],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="73e5c-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="73e5c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73e5c-107">Parameters</span></span>

|<span data-ttu-id="73e5c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="73e5c-108">**Name**</span></span>|<span data-ttu-id="73e5c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="73e5c-109">**Required/Optional**</span></span>|<span data-ttu-id="73e5c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="73e5c-110">**Data Type**</span></span>|<span data-ttu-id="73e5c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="73e5c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="73e5c-112">_procedure_</span><span class="sxs-lookup"><span data-stu-id="73e5c-112">_procedure_</span></span> <br/> |<span data-ttu-id="73e5c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73e5c-113">Required</span></span>  <br/> |<span data-ttu-id="73e5c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="73e5c-114">**String**</span></span> <br/> | <span data-ttu-id="73e5c-115">Nom de la procédure à appeler.</span><span class="sxs-lookup"><span data-stu-id="73e5c-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="73e5c-116">_projet_</span><span class="sxs-lookup"><span data-stu-id="73e5c-116">_project_</span></span> <br/> |<span data-ttu-id="73e5c-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="73e5c-117">Optional</span></span>  <br/> |<span data-ttu-id="73e5c-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="73e5c-118">**String**</span></span> <br/> |<span data-ttu-id="73e5c-119">Projet qui contient la procédure.</span><span class="sxs-lookup"><span data-stu-id="73e5c-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="73e5c-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="73e5c-120">_arg_</span></span> <br/> |<span data-ttu-id="73e5c-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="73e5c-121">Optional</span></span>  <br/> |<span data-ttu-id="73e5c-122">**Number, String, Date ou Currency**</span><span class="sxs-lookup"><span data-stu-id="73e5c-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="73e5c-123">Transmis comme paramètres à la procédure.</span><span class="sxs-lookup"><span data-stu-id="73e5c-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73e5c-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="73e5c-124">Remarks</span></span>

<span data-ttu-id="73e5c-125">Dans le projet VBA,  *la procédure*  est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="73e5c-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="73e5c-126">procedure(*vsoShape* As Visio. Shape [arg1 As type, arg2 As type...])</span><span class="sxs-lookup"><span data-stu-id="73e5c-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="73e5c-127">où  *vsoShape*  est une référence à l’objet **Shape** qui contient la formule CALLTHIS en cours d’évaluation, et  _arg1_,  *arg2*  ... sont les arguments spécifiés dans cette formule.</span><span class="sxs-lookup"><span data-stu-id="73e5c-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="73e5c-128">Notez  *que vsoShape*  est très proche de l’argument « this » passé à une procédure membre C++ ; d’où le nom « CALLTHIS ».</span><span class="sxs-lookup"><span data-stu-id="73e5c-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="73e5c-129">En effet, une cellule qui contient une formule incluant CALLTHIS peut être lue comme « Appeler cette procédure et lui transmettre une référence à ma forme ».</span><span class="sxs-lookup"><span data-stu-id="73e5c-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="73e5c-130">Si _le projet_ est spécifié, Microsoft Visio tous les documents  ouverts pour celui contenant le projet et appelle la procédure _dans_ ce projet.</span><span class="sxs-lookup"><span data-stu-id="73e5c-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="73e5c-131">Si _le_ projet est omis ou null  (« ») Visio suppose que la procédure se trouve dans le projet VBA du document qui contient la formule CALLTHIS en cours d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="73e5c-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="73e5c-132">Les nombres  _dans arg1,_  _arg2... sont_ transmis en unités externes.</span><span class="sxs-lookup"><span data-stu-id="73e5c-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="73e5c-133">Par exemple, si vous transmettez la valeur de la cellule Height à partir d’une forme haute de 3 cm, la valeur 3 est transmise.</span><span class="sxs-lookup"><span data-stu-id="73e5c-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="73e5c-134">Pour transmettre différentes unités avec un nombre, utilisez la fonction FORMATEX ou définissez explicitement les unités en ajoutant une paire nombre nul-unité (0 m + Height, par exemple).</span><span class="sxs-lookup"><span data-stu-id="73e5c-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="73e5c-135">La deuxième virgule dans la fonction CALLTHIS est facultative.</span><span class="sxs-lookup"><span data-stu-id="73e5c-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="73e5c-136">Elle correspond au nombre de paramètres supplémentaires ajoutés à votre procédure.</span><span class="sxs-lookup"><span data-stu-id="73e5c-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="73e5c-137">Si vous n’utilisez aucun paramètre supplémentaire, sauf , n’ajoutez pas la deuxième virgule ; utilisez  `(vsoShape as Visio.Shape)` CALLTHIS(« , »).</span><span class="sxs-lookup"><span data-stu-id="73e5c-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="73e5c-138">Si vous ajoutez deux paramètres, par exemple, utilisez CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="73e5c-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="73e5c-139">La fonction CALLTHIS est toujours évaluée à  0 et l’appel à la procédure se produit pendant les périodes d’inactivité une fois le processus de recalcul terminé.</span><span class="sxs-lookup"><span data-stu-id="73e5c-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="73e5c-140">_procedure_ peut renvoyer une valeur, mais Visio l’ignore.</span><span class="sxs-lookup"><span data-stu-id="73e5c-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="73e5c-141">_La_ procédure renvoie une valeur que Visio peut reconnaître en fixant la formule ou le résultat d’une autre cellule du document, mais pas la cellule qui a appelé la _procédure,_ sauf si vous souhaitez réécrire la formule CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="73e5c-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="73e5c-142">La fonction CALLTHIS est différente de la fonction RUNADDON ; en effet, un projet de document ne doit pas nécessairement faire référence à un autre projet pour appeler une procédure de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="73e5c-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="73e5c-143">Le code VBA appelé lorsque l’instance de Visio calcule une fonction CALLTHIS dans une formule ne doit pas fermer le document contenant la cellule qui utilise la fonction, sans quoi une erreur d’application se produit et Visio se ferme.</span><span class="sxs-lookup"><span data-stu-id="73e5c-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="73e5c-144">Si vous devez fermer le document contenant la cellule qui utilise la fonction CALLTHIS, utilisez l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="73e5c-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="73e5c-145">fermez le document à partir de code non-VBA ;</span><span class="sxs-lookup"><span data-stu-id="73e5c-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="73e5c-146">fermez le document à partir d’un projet autre que celui qui est en train de se fermer ;</span><span class="sxs-lookup"><span data-stu-id="73e5c-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="73e5c-147">envoyez des messages de fenêtre pour fermer les fenêtres du document plutôt que de fermer le document.</span><span class="sxs-lookup"><span data-stu-id="73e5c-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="73e5c-148">Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="73e5c-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="73e5c-149">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="73e5c-149">Example 1</span></span>

<span data-ttu-id="73e5c-150">CALLTHIS("p",,FORMATEX(Height,"#,00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="73e5c-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="73e5c-151">Appelle la procédure nommée p située dans un module et transmet la valeur de la cellule Height en centimètres, par exemple 7,62 cm.</span><span class="sxs-lookup"><span data-stu-id="73e5c-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="73e5c-152">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="73e5c-152">Example 2</span></span>

<span data-ttu-id="73e5c-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="73e5c-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="73e5c-154">Appelle la procédure nommée q située dans un module et transmet la hauteur de la cellule en centimètres et la largeur en unités internes.</span><span class="sxs-lookup"><span data-stu-id="73e5c-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="73e5c-155">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="73e5c-155">Example 3</span></span>

<span data-ttu-id="73e5c-156">Utilisez la procédure suivante dans le module de classe *ThisDocument.*</span><span class="sxs-lookup"><span data-stu-id="73e5c-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="73e5c-157">Utilisez l’une des syntaxes suivantes dans la cellule EventDblClick d’une forme avec les procédures qui précèdent.</span><span class="sxs-lookup"><span data-stu-id="73e5c-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="73e5c-158">CALLTHIS(« ThisDocument.A »,)</span><span class="sxs-lookup"><span data-stu-id="73e5c-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="73e5c-159">CALLTHIS(« ThisDocument.B »,,"Click »)</span><span class="sxs-lookup"><span data-stu-id="73e5c-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="73e5c-160">CALLTHIS("ThisDocument.C",,"Cliquez sur", " OK.")</span><span class="sxs-lookup"><span data-stu-id="73e5c-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

