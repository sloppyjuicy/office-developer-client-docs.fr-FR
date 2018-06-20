---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- fonction xlsheetnm [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782245"
---
# <a name="xlsheetnm"></a><span data-ttu-id="a434a-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="a434a-104">xlSheetNm</span></span>

<span data-ttu-id="a434a-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a434a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a434a-106">Renvoie le nom d’une feuille de calcul ou une feuille macro à partir de son ID interne feuille contenue dans une référence externe, ou le nom de la feuille en cours si passé une référence interne.</span><span class="sxs-lookup"><span data-stu-id="a434a-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="a434a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a434a-107">Parameters</span></span>

<span data-ttu-id="a434a-108">_pxExtref_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="a434a-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="a434a-109">Une référence à la feuille dont vous souhaitez que le nom.</span><span class="sxs-lookup"><span data-stu-id="a434a-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="a434a-110">Si vous passez une référence externe (**xltypeRef**) il doit contenir uniquement l’ID de la feuille.</span><span class="sxs-lookup"><span data-stu-id="a434a-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="a434a-111">Les structures de données qui décrivent les cellules de la feuille de calcul sont ignorées et n’avez pas besoin de fournir.</span><span class="sxs-lookup"><span data-stu-id="a434a-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="a434a-112">Si l’ID est défini sur zéro, **xlSheetNm** renvoie le nom de la feuille active.</span><span class="sxs-lookup"><span data-stu-id="a434a-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="a434a-113">Si vous passez une référence interne (**xltypeSef**), **xlSheetNm** renvoie le nom de la feuille active.</span><span class="sxs-lookup"><span data-stu-id="a434a-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a434a-114">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a434a-114">Property value/Return value</span></span>

<span data-ttu-id="a434a-115">Renvoie le nom de la feuille (**xltypeStr**) sous la forme `[Book1]Sheet1`.</span><span class="sxs-lookup"><span data-stu-id="a434a-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="a434a-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="a434a-116">Example</span></span>

<span data-ttu-id="a434a-117">L’exemple suivant affiche le nom de la feuille à partir de laquelle la fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="a434a-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="a434a-118">La fonction fonctionne correctement uniquement si appelée à partir d’une feuille macro lors de l’exécution d’une macro de commande XLM.</span><span class="sxs-lookup"><span data-stu-id="a434a-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="a434a-119">Il s’agit parce qu’elle appelle **xlcAlert**, laquelle uniquement les commandes peuvent faire et elle doit être appelée à partir d’une feuille plutôt qu’une boîte de dialogue, un menu ou la barre de commandes dans l’ordre pour **xlfCaller** renvoyer une référence.</span><span class="sxs-lookup"><span data-stu-id="a434a-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a434a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a434a-120">See also</span></span>

- [<span data-ttu-id="a434a-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="a434a-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="a434a-122">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="a434a-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

