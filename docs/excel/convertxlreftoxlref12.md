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
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de la structure qui tente de convertir un **XLREF** un **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Paramètres

 _pxRef_ (**LPXLREF**)
  
Pointeur vers la structure de référence source.
  
 _pxRef12_ (**LPXLREF12**)
  
Pointeur vers la structure de référence cible dans lequel la valeur convertie doit être placé.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

 **TRUE** si la conversion a réussi, **FALSE** dans le cas contraire. 
  
## <a name="remarks"></a>Remarques

À condition que le passé dans **XLREF** est valide, cette opération doit toujours être réussie. En revanche, l’autre moyen de **XLREF12** **XLREF**, effectuée par [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), Échec de conversion si la référence fournie fait référence à la partie d’une feuille de calcul Excel 2007 n’est pas pris en charge dans les versions antérieures.
  
## <a name="example"></a>Exemple

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

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

