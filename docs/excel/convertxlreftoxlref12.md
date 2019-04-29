---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- fonction convertxlreftoxlref12 [Excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432029"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="6dc9d-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="6dc9d-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="6dc9d-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6dc9d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6dc9d-106">Fonction de l'infrastructure qui tente de convertir un **XLREF** en **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="6dc9d-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="6dc9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6dc9d-107">Parameters</span></span>

 <span data-ttu-id="6dc9d-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="6dc9d-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="6dc9d-109">Pointeur vers la structure de référence source.</span><span class="sxs-lookup"><span data-stu-id="6dc9d-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="6dc9d-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="6dc9d-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="6dc9d-111">Pointeur vers la structure de référence cible dans laquelle la valeur convertie doit être placée.</span><span class="sxs-lookup"><span data-stu-id="6dc9d-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6dc9d-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="6dc9d-112">Property value/Return value</span></span>

 <span data-ttu-id="6dc9d-113">**True** si la conversion a réussi \*\*\*\* , false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6dc9d-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6dc9d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6dc9d-114">Remarks</span></span>

<span data-ttu-id="6dc9d-115">Si le **XLREF** transmis est valide, cette opération doit toujours aboutir.</span><span class="sxs-lookup"><span data-stu-id="6dc9d-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="6dc9d-116">En revanche, la conversion de **XLREF12** vers **XLREF**, effectuée par [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), échoue si la référence fournie fait référence à une partie d'une feuille de calcul Excel 2007 qui n'est pas prise en charge dans les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="6dc9d-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="6dc9d-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="6dc9d-117">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="6dc9d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dc9d-118">See also</span></span>



[<span data-ttu-id="6dc9d-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="6dc9d-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

