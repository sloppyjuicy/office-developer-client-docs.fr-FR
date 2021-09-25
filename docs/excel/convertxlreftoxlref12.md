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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f0f48a473024003628a3d0ec1059b4a4a971b78c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601400"
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

