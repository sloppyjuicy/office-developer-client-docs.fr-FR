---
title: Fonctions XLM essentielles et utiles de l'API C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions [Excel 2007], c API XLM
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
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="65c09-104">Fonctions XLM essentielles et utiles de l'API C</span><span class="sxs-lookup"><span data-stu-id="65c09-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="65c09-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="65c09-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="65c09-106">Les fonctions décrites dans cette section sont des fonctions de rappel Microsoft Excel qui sont particulièrement utiles pour les développeurs DLL et XLL.</span><span class="sxs-lookup"><span data-stu-id="65c09-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="65c09-107">La fonction **xlfRegister** est, quant à elle, essentielle pour les XLL et les dll qui souhaitent enregistrer leurs fonctions et leurs commandes de sorte qu'elles puissent être appelées directement à partir d'Excel.</span><span class="sxs-lookup"><span data-stu-id="65c09-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="65c09-108">Les fonctions **xlfUnregister** et **xlfSetName** sont utilisées conjointement pour annuler l'inscription des fonctions et commandes de dll et XLL.</span><span class="sxs-lookup"><span data-stu-id="65c09-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="65c09-109">De nombreuses fonctions supplémentaires sont exposées par Excel via l'API C, qui sont utiles lorsque vous développez des XLL.</span><span class="sxs-lookup"><span data-stu-id="65c09-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="65c09-110">Elles correspondent aux fonctions et fonctions de feuille de calcul Excel qui sont disponibles à partir de feuilles macro XLM.</span><span class="sxs-lookup"><span data-stu-id="65c09-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="65c09-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="65c09-111">In this section</span></span>

[<span data-ttu-id="65c09-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="65c09-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="65c09-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="65c09-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="65c09-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="65c09-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="65c09-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="65c09-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="65c09-116">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="65c09-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="65c09-117">xlfRegister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="65c09-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="65c09-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="65c09-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="65c09-119">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="65c09-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="65c09-120">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="65c09-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="65c09-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="65c09-121">xlfSetName</span></span>](xlfsetname.md)
  

