---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- fonction xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782228"
---
# <a name="xlgetinst"></a><span data-ttu-id="79450-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="79450-104">xlGetInst</span></span>

 <span data-ttu-id="79450-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79450-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="79450-106">Renvoie le descripteur d’instances de l’instance de Microsoft Excel en appelant une DLL.</span><span class="sxs-lookup"><span data-stu-id="79450-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="79450-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79450-107">Parameters</span></span>

<span data-ttu-id="79450-108">Cette fonction ne comporte aucun argument.</span><span class="sxs-lookup"><span data-stu-id="79450-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="79450-109">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="79450-109">Property value/Return value</span></span>

<span data-ttu-id="79450-110">Le descripteur d’instances (**xltypeInt**) est inclus dans le champ **val.w** .</span><span class="sxs-lookup"><span data-stu-id="79450-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="79450-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="79450-111">Remarks</span></span>

<span data-ttu-id="79450-112">Cette fonction peut être utilisée pour faire la distinction entre plusieurs instances en cours d’exécution de Microsoft Excel qui appellent la DLL.</span><span class="sxs-lookup"><span data-stu-id="79450-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="79450-113">Lorsque vous appelez cette fonction à l’aide de [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), la variable de type entier XLOPER renvoyée est un entier signé 16 bits courte. Il s’agit des 16 bits de poids faibles de la poignée de Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="79450-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="79450-114">À compter d’Excel 2007, la variable de type entier de la **XLOPER12** est un int 32 bits signé et par conséquent contient le handle entier, évite d’avoir à parcourir toutes les fenêtres ouvertes.</span><span class="sxs-lookup"><span data-stu-id="79450-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="79450-115">Si la fonction **xlGetInst** est utilisée avec la version 64 bits de Microsoft Excel, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="79450-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="79450-116">Il s’agit, car le type de valeur **xltypeInt** n’est pas assez large pour contenir la poignée de type longue 64 bits renvoyée par Excel dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="79450-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="79450-117">Pour cela, Excel 2010 introduit une nouvelle fonction nommée [xlGetInstPtr](xlgetinstptr.md), qui s’exécute correctement avec les versions 32 bits et 64 bits de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="79450-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="79450-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="79450-118">Example</span></span>

<span data-ttu-id="79450-119">L’exemple suivant compare l’instance de la dernière copie d’Excel qui l’a appelé à la copie active de Microsoft Excel qui l’a appelé.</span><span class="sxs-lookup"><span data-stu-id="79450-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="79450-120">Si elles sont les mêmes, elle renvoie la valeur 1 ; dans le cas contraire, elle renvoie la valeur 0 ; Si la fonction échoue, elle renvoie -1.</span><span class="sxs-lookup"><span data-stu-id="79450-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="79450-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79450-121">See also</span></span>



[<span data-ttu-id="79450-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="79450-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="79450-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="79450-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="79450-124">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="79450-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

