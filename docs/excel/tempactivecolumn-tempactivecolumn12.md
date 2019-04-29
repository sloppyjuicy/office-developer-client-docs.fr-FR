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
- fonction TempActiveColumn12 [Excel 2007], fonction TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417874"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque d'infrastructure qui créent une liste **XLOPER**/ **** temporaire contenant une référence externe à une colonne entière sur la feuille active. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Paramètres

 _col_ (**Octet**)
  
Colonne à référencer. Il s'agit d'un type de base zéro de sorte que la colonne A passe à la valeur 0. Dans Microsoft Office Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 255 = 2 ^ 8-1 et représente la valeur maximale pouvant être prise par un nombre entier d'octets. À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 16 383 = 2 ^ 14-1. COL est défini comme un entier signé de 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence externe **xltypeRef** à la colonne passée. 
  
## <a name="example"></a>Exemple

L'exemple suivant utilise **TempActiveColumn12** pour sélectionner toute la colonne B. 
  
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

