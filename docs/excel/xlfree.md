---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- fonction xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782230"
---
# <a name="xlfree"></a><span data-ttu-id="f2bcf-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="f2bcf-104">xlFree</span></span>

 <span data-ttu-id="f2bcf-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2bcf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f2bcf-106">Utilisé pour libérer de la mémoire de ressources alloués par Microsoft Excel lors de la création du retour valeur **XLOPER**/ **XLOPER12** dans un appel à [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="f2bcf-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="f2bcf-107">La fonction **xlFree** libère la mémoire auxiliaire et réinitialise le pointeur de la **valeur null** , mais ne supprime pas les autres parties de la **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="f2bcf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2bcf-108">Parameters</span></span>

 <span data-ttu-id="f2bcf-109">_px_1,..., px_n_</span><span class="sxs-lookup"><span data-stu-id="f2bcf-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="f2bcf-110">Un ou plusieurs **XLOPER**/ s**XLOPER12**à libérer.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-110">One or more **XLOPER**/ **XLOPER12**s to be freed.</span></span> <span data-ttu-id="f2bcf-111">Dans les versions Excel jusqu'à 2003, le nombre maximal de pointeurs qui peut être passé est 30.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="f2bcf-112">À compter d’Excel 2007, il est augmentée à 255.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f2bcf-113">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f2bcf-113">Property value/Return value</span></span>

<span data-ttu-id="f2bcf-114">Cette fonction ne retourne pas une valeur.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2bcf-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2bcf-115">Remarks</span></span>

<span data-ttu-id="f2bcf-116">Vous devez libérer chaque **XLOPER** que vous obtenez en tant qu’une valeur de retour **Excel4** ou **Excel4v** et chaque **XLOPER12** que vous obtenez comme valeur de retour **d’Excel12** ou **Excel12v** s’il s’agit des types suivants : xltypeStr ** **, **xltypeMulti**ou **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="f2bcf-117">Il est recommandé d’autres types de même si elles n’utilisent pas la mémoire auxiliaire, dans la mesure où les obtenue depuis **Excel4** ou **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="f2bcf-118">Lorsque vous retournez à Excel un pointeur vers un **XLOPER**/ **XLOPER12** qui contient toujours mémoire allouée Excel à libérer, vous devez définir la **xlbitXLFree** la mémoire pour les versions d’Excel.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f2bcf-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2bcf-119">Example</span></span>

<span data-ttu-id="f2bcf-120">Cet exemple appelle **obtenir. WORKSPACE(1)** pour renvoyer la plate-forme les Excel est en cours d’exécution sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="f2bcf-121">Le code copie ce retourné de chaîne dans une mémoire tampon pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="f2bcf-122">Le code place la mémoire tampon dans le **XLOPER12** pour une utilisation ultérieure avec la fonction Excel.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="f2bcf-123">Enfin, le code affiche la chaîne dans un message d’alerte.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-123">Finally, the code displays the string in an alert box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f2bcf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2bcf-124">See also</span></span>

- [<span data-ttu-id="f2bcf-125">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="f2bcf-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

