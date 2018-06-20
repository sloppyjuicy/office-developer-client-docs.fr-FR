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
- fonction tempactivecolumn12 [excel 2007], fonction TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782193"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque Framework qui créent un temporaire **XLOPER**/ **XLOPER12** contenant une référence à une colonne entière de la feuille active. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Paramètres

 _col_ (**Octets**)
  
La colonne à référencer. Il s’agit en partant de zéro afin que la colonne A est transmise en tant que 0. Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est de 255 = 2 ^ 8-1 et la valeur maximale qui peut être effectuée par un entier. À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 16 383 = 2 ^ 14-1. COL est défini comme un entier signé 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une référence externe **xltypeRef** à la colonne passée. 
  
## <a name="example"></a>Exemple

L’exemple suivant utilise **TempActiveColumn12** pour sélectionner toute la colonne B. 
  
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

