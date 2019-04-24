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
description: Exécute un complément ou une macro dans un projet Microsoft Visual Basic pour applications (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319060"
---
# <a name="runaddon-function"></a><span data-ttu-id="89e64-103">Fonction RUNADDON</span><span class="sxs-lookup"><span data-stu-id="89e64-103">RUNADDON Function</span></span>

<span data-ttu-id="89e64-104">Exécute un complément ou une macro dans un projet Microsoft Visual Basic pour applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="89e64-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="89e64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89e64-105">Syntax</span></span>

<span data-ttu-id="89e64-106">RUNADDON (" *chaîne* ")</span><span class="sxs-lookup"><span data-stu-id="89e64-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="89e64-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89e64-107">Parameters</span></span>

|<span data-ttu-id="89e64-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="89e64-108">**Name**</span></span>|<span data-ttu-id="89e64-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="89e64-109">**Required/Optional**</span></span>|<span data-ttu-id="89e64-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="89e64-110">**Data Type**</span></span>|<span data-ttu-id="89e64-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="89e64-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="89e64-112">_string_</span><span class="sxs-lookup"><span data-stu-id="89e64-112">_string_</span></span> <br/> |<span data-ttu-id="89e64-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="89e64-113">Required</span></span>  <br/> |<span data-ttu-id="89e64-114">**String**</span><span class="sxs-lookup"><span data-stu-id="89e64-114">**String**</span></span> <br/> | <span data-ttu-id="89e64-115">Nom d’un module complémentaire de la collection **Addons** ou d’une macro dans un projet VBA.</span><span class="sxs-lookup"><span data-stu-id="89e64-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89e64-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="89e64-116">Remarks</span></span>

<span data-ttu-id="89e64-117">Si le projet du document qui contient l'appel de fonction RUNADDON (ou un autre projet s'il est référencé) n'a pas de macro (une procédure sans argument) nommée _String_, Microsoft Visio exécute le module complémentaire nommé _String_.</span><span class="sxs-lookup"><span data-stu-id="89e64-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="89e64-118">Si aucun module complémentaire nommé _String_ ne peut être trouvé, Visio ne fait rien et ne signale aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="89e64-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="89e64-119">(Vous pouvez utiliser la propriété **TraceFlags** pour contrôler les procédures et modules complémentaires que Visio tente d’exécuter.)</span><span class="sxs-lookup"><span data-stu-id="89e64-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="89e64-120">Lorsque vous appelez une procédure dans un module standard, il est recommandé de faire précéder la chaîne du nom du module qui contient la procédure (par exemple, *moduleName.* ProcName), car plusieurs modules peuvent avoir une procédure portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="89e64-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="89e64-121">Pour appeler une procédure dans un projet autre que le projet du document qui contient l'appel de fonction RUNADDON, utilisez la syntaxe *ProjName. n.* procname (vous devez avoir explicitement défini une référence à *ProjName* dans votre projet VBA).</span><span class="sxs-lookup"><span data-stu-id="89e64-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="89e64-p102">À partir de Visio 2002, la fonction RUNADDON ne peut exécuter une chaîne contenant du code VBA arbitraire. Le code précédemment transmis à la fonction RUNADDON peut être déplacé vers une procédure dans un projet VBA de document appelé à partir de la fonction RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="89e64-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="89e64-124">Pour plus d’informations sur l’exécution de code dans Visio, reportez-vous à la rubrique [À propos des paramètres de sécurité et de l’exécution de code dans Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) dans la Référence de la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="89e64-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="89e64-p103">Dans les versions précédentes de Visio, cette fonction s’appelait _RUNADDON. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre de ces styles.</span><span class="sxs-lookup"><span data-stu-id="89e64-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="89e64-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="89e64-127">Example 1</span></span>

<span data-ttu-id="89e64-128">RUNADDON ("Calendar. exe")</span><span class="sxs-lookup"><span data-stu-id="89e64-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="89e64-129">Lance un module complémentaire appelé Calendar. exe.</span><span class="sxs-lookup"><span data-stu-id="89e64-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="89e64-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="89e64-130">Example 2</span></span>

<span data-ttu-id="89e64-131">RUNADDON("Array Shapes")</span><span class="sxs-lookup"><span data-stu-id="89e64-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="89e64-132">Lance le module complémentaire (implémenté par VSL) dont le nom est Array Shapes.</span><span class="sxs-lookup"><span data-stu-id="89e64-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="89e64-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="89e64-133">Example 3</span></span>

<span data-ttu-id="89e64-134">RUNADDON ("ThisDocument. ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="89e64-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="89e64-135">Appelle la macro ReportStatistics dans le module **ThisDocument** dans le projet de document contenant cet appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="89e64-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="89e64-136">Pour appeler une macro dans un module **ThisDocument**, vous devez faire précéder la chaîne de "ThisDocument" comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="89e64-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="89e64-137">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="89e64-137">Example 4</span></span>

<span data-ttu-id="89e64-138">RUNADDON (" *modulename* . ReportStatistics ")</span><span class="sxs-lookup"><span data-stu-id="89e64-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="89e64-139">Appelle la macro ReportStatistics dans *modulename* dans le projet de document qui contient cet appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="89e64-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

