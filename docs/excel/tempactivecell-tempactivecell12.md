---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- fonction tempactivecell12 [excel 2007],TempActiveCell function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 70222ff1e057427d6964ea6cae166f1ad08481ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611272"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de bibliothèque d’infrastructure qui créent une **XLOPER** /  **XLOPER12** temporaire contenant une référence externe à une cellule de la feuille active. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Paramètres

 _row_
  
Ligne à référencer. Les arguments de ligne sont basés sur zéro afin que la ligne 1 soit passée en tant que 0. Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 65 535 = 2^16 - 1 et est la valeur maximale qui peut être prise par un nombre total WORD. À compter Excel 2007 exécutant un manuel, la valeur maximale est 1 048 575 = 2^20 - 1. RW est défini comme un integer signé 32 bits dans XLCALL.H.
  
 _col_
  
Colonne à référencer. Il s’agit d’une valeur de base zéro afin que la colonne A soit passée sous la valeur 0. Dans Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 255 = 2^8 - 1 et est la valeur maximale qui peut être prise par un nombre d’nombres byTE. À partir Excel 2007 exécutant un manuel, la valeur maximale est 16 383 = 2^14 - 1. Col est défini comme un integer signé 32 bits dans XLCALL.H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une **référence externe xltypeRef** à la cellule transmise. 
  
## <a name="example"></a>Exemple

L’exemple suivant **utilise TempActiveCell12** pour afficher le contenu de B94 sur la feuille active. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

