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
- fonction tempactivecell12 [excel 2007], fonction TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782187"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque Framework qui créent un temporaire **XLOPER**/ **XLOPER12** contenant une référence à une cellule dans la feuille active. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Paramètres

 _ligne_
  
La ligne à référencer. Arguments de ligne commencent par zéro afin que la ligne 1 est transmise en tant que 0. Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et la valeur maximale qui peut être effectuée par un nombre entier de WORD. À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 1 048 575 = 2 ^ 20-1. RW est défini comme un entier signé 32 bits dans XLCALL. H.
  
 _col_
  
La colonne à référencer. Il s’agit en partant de zéro afin que la colonne A est transmise en tant que 0. Dans Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est de 255 = 2 ^ 8-1 et la valeur maximale qui peut être effectuée par un entier. À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 16 383 = 2 ^ 14-1. COL est défini comme un entier signé 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une référence externe **xltypeRef** à la cellule passée. 
  
## <a name="example"></a>Exemple

L’exemple suivant utilise **TempActiveCell12** pour afficher le contenu de B94 dans la feuille active. 
  
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

