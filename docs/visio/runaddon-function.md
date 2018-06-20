---
title: RUNADDON, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Exécute un module complémentaire ou une macro dans un Microsoft projet Visual Basic pour Applications (VBA).
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789589"
---
# <a name="runaddon-function"></a><span data-ttu-id="7b1a1-103">RUNADDON, fonction</span><span class="sxs-lookup"><span data-stu-id="7b1a1-103">RUNADDON Function</span></span>

<span data-ttu-id="7b1a1-104">Exécute un module complémentaire ou une macro dans un Microsoft projet Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="7b1a1-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7b1a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b1a1-105">Syntax</span></span>

<span data-ttu-id="7b1a1-106">RUNADDON (« *chaîne* »)</span><span class="sxs-lookup"><span data-stu-id="7b1a1-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7b1a1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b1a1-107">Parameters</span></span>

|<span data-ttu-id="7b1a1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7b1a1-108">**Name**</span></span>|<span data-ttu-id="7b1a1-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7b1a1-109">**Required/Optional**</span></span>|<span data-ttu-id="7b1a1-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7b1a1-110">**Data Type**</span></span>|<span data-ttu-id="7b1a1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b1a1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7b1a1-112">_string_</span><span class="sxs-lookup"><span data-stu-id="7b1a1-112">_string_</span></span> <br/> |<span data-ttu-id="7b1a1-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7b1a1-113">Required</span></span>  <br/> |<span data-ttu-id="7b1a1-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="7b1a1-114">**String**</span></span> <br/> | <span data-ttu-id="7b1a1-115">Le nom d’un module complémentaire de la collection **Addons** ou d’une macro dans un projet VBA.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b1a1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b1a1-116">Remarks</span></span>

<span data-ttu-id="7b1a1-117">Si le projet du document qui contient l’appel de fonction RUNADDON (ou un autre projet s’il est référencé) n’a pas de macro (une procédure sans argument) nommée _chaîne_, Microsoft Visio exécute le module complémentaire nommé _chaîne_.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="7b1a1-118">Si aucun module complémentaire nommé _chaîne_ ne peut être trouvé, Visio ne fait rien et ne génère aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="7b1a1-119">(Vous pouvez utiliser la propriété **TraceFlags** pour contrôler les procédures et les modules complémentaires Visio tente de s’exécuter).</span><span class="sxs-lookup"><span data-stu-id="7b1a1-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="7b1a1-120">Lorsque vous appelez une procédure dans un module standard, il est recommandé de préfixe de la chaîne avec le nom du module qui contient la procédure (par exemple, *moduleName.procName*), car plusieurs modules peuvent avoir une procédure portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="7b1a1-121">Pour appeler une procédure dans un projet autre que le projet du document qui contient l’appel de fonction RUNADDON, utilisez la syntaxe *projName.modName.procName* (vous devez avoir explicitement défini une référence au *NomProj* dans votre projet VBA).</span><span class="sxs-lookup"><span data-stu-id="7b1a1-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="7b1a1-p102">À partir de Visio 2002, la fonction RUNADDON ne peut exécuter une chaîne contenant du code VBA arbitraire. Le code précédemment transmis à la fonction RUNADDON peut être déplacé vers une procédure dans un projet VBA de document appelé à partir de la fonction RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="7b1a1-124">Pour plus d’informations sur l’exécution de code dans Visio, voir [sur les paramètres de sécurité et l’exécution de Code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans ce guide de référence de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="7b1a1-p103">Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDON. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7b1a1-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="7b1a1-127">Example 1</span></span>

<span data-ttu-id="7b1a1-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="7b1a1-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="7b1a1-129">Lance un module complémentaire appelé Calendar.exe.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7b1a1-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="7b1a1-130">Example 2</span></span>

<span data-ttu-id="7b1a1-131">RUNADDON("Array Shapes")</span><span class="sxs-lookup"><span data-stu-id="7b1a1-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="7b1a1-132">Lance le module complémentaire (implémenté par VSL) dont le nom est Array Shapes.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7b1a1-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="7b1a1-133">Example 3</span></span>

<span data-ttu-id="7b1a1-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="7b1a1-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="7b1a1-135">Appelle la macro ReportStatistics dans le module **ThisDocument** dans le projet de document contenant cet appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="7b1a1-136">Pour appeler une macro dans le module **ThisDocument** , vous devez faire précéder la chaîne de « ThisDocument » comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="7b1a1-137">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="7b1a1-137">Example 4</span></span>

<span data-ttu-id="7b1a1-138">RUNADDON (« *NomModule* . ReportStatistics »)</span><span class="sxs-lookup"><span data-stu-id="7b1a1-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="7b1a1-139">Appelle la macro ReportStatistics dans *NomModule* dans le projet de document qui contient cet appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="7b1a1-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

