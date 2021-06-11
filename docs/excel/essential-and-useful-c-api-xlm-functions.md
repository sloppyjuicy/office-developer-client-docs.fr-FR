---
title: Fonctions XLM de l’API C essentielles et utiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434514"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="c7bc3-104">Fonctions XLM de l’API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="c7bc3-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="c7bc3-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7bc3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c7bc3-106">Les fonctions décrites dans cette section sont Microsoft Excel de rappel qui sont particulièrement utiles pour les développeurs DLL et XLL.</span><span class="sxs-lookup"><span data-stu-id="c7bc3-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="c7bc3-107">Parmi celles-ci, la fonction **xlfRegister** est essentielle pour les XL et les DLL qui souhaitent inscrire leurs fonctions et commandes afin qu’elles soient appelées directement à partir de Excel.</span><span class="sxs-lookup"><span data-stu-id="c7bc3-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="c7bc3-108">Les fonctions **xlfUnregister** et **xlfSetName** sont utilisées en combinaison pour désinsser les fonctions et commandes DLL et XLL.</span><span class="sxs-lookup"><span data-stu-id="c7bc3-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="c7bc3-109">De nombreuses autres fonctions sont exposées par les Excel via l’API C qui sont utiles lorsque vous développez des XL.</span><span class="sxs-lookup"><span data-stu-id="c7bc3-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="c7bc3-110">Elles correspondent aux fonctions Excel de feuille de calcul, ainsi qu’aux fonctions et commandes disponibles dans les feuilles macro XLM.</span><span class="sxs-lookup"><span data-stu-id="c7bc3-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="c7bc3-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c7bc3-111">In this section</span></span>

[<span data-ttu-id="c7bc3-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="c7bc3-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="c7bc3-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="c7bc3-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="c7bc3-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="c7bc3-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="c7bc3-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="c7bc3-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="c7bc3-116">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="c7bc3-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="c7bc3-117">xlfRegister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="c7bc3-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="c7bc3-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="c7bc3-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="c7bc3-119">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="c7bc3-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="c7bc3-120">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="c7bc3-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="c7bc3-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="c7bc3-121">xlfSetName</span></span>](xlfsetname.md)
  

