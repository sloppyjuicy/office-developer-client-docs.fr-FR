---
title: Fonctions XLM API C essentielles et utiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions [excel 2007], xlm d’api c
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782039"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="7e456-104">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="7e456-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="7e456-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e456-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7e456-106">Les fonctions décrites dans cette section sont des fonctions de rappel de Microsoft Excel sont particulièrement utiles aux développeurs DLL et XLL.</span><span class="sxs-lookup"><span data-stu-id="7e456-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="7e456-107">D'entre eux, la fonction **xlfRegister** est essentielle pour XLL et les DLL want enregistrer leurs fonctions et les commandes afin qu’elles peuvent être appelées directement à partir d’Excel.</span><span class="sxs-lookup"><span data-stu-id="7e456-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="7e456-108">Les fonctions **xlfUnregister** et **xlfSetName** sont utilisés conjointement pour annuler l’inscription de commandes et les fonctions XLL et de DLL.</span><span class="sxs-lookup"><span data-stu-id="7e456-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="7e456-109">Davantage de fonctions est exposés par Excel par le biais de l’API C qui sont utiles lorsque vous développez des solutions XLL.</span><span class="sxs-lookup"><span data-stu-id="7e456-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="7e456-110">Ils correspondent à la feuille de calcul Excel les fonctions et les fonctions et les commandes disponibles à partir des feuilles macro XLM.</span><span class="sxs-lookup"><span data-stu-id="7e456-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7e456-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7e456-111">In this section</span></span>

[<span data-ttu-id="7e456-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="7e456-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="7e456-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="7e456-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="7e456-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="7e456-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="7e456-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="7e456-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="7e456-116">xlfRegister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="7e456-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="7e456-117">xlfRegister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="7e456-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="7e456-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="7e456-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="7e456-119">xlfUnregister (formulaire 1)</span><span class="sxs-lookup"><span data-stu-id="7e456-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="7e456-120">xlfUnregister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="7e456-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="7e456-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="7e456-121">xlfSetName</span></span>](xlfsetname.md)
  

