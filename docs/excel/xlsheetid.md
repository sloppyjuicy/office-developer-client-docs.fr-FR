---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- fonction xlSheetId [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310303"
---
# <a name="xlsheetid"></a><span data-ttu-id="03eb1-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="03eb1-104">xlSheetId</span></span>

<span data-ttu-id="03eb1-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03eb1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="03eb1-106">Recherche l'ID de feuille d'une feuille nommée afin de construire des références externes.</span><span class="sxs-lookup"><span data-stu-id="03eb1-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="03eb1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03eb1-107">Parameters</span></span>

<span data-ttu-id="03eb1-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="03eb1-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="03eb1-109">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="03eb1-109">(Optional).</span></span> <span data-ttu-id="03eb1-110">Nom du livre et de la feuille à rechercher.</span><span class="sxs-lookup"><span data-stu-id="03eb1-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="03eb1-111">Si cet argument est omis, la fonction **xlSheetId** renvoie l'ID de feuille de la feuille (avant) active.</span><span class="sxs-lookup"><span data-stu-id="03eb1-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="03eb1-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03eb1-112">Return value</span></span>

<span data-ttu-id="03eb1-113">Renvoie l'ID de la feuille dans _pxRes-\>Val. mref. idSheet_.</span><span class="sxs-lookup"><span data-stu-id="03eb1-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03eb1-114">Le pointeur de tableau _pxRes-\>Val. mref. lpmref_ est défini sur null après cet appel de sorte qu'il n'est pas nécessaire d'appeler **xlFree** pour libérer la mémoire que ce type contient normalement, bien qu'il soit entièrement sûr de le faire.</span><span class="sxs-lookup"><span data-stu-id="03eb1-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="03eb1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="03eb1-115">Remarks</span></span>

<span data-ttu-id="03eb1-116">Le classeur contenant la feuille spécifiée doit être ouvert pour utiliser cette fonction.</span><span class="sxs-lookup"><span data-stu-id="03eb1-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="03eb1-117">Il n'existe aucun moyen de créer une référence à un classeur non ouvert à partir d'une DLL.</span><span class="sxs-lookup"><span data-stu-id="03eb1-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="03eb1-118">Pour plus d'informations sur l'utilisation de **xlSheetId** pour construire des références, consultez la rubrique gestion de la [mémoire dans Excel](memory-management-in-excel.md) pour obtenir des exemples de construction de **xltypeRef** .</span><span class="sxs-lookup"><span data-stu-id="03eb1-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="03eb1-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="03eb1-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="03eb1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03eb1-120">See also</span></span>

- [<span data-ttu-id="03eb1-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="03eb1-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="03eb1-122">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="03eb1-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

