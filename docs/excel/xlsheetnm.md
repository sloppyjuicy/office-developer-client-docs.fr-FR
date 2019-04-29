---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- fonction xlSheetNm [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437412"
---
# <a name="xlsheetnm"></a><span data-ttu-id="7c978-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="7c978-104">xlSheetNm</span></span>

<span data-ttu-id="7c978-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c978-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c978-106">Renvoie le nom d'une feuille de calcul ou d'une feuille macro à partir de son ID de feuille interne contenu dans une référence externe ou du nom de la feuille active si une référence interne lui a été transmise.</span><span class="sxs-lookup"><span data-stu-id="7c978-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="7c978-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c978-107">Parameters</span></span>

<span data-ttu-id="7c978-108">_pxExtref_ (**xltypeRef** ou **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="7c978-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="7c978-109">Référence à la feuille dont vous souhaitez obtenir le nom.</span><span class="sxs-lookup"><span data-stu-id="7c978-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="7c978-110">Si vous transférez une référence externe (**xltypeRef**), elle doit uniquement contenir l'ID de la feuille.</span><span class="sxs-lookup"><span data-stu-id="7c978-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="7c978-111">Les structures de données qui décrivent les cellules de la feuille de calcul sont ignorées et n'ont pas besoin d'être fournies.</span><span class="sxs-lookup"><span data-stu-id="7c978-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="7c978-112">Si la valeur de l'ID est définie sur zéro, **xlSheetNm** renvoie le nom de la feuille actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c978-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="7c978-113">Si vous transférez une référence interne (**xltypeSef**), **xlSheetNm** renvoie le nom de la feuille actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c978-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7c978-114">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="7c978-114">Property value/Return value</span></span>

<span data-ttu-id="7c978-115">Renvoie le nom de la feuille (**xltypeStr**) dans le formulaire `[Book1]Sheet1`.</span><span class="sxs-lookup"><span data-stu-id="7c978-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="7c978-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c978-116">Example</span></span>

<span data-ttu-id="7c978-117">L'exemple suivant montre comment afficher le nom de la feuille à partir de laquelle la fonction a été appelée.</span><span class="sxs-lookup"><span data-stu-id="7c978-117">The following example displays the name of the sheet from which the function was called.</span></span> <span data-ttu-id="7c978-118">La fonction fonctionne correctement uniquement si elle est appelée à partir d'une feuille macro lors de l'exécution d'une macro de commande XLM.</span><span class="sxs-lookup"><span data-stu-id="7c978-118">The function works correctly only if called from a macro sheet while executing an XLM command macro.</span></span> <span data-ttu-id="7c978-119">Cela est dû au fait qu'il appelle **xlcAlert**, que seules les commandes peuvent faire, et qu'il doit être appelé à partir d'une feuille plutôt que d'une boîte de dialogue, d'un menu ou d'une barre de commandes afin que **xlfCaller** renvoie une référence.</span><span class="sxs-lookup"><span data-stu-id="7c978-119">This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="7c978-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c978-120">See also</span></span>

- [<span data-ttu-id="7c978-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="7c978-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="7c978-122">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="7c978-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

