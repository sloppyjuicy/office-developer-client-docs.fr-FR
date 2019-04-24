---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- fonction xlAddInManagerInfo [Excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303996"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="3f6de-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="3f6de-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="3f6de-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f6de-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f6de-106">Appelé par Microsoft Excel lorsque le gestionnaire de compléments est appelé pour la première fois dans une session Excel.</span><span class="sxs-lookup"><span data-stu-id="3f6de-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="3f6de-107">Cette fonction permet au gestionnaire de compléments d'obtenir des informations sur votre complément.</span><span class="sxs-lookup"><span data-stu-id="3f6de-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="3f6de-108">Excel 2007 et les versions ultérieures appellent **xlAddInManagerInfo12** de préférence sur **xlAddInManagerInfo** s'ils sont exportés par le XLL.</span><span class="sxs-lookup"><span data-stu-id="3f6de-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="3f6de-109">La fonction **xlAddInManagerInfo12** doit fonctionner de la même manière que **xlAddInManagerInfo** pour éviter les différences de comportement de la XLL.</span><span class="sxs-lookup"><span data-stu-id="3f6de-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="3f6de-110">Excel s'attend à ce qu' **xlAddInManagerInfo12** renvoie un type de données **XLOPER12** , tandis que **xlAddInManagerInfo** doit renvoyer un **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="3f6de-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="3f6de-111">La fonction **xlAddInManagerInfo12** n'est pas appelée par les versions d'Excel antérieures à Excel 2007, car elles ne prennent pas en charge la méthode **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="3f6de-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="3f6de-112">Excel ne nécessite pas de XLL pour implémenter et exporter l'une ou l'autre de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="3f6de-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="3f6de-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f6de-113">Parameters</span></span>

 <span data-ttu-id="3f6de-114">_pxAction:_ Pointeur vers un type **XLOPER/XLOPER12** numérique (**xltypeInt** ou **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="3f6de-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="3f6de-115">Informations demandées par Excel.</span><span class="sxs-lookup"><span data-stu-id="3f6de-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3f6de-116">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="3f6de-116">Property value/Return value</span></span>

<span data-ttu-id="3f6de-117">Si _pxAction_ est, ou peut être forcé, le nombre 1, votre implémentation de cette fonction doit renvoyer une chaîne contenant des informations sur le complément, généralement son nom et peut-être un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="3f6de-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="3f6de-118">Sinon, il doit retourner #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="3f6de-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="3f6de-119">Si vous ne renvoyez pas de chaîne, Excel essaie de convertir la valeur renvoyée en chaîne.</span><span class="sxs-lookup"><span data-stu-id="3f6de-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f6de-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f6de-120">Remarks</span></span>

<span data-ttu-id="3f6de-121">Si la chaîne renvoyée pointe vers la mémoire tampon allouée dynamiquement, vous devez vous assurer que cette mémoire tampon est finalement libérée.</span><span class="sxs-lookup"><span data-stu-id="3f6de-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="3f6de-122">Si la chaîne a été allouée par Excel, vous pouvez le faire en définissant **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="3f6de-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="3f6de-123">Si la chaîne a été allouée par la DLL, vous devez le faire en définissant **xlbitDLLFree**, et vous devez également l'implémenter dans [xlAutoFree](xlautofree-xlautofree12.md) (si vous renvoyez un **XLOPER**) ou **XlAutoFree12** (si vous renvoyez un **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="3f6de-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="3f6de-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f6de-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="3f6de-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f6de-125">See also</span></span>



[<span data-ttu-id="3f6de-126">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="3f6de-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

