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
- tempactiverow function [excel 2007],TempActiveRow12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
ms.openlocfilehash: 2718570fea5fc8b52d9c8f5ff38e2ce11d0c906d
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198189"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de bibliothèque d’infrastructure qui créent une **XLOPER XLOPER12** temporaire contenant une référence externe à une ligne /   entière de la feuille active. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Paramètres

 _row_
  
Ligne à référencer. Les arguments de ligne sont basés sur zéro afin que la ligne 1 soit passée en tant que 0. Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 65 535 = 2^16 - 1 et est la valeur maximale qui peut être prise par un nombre total WORD. À partir Excel 2007 exécutant un manuel, la valeur maximale est 1 048 575 = 2^20 - 1. RW est défini comme un integer signé 32 bits dans XLCALL.H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une **référence externe xltypeRef** aux cellules de ligne transmises. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction TempActiveRow12** pour sélectionner la ligne 113. 
  
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

