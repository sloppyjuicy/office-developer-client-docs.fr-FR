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
ms.localizationpriority: medium
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
ms.openlocfilehash: bc8a4d85a21add0c98a06701b2ca4581b5c31c25
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198717"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Tente de convertir un **xlREF12** en **xlREF**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Paramètres

 _pxRef12_ (**LPXLREF12**)
  
Pointeur vers la structure de référence source.
  
 _pxRef_ (**LPXLREF**)
  
Pointeur vers la structure de référence cible dans laquelle la valeur convertie doit être placée.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 **TRUE** si la conversion a réussi, FALSE dans **le** cas contraire. 
  
## <a name="remarks"></a>Remarques

La conversion de **XLREF12** en **XLREF** échoue si la référence fournie fait référence à une partie d’une feuille de calcul Excel 2007 qui n’est pas prise en charge dans les versions antérieures. 
  
## <a name="example"></a>Exemple

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

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

