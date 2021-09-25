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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0c3a629dc8c036508f81b65e8ec7d4b6a8525c39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562012"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de bibliothèque d’infrastructure qui créent une **XLOPER** /  **XLOPER12** temporaire contenant une référence externe à une ligne entière de la feuille active. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Paramètres

 _row_
  
Ligne à référencer. Les arguments de ligne sont basés sur zéro afin que la ligne 1 soit passée en tant que 0. Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 65 535 = 2^16 - 1 et est la valeur maximale qui peut être prise par un nombre total WORD. À compter Excel 2007 exécutant un manuel, la valeur maximale est 1 048 575 = 2^20 - 1. RW est défini comme un integer signé 32 bits dans XLCALL.H.
  
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

