---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- fonction tempint12 [Excel 2007], fonction TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438749"
---
# <a name="tempinttempint12"></a><span data-ttu-id="fba5e-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="fba5e-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="fba5e-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fba5e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fba5e-106">Fonction de bibliothèque d'infrastructure qui crée une expression **XLOPER**/ \*\*\*\* temporaire contenant un entier.</span><span class="sxs-lookup"><span data-stu-id="fba5e-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="fba5e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fba5e-107">Parameters</span></span>

 <span data-ttu-id="fba5e-108">_i_</span><span class="sxs-lookup"><span data-stu-id="fba5e-108">_i_</span></span>
  
<span data-ttu-id="fba5e-109">Valeur entière prévue.</span><span class="sxs-lookup"><span data-stu-id="fba5e-109">The intended integer value.</span></span> <span data-ttu-id="fba5e-110">Notez que l'entier **XLOPER** est un entier 16 bits signé (short int), tandis que l'entier **XLOPER12** est un entier 32 bits signé ([long] int).</span><span class="sxs-lookup"><span data-stu-id="fba5e-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="fba5e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fba5e-111">Return value</span></span>

<span data-ttu-id="fba5e-112">Renvoie un entier **xltypeInt** contenant la valeur passée.</span><span class="sxs-lookup"><span data-stu-id="fba5e-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fba5e-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="fba5e-113">Example</span></span>

<span data-ttu-id="fba5e-114">Cet exemple utilise la fonction **TempInt12** pour transmettre un argument à **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="fba5e-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="fba5e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fba5e-115">See also</span></span>



[<span data-ttu-id="fba5e-116">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="fba5e-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

