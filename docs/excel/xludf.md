---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- fonction xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782246"
---
# <a name="xludf"></a><span data-ttu-id="c49fb-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="c49fb-104">xlUDF</span></span>

<span data-ttu-id="c49fb-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c49fb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c49fb-106">Appelle une fonction définie par l’utilisateur (UDF).</span><span class="sxs-lookup"><span data-stu-id="c49fb-106">Calls a user-defined function (UDF).</span></span> <span data-ttu-id="c49fb-107">Cette fonction permet une DLL pour appeler Visual Basic pour des fonctions définies par l’utilisateur d’Applications (VBA), les fonctions de langage macro XLM et des fonctions contenues dans d’autres compléments.</span><span class="sxs-lookup"><span data-stu-id="c49fb-107">This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="c49fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c49fb-108">Parameters</span></span>

<span data-ttu-id="c49fb-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** ou **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="c49fb-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="c49fb-110">La référence de la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="c49fb-110">The reference of the function you want to call.</span></span> <span data-ttu-id="c49fb-111">Il peut s’agir d’une référence de la cellule de la feuille de macro, le nom enregistré de la fonction sous forme de chaîne ou l’identificateur de Registre de la fonction.</span><span class="sxs-lookup"><span data-stu-id="c49fb-111">This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function.</span></span> <span data-ttu-id="c49fb-112">Pour les fonctions XLL complément inscrits à l’aide de **xlfRegister** ou **enregistrez** avec l' argument _pxFunctionText_ fourni, l’ID peut être obtenu à l’aide de **xlfEvaluate** pour rechercher le nom.</span><span class="sxs-lookup"><span data-stu-id="c49fb-112">For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="c49fb-113">_pxArg1..._</span><span class="sxs-lookup"><span data-stu-id="c49fb-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="c49fb-114">Zéro ou plusieurs arguments à la fonction définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c49fb-114">Zero or more arguments to the user-defined function.</span></span> <span data-ttu-id="c49fb-115">Lorsque vous appelez cette fonction dans les versions antérieures à Excel 2007, le nombre maximal d’arguments supplémentaires qui peuvent être transmises est 29, 30, y compris _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="c49fb-115">When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_.</span></span> <span data-ttu-id="c49fb-116">À compter d’Excel 2007, cette limite est déclenchée à 254, qui est 255, y compris _pxFnRef_.</span><span class="sxs-lookup"><span data-stu-id="c49fb-116">Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c49fb-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c49fb-117">Return value</span></span>

<span data-ttu-id="c49fb-118">Renvoie la valeur qui la fonction définie par l’utilisateur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c49fb-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="c49fb-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="c49fb-119">Example</span></span>

<span data-ttu-id="c49fb-120">L’exemple suivant exécute **TestMacro** sur feuille Macro1 Classeur1. XLS.</span><span class="sxs-lookup"><span data-stu-id="c49fb-120">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS.</span></span> <span data-ttu-id="c49fb-121">Assurez-vous que la macro est effectuée sur une feuille nommée Macro1.</span><span class="sxs-lookup"><span data-stu-id="c49fb-121">Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c49fb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c49fb-122">See also</span></span>

- [<span data-ttu-id="c49fb-123">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="c49fb-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

