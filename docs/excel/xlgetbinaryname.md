---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- fonction xlGetBinaryName [Excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303835"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="24ab8-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="24ab8-104">xlGetBinaryName</span></span>

<span data-ttu-id="24ab8-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="24ab8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="24ab8-106">Permet de renvoyer un descripteur pour les données enregistrées par la [fonction xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="24ab8-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="24ab8-107">Les données avec un nom binaire défini sont enregistrées avec le classeur et sont accessibles par nom à tout moment.</span><span class="sxs-lookup"><span data-stu-id="24ab8-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="24ab8-108">Pour plus d'informations, voir «limitation de l'étendue de nom binaire» dans [problèmes connus dans Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="24ab8-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="24ab8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24ab8-109">Parameters</span></span>

<span data-ttu-id="24ab8-110">_pxRes_ (**xltypeBigData** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="24ab8-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="24ab8-111">La structure bigdata spécifiant les données récupérées ou une erreur est que les données n'ont pas pu être récupérées ou que le nom n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="24ab8-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="24ab8-112">Lorsque la fonction renvoie, le membre **hdata** de la méthode **XLOPER**/ **XLOPER12** contient un descripteur pour les données nommées.</span><span class="sxs-lookup"><span data-stu-id="24ab8-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="24ab8-113">_pxRes_ doit être libéré dans un appel à **xlFree** lorsqu'il n'est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="24ab8-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="24ab8-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="24ab8-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="24ab8-115">Chaîne spécifiant le nom des données.</span><span class="sxs-lookup"><span data-stu-id="24ab8-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24ab8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="24ab8-116">Remarks</span></span>

<span data-ttu-id="24ab8-117">Microsoft Excel est propriétaire du handle de mémoire renvoyé dans **hdata**.</span><span class="sxs-lookup"><span data-stu-id="24ab8-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="24ab8-118">Dans Windows, le descripteur est un descripteur de mémoire globale (alloué par la fonction **GlobalAlloc** ).</span><span class="sxs-lookup"><span data-stu-id="24ab8-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24ab8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24ab8-119">See also</span></span>

- [<span data-ttu-id="24ab8-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="24ab8-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="24ab8-121">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="24ab8-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

