---
title: RUNMACRO, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Appelle une macro dans un Microsoft Visual Basic pour Applications (VBA) project.
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789586"
---
# <a name="runmacro-function"></a><span data-ttu-id="9da9b-103">RUNMACRO, fonction</span><span class="sxs-lookup"><span data-stu-id="9da9b-103">RUNMACRO Function</span></span>

<span data-ttu-id="9da9b-104">Appelle une macro dans un Microsoft Visual Basic pour Applications (VBA) project.</span><span class="sxs-lookup"><span data-stu-id="9da9b-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9da9b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9da9b-105">Syntax</span></span>

<span data-ttu-id="9da9b-106">RUNMACRO (** *nommacro* ** [, ** *projname_opt* **])</span><span class="sxs-lookup"><span data-stu-id="9da9b-106">RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9da9b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9da9b-107">Parameters</span></span>

|<span data-ttu-id="9da9b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9da9b-108">**Name**</span></span>|<span data-ttu-id="9da9b-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9da9b-109">**Required/Optional**</span></span>|<span data-ttu-id="9da9b-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9da9b-110">**Data Type**</span></span>|<span data-ttu-id="9da9b-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9da9b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9da9b-112">_nommacro_</span><span class="sxs-lookup"><span data-stu-id="9da9b-112">_macroname_</span></span> <br/> |<span data-ttu-id="9da9b-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9da9b-113">Required</span></span>  <br/> |<span data-ttu-id="9da9b-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="9da9b-114">**String**</span></span> <br/> |<span data-ttu-id="9da9b-115">Nom de la macro à appeler</span><span class="sxs-lookup"><span data-stu-id="9da9b-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="9da9b-116">_projname_opt_</span><span class="sxs-lookup"><span data-stu-id="9da9b-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="9da9b-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="9da9b-117">Optional</span></span>  <br/> |<span data-ttu-id="9da9b-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="9da9b-118">**String**</span></span> <br/> | <span data-ttu-id="9da9b-119">Projet qui contient la macro</span><span class="sxs-lookup"><span data-stu-id="9da9b-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9da9b-120">Note</span><span class="sxs-lookup"><span data-stu-id="9da9b-120">Remarks</span></span>

<span data-ttu-id="9da9b-121">Si un projet n’est spécifié, Microsoft Visio recherche tous les documents ouverts pour l’un contenant _projname_opt_ et appelle _macroname_ dans ce projet.</span><span class="sxs-lookup"><span data-stu-id="9da9b-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="9da9b-122">Si le _nomproj_facult_ est omis ou nul (« »), _nommacro_ est supposé pour être dans le projet VBA du document contenant la formule RUNMACRO calculée.</span><span class="sxs-lookup"><span data-stu-id="9da9b-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="9da9b-123">La fonction RUNMACRO diffère de la fonction CALLTHIS car elle ne transmet une référence à la forme qui possède la formule à _nommacro_.</span><span class="sxs-lookup"><span data-stu-id="9da9b-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="9da9b-124">Comme CALLTHIS, la fonction RUNMACRO ne nécessite pas une référence à _projname_opt_ pour l’appeler.</span><span class="sxs-lookup"><span data-stu-id="9da9b-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="9da9b-125">Le code VBA appelé par l’évaluation d’une fonction RUNMACRO dans une formule par une instance Visio ne doit pas fermer le document contenant la cellule qui utilise la fonction ; dans le cas contraire, une erreur d’application se produit et Visio se ferme.</span><span class="sxs-lookup"><span data-stu-id="9da9b-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="9da9b-126">Si vous devez fermer le document contenant la cellule qui utilise la fonction RUNMACRO, procédez de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="9da9b-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="9da9b-127">Fermez le document à partir d’un code non-VBA.</span><span class="sxs-lookup"><span data-stu-id="9da9b-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="9da9b-128">Fermez le document à partir d’un projet différent de celui en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="9da9b-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="9da9b-129">Envoyez des messages de fenêtre dans le document pour fermer les fenêtres plutôt que de fermer le document.</span><span class="sxs-lookup"><span data-stu-id="9da9b-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="9da9b-130">Pour plus d’informations sur l’exécution de code dans Visio, voir [à propos des paramètres de sécurité et l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="9da9b-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9da9b-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="9da9b-131">Example</span></span>

<span data-ttu-id="9da9b-132">L’exemple suivant appelle une macro appelée MyTest dans le module de classe ThisDocument du projet VBA contenant la formule RUNMACRO.</span><span class="sxs-lookup"><span data-stu-id="9da9b-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="9da9b-133">RUNMACRO (« ThisDocument.MyTest »)</span><span class="sxs-lookup"><span data-stu-id="9da9b-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

