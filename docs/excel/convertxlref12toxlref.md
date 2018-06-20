---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- fonction convertxlref12toxlref [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782016"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="0c7e3-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="0c7e3-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="0c7e3-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c7e3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0c7e3-106">Tente de convertir un **XLREF12** un **XLREF**.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="0c7e3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c7e3-107">Parameters</span></span>

 <span data-ttu-id="0c7e3-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="0c7e3-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="0c7e3-109">Pointeur vers la structure de référence source.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="0c7e3-110">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="0c7e3-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="0c7e3-111">Pointeur vers la structure de référence cible dans lequel la valeur convertie doit être placé.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0c7e3-112">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0c7e3-112">Property value/Return value</span></span>

 <span data-ttu-id="0c7e3-113">**TRUE** si la conversion a réussi, **FALSE** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c7e3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c7e3-114">Remarks</span></span>

<span data-ttu-id="0c7e3-115">La conversion de **XLREF12** en **XLREF** échoue si la référence fournie fait référence à la partie d’une feuille de calcul Excel 2007 qui n’est pas pris en charge dans les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="0c7e3-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0c7e3-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="0c7e3-116">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="0c7e3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c7e3-117">See also</span></span>



[<span data-ttu-id="0c7e3-118">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="0c7e3-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

