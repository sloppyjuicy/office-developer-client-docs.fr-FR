---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- fonction xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782208"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="697d0-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="697d0-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="697d0-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="697d0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="697d0-106">Utilisé pour allouer un stockage persistant pour un **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="697d0-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="697d0-107">Données avec un nom défini binaire sont enregistrées avec le classeur et est accessible par un nom à tout moment.</span><span class="sxs-lookup"><span data-stu-id="697d0-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="697d0-108">Pour plus d’informations, voir « Limitation d’étendue nom binaire » dans [Les problèmes connus dans le développement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="697d0-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="697d0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="697d0-109">Parameters</span></span>

 <span data-ttu-id="697d0-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="697d0-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="697d0-111">Chaîne spécifiant le nom des données.</span><span class="sxs-lookup"><span data-stu-id="697d0-111">A string specifying the name of the data.</span></span> <span data-ttu-id="697d0-112">La chaîne est soumis aux mêmes restrictions de dénomination noms définis comme.</span><span class="sxs-lookup"><span data-stu-id="697d0-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="697d0-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="697d0-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="697d0-114">Structure Bigdata spécifiant les données à stocker.</span><span class="sxs-lookup"><span data-stu-id="697d0-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="697d0-115">Lorsque vous appelez cette fonction, le membre **lpbData** de la structure **bigdata** doit pointer sur les données pour lequel le nom est défini, et le membre **cbData** doit contenir la longueur des données en octets.</span><span class="sxs-lookup"><span data-stu-id="697d0-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="697d0-116">Si l’argument _pxData_ n’est pas spécifié (**xltypeMissing**), l’allocation nommée spécifiée par _pxName_ est supprimée.</span><span class="sxs-lookup"><span data-stu-id="697d0-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="697d0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="697d0-117">See also</span></span>



[<span data-ttu-id="697d0-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="697d0-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="697d0-119">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="697d0-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="697d0-120">Problèmes connus concernant le développement de XLL Excel</span><span class="sxs-lookup"><span data-stu-id="697d0-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

