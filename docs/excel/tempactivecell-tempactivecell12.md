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
- fonction TempActiveCell12 [Excel 2007], fonction TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301574"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque d'infrastructure qui créent une liste **XLOPER**/ **** temporaire contenant une référence externe à une cellule de la feuille active. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Paramètres

 _colonne_
  
Ligne à référencer. Les arguments de ligne sont basés sur zéro de sorte que la ligne 1 est transmise à 0. Dans Microsoft Office Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et représente la valeur maximale pouvant être prise par un entier de mot. À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 1 048 575 = 2 ^ 20-1. RW est défini comme un entier signé 32 bits dans XLCALL. H.
  
 _n°5_
  
Colonne à référencer. Il s'agit d'un type de base zéro de sorte que la colonne A passe à la valeur 0. Dans Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 255 = 2 ^ 8-1 et est la valeur maximale pouvant être prise par un nombre entier d'octets. À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 16 383 = 2 ^ 14-1. COL est défini comme un entier signé de 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence externe **xltypeRef** à la cellule transmise. 
  
## <a name="example"></a>Exemple

L'exemple suivant utilise **TempActiveCell12** pour afficher le contenu de B94 sur la feuille active. 
  
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

