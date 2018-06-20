---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782240"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="193f0-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="193f0-103">xlGetInstPtr</span></span>

<span data-ttu-id="193f0-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="193f0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="193f0-105">Renvoie le descripteur d’instances de l’instance de Microsoft Excel en appelant une DLL.</span><span class="sxs-lookup"><span data-stu-id="193f0-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="193f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="193f0-106">Parameters</span></span>

<span data-ttu-id="193f0-107">Cette fonction ne comporte aucun argument.</span><span class="sxs-lookup"><span data-stu-id="193f0-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="193f0-108">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="193f0-108">Property value/Return value</span></span>

<span data-ttu-id="193f0-109">Le descripteur d’instances (**xltypeBigData**) est inclus dans le champ **val.bigdata.h.hdata** .</span><span class="sxs-lookup"><span data-stu-id="193f0-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="193f0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="193f0-110">Remarks</span></span>

<span data-ttu-id="193f0-111">Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances en cours d’exécution de Microsoft Excel qui appellent la DLL.</span><span class="sxs-lookup"><span data-stu-id="193f0-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="193f0-112">Cette fonction renvoie une valeur correcte avec les versions 32 bits et 64 bits de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="193f0-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="193f0-113">Elle a été introduite dans Excel 2010 comme une extension à la fonction [xlGetInst](xlgetinst.md) , qui fonctionne uniquement avec les versions 32 bits de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="193f0-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="193f0-114">Cette fonction fonctionne correctement lorsqu’elle est appelée à l’aide de ces deux types de fonctions de rappel API, [Excel4 et Excel12](excel4-excel12.md) car **XLOPER** et **XLOPER12** ont la même structure qui prend en charge la valeur **xltypeBigData** tapez.</span><span class="sxs-lookup"><span data-stu-id="193f0-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="193f0-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="193f0-115">Example</span></span>

<span data-ttu-id="193f0-116">L’exemple suivant compare l’instance de la dernière copie d’Excel qui l’a appelé à la copie active de Microsoft Excel qui l’a appelé.</span><span class="sxs-lookup"><span data-stu-id="193f0-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="193f0-117">Si elles sont les mêmes, elle renvoie la valeur 1 ; dans le cas contraire, elle renvoie la valeur 0 ; Si la fonction échoue, elle renvoie -1.</span><span class="sxs-lookup"><span data-stu-id="193f0-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="193f0-118">Cet exemple fonctionne avec les versions 32 bits et 64 bits de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="193f0-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="193f0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="193f0-119">See also</span></span>

- [<span data-ttu-id="193f0-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="193f0-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="193f0-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="193f0-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="193f0-122">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="193f0-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

