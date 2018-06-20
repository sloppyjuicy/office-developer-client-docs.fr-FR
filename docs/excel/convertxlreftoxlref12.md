---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- fonction convertxlreftoxlref12 [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782023"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="d0c2b-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="d0c2b-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="d0c2b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d0c2b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d0c2b-106">Fonction de la structure qui tente de convertir un **XLREF** un **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="d0c2b-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="d0c2b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c2b-107">Parameters</span></span>

 <span data-ttu-id="d0c2b-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="d0c2b-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="d0c2b-109">Pointeur vers la structure de référence source.</span><span class="sxs-lookup"><span data-stu-id="d0c2b-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="d0c2b-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="d0c2b-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="d0c2b-111">Pointeur vers la structure de référence cible dans lequel la valeur convertie doit être placé.</span><span class="sxs-lookup"><span data-stu-id="d0c2b-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d0c2b-112">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d0c2b-112">Property value/Return value</span></span>

 <span data-ttu-id="d0c2b-113">**TRUE** si la conversion a réussi, **FALSE** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d0c2b-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0c2b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0c2b-114">Remarks</span></span>

<span data-ttu-id="d0c2b-115">À condition que le passé dans **XLREF** est valide, cette opération doit toujours être réussie.</span><span class="sxs-lookup"><span data-stu-id="d0c2b-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="d0c2b-116">En revanche, l’autre moyen de **XLREF12** **XLREF**, effectuée par [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), Échec de conversion si la référence fournie fait référence à la partie d’une feuille de calcul Excel 2007 n’est pas pris en charge dans les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="d0c2b-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="d0c2b-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="d0c2b-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d0c2b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c2b-118">See also</span></span>



[<span data-ttu-id="d0c2b-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="d0c2b-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

