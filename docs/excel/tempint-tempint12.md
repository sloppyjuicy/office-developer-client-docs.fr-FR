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
- fonction tempint12 [excel 2007], fonction TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782198"
---
# <a name="tempinttempint12"></a><span data-ttu-id="bd27e-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="bd27e-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="bd27e-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bd27e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bd27e-106">Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant un nombre entier.</span><span class="sxs-lookup"><span data-stu-id="bd27e-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="bd27e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd27e-107">Parameters</span></span>

 <span data-ttu-id="bd27e-108">_J’ai_</span><span class="sxs-lookup"><span data-stu-id="bd27e-108">_i_</span></span>
  
<span data-ttu-id="bd27e-109">Valeur entière concerné.</span><span class="sxs-lookup"><span data-stu-id="bd27e-109">The intended integer value.</span></span> <span data-ttu-id="bd27e-110">Notez que l’entier **XLOPER** est un nombre entier signé de 16 bits (int court), tandis que l’entier **XLOPER12** est un nombre entier signé de 32 bits (int [durée]).</span><span class="sxs-lookup"><span data-stu-id="bd27e-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="bd27e-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bd27e-111">Return value</span></span>

<span data-ttu-id="bd27e-112">Renvoie un entier **xltypeInt** contenant la valeur passée.</span><span class="sxs-lookup"><span data-stu-id="bd27e-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bd27e-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd27e-113">Example</span></span>

<span data-ttu-id="bd27e-114">Cet exemple utilise la fonction **TempInt12** pour passer un argument à **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="bd27e-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="bd27e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd27e-115">See also</span></span>



[<span data-ttu-id="bd27e-116">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="bd27e-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

