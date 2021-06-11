---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- fonction xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428430"
---
# <a name="xlsheetid"></a><span data-ttu-id="de4ca-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="de4ca-104">xlSheetId</span></span>

<span data-ttu-id="de4ca-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de4ca-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="de4ca-106">Recherche l’ID de feuille d’une feuille nommée afin de construire des références externes.</span><span class="sxs-lookup"><span data-stu-id="de4ca-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="de4ca-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="de4ca-107">Parameters</span></span>

<span data-ttu-id="de4ca-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="de4ca-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="de4ca-109">(Facultatif).</span><span class="sxs-lookup"><span data-stu-id="de4ca-109">(Optional).</span></span> <span data-ttu-id="de4ca-110">Nom du livre et de la feuille que vous souhaitez connaître.</span><span class="sxs-lookup"><span data-stu-id="de4ca-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="de4ca-111">Si elle est omise, **la fonction xlSheetId** renvoie l’ID de feuille de la feuille active (avant).</span><span class="sxs-lookup"><span data-stu-id="de4ca-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="de4ca-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="de4ca-112">Return value</span></span>

<span data-ttu-id="de4ca-113">Renvoie l’ID de feuille  _dans pxRes- \> val.mref.idSheet_.</span><span class="sxs-lookup"><span data-stu-id="de4ca-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="de4ca-114">Le pointeur du tableau  _pxRes- \> val.mref.lpmref_ est définie sur NULL après cet appel, de sorte qu’il n’est pas nécessaire d’appeler **xlFree** pour libérer la mémoire que ce type contient normalement, bien qu’il soit totalement sûr de le faire.</span><span class="sxs-lookup"><span data-stu-id="de4ca-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de4ca-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="de4ca-115">Remarks</span></span>

<span data-ttu-id="de4ca-116">Le workbook contenant la feuille spécifiée doit être ouvert pour utiliser cette fonction.</span><span class="sxs-lookup"><span data-stu-id="de4ca-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="de4ca-117">Il n’existe aucun moyen de construire une référence à un livre de travail non ouvert à partir d’une DLL.</span><span class="sxs-lookup"><span data-stu-id="de4ca-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="de4ca-118">Pour plus d’informations sur l’utilisation de **xlSheetId** pour construire des références, voir Gestion de [la mémoire dans Excel](memory-management-in-excel.md) pour obtenir des exemples de construction **xltypeRef.**</span><span class="sxs-lookup"><span data-stu-id="de4ca-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="de4ca-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="de4ca-119">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="de4ca-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de4ca-120">See also</span></span>

- [<span data-ttu-id="de4ca-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="de4ca-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="de4ca-122">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="de4ca-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

