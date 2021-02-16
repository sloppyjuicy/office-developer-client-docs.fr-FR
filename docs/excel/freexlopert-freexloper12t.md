---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- fonction freexlopert [excel 2007],Fonction FreeXLOper12T [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0b604cbe5cb24ac7d8de28278dfbcf0d4fd92c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421521"
---
# <a name="freexlopertfreexloper12t"></a><span data-ttu-id="72256-104">FreeXLOperT/FreeXLOper12T</span><span class="sxs-lookup"><span data-stu-id="72256-104">FreeXLOperT/FreeXLOper12T</span></span>

 <span data-ttu-id="72256-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="72256-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="72256-106">Fonction Framework qui libère la mémoire associée à **une structure** /  **XLOPER XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="72256-106">Framework function that frees memory associated with an **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="72256-107">La fonction suppose que la mémoire a été allouée avec des appels à malloc dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="72256-107">The function assumes that the memory was allocated with calls to malloc within the DLL.</span></span> <span data-ttu-id="72256-108">Si la mémoire a été allouée par Microsoft Excel ou d’une autre manière ou par un autre processus, cette fonction ne doit pas être utilisée pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="72256-108">If the memory was allocated by Microsoft Excel or in some other way or by some other process, this function should not be used to free the memory.</span></span> <span data-ttu-id="72256-109">Utilisez [xlFree pour](xlfree.md) libérer de la mémoire allouée par Excel pour  /  **XLOPER XLOPER12** s.</span><span class="sxs-lookup"><span data-stu-id="72256-109">Use [xlFree](xlfree.md) to free memory allocated by Excel for **XLOPER**/ **XLOPER12** s.</span></span> 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="72256-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72256-110">Parameters</span></span>

 <span data-ttu-id="72256-111">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="72256-111">_pxloper_ (**LPXLOPER**)</span></span>
  
 <span data-ttu-id="72256-112">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="72256-112">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="72256-113">Pointeur vers **la XLOPER** /  **XLOPER12** à libérer.</span><span class="sxs-lookup"><span data-stu-id="72256-113">Pointer to the **XLOPER**/ **XLOPER12** to be freed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="72256-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="72256-114">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a><span data-ttu-id="72256-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72256-115">See also</span></span>



[<span data-ttu-id="72256-116">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="72256-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

