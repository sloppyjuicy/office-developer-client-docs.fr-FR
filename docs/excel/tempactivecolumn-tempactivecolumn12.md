---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- fonction tempactivecolumn12 [excel 2007],TempActiveColumn function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
ms.openlocfilehash: 91a8935eabb3944bae50324f712f72c189a38d4f
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198470"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de bibliothèque d’infrastructure qui créent une **XLOPER XLOPER12** temporaire contenant une référence externe à une colonne /   entière de la feuille active. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Paramètres

 _col_ (**BYTE**)
  
Colonne à référencer. En fonction de zéro, la colonne A est passée sous la valeur 0. Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 255 = 2^8 - 1 et est la valeur maximale qui peut être prise par un nombre d’nombres byTE. À partir Excel 2007 exécutant un manuel, la valeur maximale est 16 383 = 2^14 - 1. Col est défini comme un integer signé 32 bits dans XLCALL.H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une **référence externe xltypeRef** à la colonne transmise. 
  
## <a name="example"></a>Exemple

L’exemple suivant **utilise TempActiveColumn12** pour sélectionner la colonne entière B. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

