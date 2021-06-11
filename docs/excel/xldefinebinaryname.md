---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- fonction xldefinebinaryname [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430251"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="cc121-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="cc121-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="cc121-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cc121-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cc121-106">Utilisé pour allouer un stockage persistant pour **un xltypeBigData** **XLOPER** /  **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="cc121-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="cc121-107">Les données avec un nom binaire défini sont enregistrées avec le workbook et sont accessibles par nom à tout moment.</span><span class="sxs-lookup"><span data-stu-id="cc121-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="cc121-108">Pour plus d’informations, voir « Limite d’étendue du nom binaire » dans Problèmes connus [Excel développement XLL .](known-issues-in-excel-xll-development.md)</span><span class="sxs-lookup"><span data-stu-id="cc121-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="cc121-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="cc121-109">Parameters</span></span>

 <span data-ttu-id="cc121-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="cc121-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="cc121-111">Chaîne spécifiant le nom des données.</span><span class="sxs-lookup"><span data-stu-id="cc121-111">A string specifying the name of the data.</span></span> <span data-ttu-id="cc121-112">La chaîne est soumise aux mêmes restrictions d’attribution de noms que les noms définis.</span><span class="sxs-lookup"><span data-stu-id="cc121-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="cc121-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="cc121-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="cc121-114">Structure Bigdata spécifiant les données à stocker.</span><span class="sxs-lookup"><span data-stu-id="cc121-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="cc121-115">Lorsque vous appelez cette fonction, le membre **lpbData** de la structure **bigdata** doit pointer vers les données pour lesquelles le nom est défini et le membre **cbData** doit contenir la longueur des données en octets.</span><span class="sxs-lookup"><span data-stu-id="cc121-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="cc121-116">Si  _l’argument pxData_ n’est pas spécifié (**xltypeMissing**), l’allocation nommée spécifiée par  _pxName_ est supprimée.</span><span class="sxs-lookup"><span data-stu-id="cc121-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc121-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc121-117">See also</span></span>



[<span data-ttu-id="cc121-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="cc121-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="cc121-119">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="cc121-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="cc121-120">Problèmes connus dans le développement Excel XLL</span><span class="sxs-lookup"><span data-stu-id="cc121-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

