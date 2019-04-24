---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- fonction xlGetName [Excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 350ae99baf088a36fa3e1159caa1805cdd623276
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303828"
---
# <a name="xlgetname"></a><span data-ttu-id="c5700-104">xlGetName</span><span class="sxs-lookup"><span data-stu-id="c5700-104">xlGetName</span></span>

<span data-ttu-id="c5700-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c5700-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c5700-106">Renvoie le chemin d'accès complet et le nom de fichier de la DLL sous la forme d'une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c5700-106">Returns the full path and file name of the DLL in the form of a string.</span></span>
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="c5700-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5700-107">Parameters</span></span>

<span data-ttu-id="c5700-108">Cette fonction n'a pas d'argument.</span><span class="sxs-lookup"><span data-stu-id="c5700-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c5700-109">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="c5700-109">Property value/Return value</span></span>

<span data-ttu-id="c5700-110">Renvoie le chemin d'accès et le nom de fichier (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="c5700-110">Returns the path and file name (**xltypeStr**).</span></span> 
  
## <a name="example"></a><span data-ttu-id="c5700-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="c5700-111">Example</span></span>

`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetNameExample(void)
{
    XLOPER12 xRes;
    Excel12(xlGetName, (LPXLOPER12)&xRes, 0);
    Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c5700-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5700-112">See also</span></span>

- [<span data-ttu-id="c5700-113">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="c5700-113">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

