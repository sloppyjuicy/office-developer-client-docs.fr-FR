---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- fonction xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782224"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="e32f5-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="e32f5-104">xlGetBinaryName</span></span>

<span data-ttu-id="e32f5-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e32f5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e32f5-106">Utilisé pour retourner un handle pour les données enregistrées par la [fonction xlDefineBinaryName](xldefinebinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="e32f5-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="e32f5-107">Données avec un nom défini binaire sont enregistrées avec le classeur et est accessible par un nom à tout moment.</span><span class="sxs-lookup"><span data-stu-id="e32f5-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="e32f5-108">Pour plus d’informations, voir « Binaire » nom Limitation d’étendue dans [Problèmes connus dans le développement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="e32f5-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="e32f5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e32f5-109">Parameters</span></span>

<span data-ttu-id="e32f5-110">_pxRes_ (**xltypeBigData** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="e32f5-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="e32f5-111">Structure Bigdata spécifiant que les données récupérées ou une erreur est les données n’a pas pu être récupéré ou le nom n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="e32f5-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="e32f5-112">Lorsque la fonction retourne, le membre **hdata** de la **XLOPER**/ **XLOPER12** contient un handle pour les données nommées.</span><span class="sxs-lookup"><span data-stu-id="e32f5-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="e32f5-113">_pxRes_ doit être libéré dans un appel à **xlFree** n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e32f5-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="e32f5-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="e32f5-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="e32f5-115">Chaîne spécifiant le nom des données.</span><span class="sxs-lookup"><span data-stu-id="e32f5-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e32f5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e32f5-116">Remarks</span></span>

<span data-ttu-id="e32f5-117">Microsoft Excel possède le handle de mémoire retourné dans **hdata**.</span><span class="sxs-lookup"><span data-stu-id="e32f5-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="e32f5-118">Dans Windows, le handle est le handle de mémoire globale (alloué par la fonction **GlobalAlloc** ).</span><span class="sxs-lookup"><span data-stu-id="e32f5-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e32f5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e32f5-119">See also</span></span>

- [<span data-ttu-id="e32f5-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="e32f5-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="e32f5-121">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="e32f5-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

