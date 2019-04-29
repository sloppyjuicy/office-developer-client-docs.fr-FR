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
- fonction tempactiverow [Excel 2007], fonction TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413107"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonctions de la bibliothèque d'infrastructure qui créent une liste **XLOPER**/ **** temporaire contenant une référence externe à une ligne entière dans la feuille active. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Paramètres

 _colonne_
  
Ligne à référencer. Les arguments de ligne sont basés sur zéro de sorte que la ligne 1 est transmise à 0. Dans Microsoft Office Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et représente la valeur maximale pouvant être prise par un entier de mot. À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 1 048 575 = 2 ^ 20-1. RW est défini comme un entier signé 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence externe **xltypeRef** aux cellules de ligne transmises. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempActiveRow12** pour sélectionner la ligne 113. 
  
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

