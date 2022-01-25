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
ms.localizationpriority: medium
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
ms.openlocfilehash: acf4147df5b419bf1275370b352c6491d09fb960
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199268"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction Framework qui tente de convertir un **xlREF** en **xlREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Paramètres

 _pxRef_ (**LPXLREF**)
  
Pointeur vers la structure de référence source.
  
 _pxRef12_ (**LPXLREF12**)
  
Pointeur vers la structure de référence cible dans laquelle la valeur convertie doit être placée.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

 **TRUE** si la conversion a réussi, FALSE dans **le** cas contraire. 
  
## <a name="remarks"></a>Remarques

À condition que la **xlREF** transmise soit valide, cette opération doit toujours réussir. En revanche, la conversion de **XLREF12** en **XLREF**, effectuée par [ConvertXLRef12ToXLRef,](convertxlref12toxlref.md)échoue si la référence fournie fait référence à une partie d’une feuille de calcul Excel 2007 qui n’est pas prise en charge dans les versions antérieures.
  
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

