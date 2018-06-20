---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- fonction tempactiverow [excel 2007], fonction TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782188"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque Framework qui créent un temporaire **XLOPER**/ **XLOPER12** contenant une référence à une ligne entière de la feuille active. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Paramètres

 _ligne_
  
La ligne à référencer. Arguments de ligne commencent par zéro afin que la ligne 1 est transmise en tant que 0. Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et la valeur maximale qui peut être effectuée par un nombre entier de WORD. À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 1 048 575 = 2 ^ 20-1. RW est défini comme un entier signé 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une référence externe **xltypeRef** aux cellules de ligne passé. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempActiveRow12** pour sélectionner ligne 113. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

