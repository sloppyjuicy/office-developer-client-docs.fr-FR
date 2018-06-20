---
title: xlfRegister (formulaire 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- fonction xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782219"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="6cfe4-104">xlfRegister (formulaire 2)</span><span class="sxs-lookup"><span data-stu-id="6cfe4-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="6cfe4-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6cfe4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6cfe4-106">Peut être appelée à partir d’une commande DLL ou XLL lui-même a été appelée par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6cfe4-106">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="6cfe4-107">Cela équivaut à appeler **l’Enregistrer** à partir d’une feuille de macro Excel XLM.</span><span class="sxs-lookup"><span data-stu-id="6cfe4-107">This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="6cfe4-108">La fonction **xlfRegister** peut être appelée sous deux formes :</span><span class="sxs-lookup"><span data-stu-id="6cfe4-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="6cfe4-109">[xlfRegister (formulaire 1)](xlfregister-form-1.md): enregistre une commande ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="6cfe4-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="6cfe4-110">xlfRegister (formulaire 2) : charges et Active une solution XLL.</span><span class="sxs-lookup"><span data-stu-id="6cfe4-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="6cfe4-111">Appelée dans le formulaire 2, cette fonction peut uniquement être utilisée pour charger et activer un XLL contenant une procédure [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="6cfe4-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="6cfe4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cfe4-112">Parameters</span></span>

 <span data-ttu-id="6cfe4-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="6cfe4-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="6cfe4-114">Le nom de la DLL à être chargé et activé.</span><span class="sxs-lookup"><span data-stu-id="6cfe4-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6cfe4-115">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6cfe4-115">Property value/Return value</span></span>

<span data-ttu-id="6cfe4-116">Si l’opération réussit, cela renvoie le nom de la DLL (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="6cfe4-116">If successful, this returns the name of the DLL (**xltypeStr**).</span></span> <span data-ttu-id="6cfe4-117">Dans le cas contraire, elle renvoie une #VALUE !</span><span class="sxs-lookup"><span data-stu-id="6cfe4-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="6cfe4-118">erreur.</span><span class="sxs-lookup"><span data-stu-id="6cfe4-118">error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6cfe4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cfe4-119">See also</span></span>



[<span data-ttu-id="6cfe4-120">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="6cfe4-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

