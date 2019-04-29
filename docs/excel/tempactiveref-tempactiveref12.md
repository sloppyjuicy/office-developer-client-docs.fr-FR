---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- fonction tempactiveref [Excel 2007], fonction TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415543"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d'infrastructure qui crée ****/ **** une liste composée temporaire contenant une référence externe au bloc rectangulaire de cellules dans la feuille active. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Paramètres

 _rwFirst_
  
Ligne de départ de la référence.
  
 _rwLast_
  
Ligne de fin de la référence.
  
Les arguments de ligne sont basés sur zéro de sorte que la ligne 1 est transmise à 0. Dans Microsoft Office Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et représente la valeur maximale pouvant être prise par un entier de mot. À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 1 048 575 = 2 ^ 20-1. RW est défini comme un entier signé 32 bits dans XLCALL. H.
  
 _colFirst_
  
Numéro de la colonne de départ de la référence.
  
 _colLast_
  
Numéro de la dernière colonne de la référence.
  
Les arguments de colonne sont basés sur zéro de sorte que la colonne A passe à la valeur 0. Dans Excel 2003 et les versions antérieures, et en commençant dans Excel 2007 exécutant un classeur en mode de compatibilité, la valeur maximale est 255 = 2 ^ 8-1 et est la valeur maximale pouvant être prise par un nombre entier d'octets. À partir d'Excel 2007 exécutant un classeur, la valeur maximale est 16 383 = 2 ^ 14-1. COL est défini comme un entier signé de 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence externe **xltypeRef** au bloc rectangulaire de cellules transmis. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempActiveRef12** pour sélectionner les cellules A105: C110. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

