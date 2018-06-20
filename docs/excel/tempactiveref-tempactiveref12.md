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
- fonction tempactiveref [excel 2007], fonction TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782190"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant une référence à un bloc rectangulaire de cellules dans la feuille active. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Paramètres

 _rwFirst_
  
La ligne de début de la référence.
  
 _rwLast_
  
La ligne de fin de la référence.
  
Arguments de ligne commencent par zéro afin que la ligne 1 est transmise en tant que 0. Dans Microsoft Office Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est 65 535 = 2 ^ 16-1 et la valeur maximale qui peut être effectuée par un nombre entier de WORD. À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 1 048 575 = 2 ^ 20-1. RW est défini comme un entier signé 32 bits dans XLCALL. H.
  
 _colFirst_
  
Le numéro de colonne de départ de la référence.
  
 _colLast_
  
Numéro de colonne de fin de la référence.
  
Arguments de colonne sont de base zéro afin que la colonne A est transmise en tant que 0. Dans Excel 2003 et les précédentes versions et à compter d’Excel 2007 en cours d’exécution un classeur en mode de compatibilité, la valeur maximale est de 255 = 2 ^ 8-1 et la valeur maximale qui peut être effectuée par un entier. À compter d’Excel 2007, un classeur en cours d’exécution, la valeur maximale est de 16 383 = 2 ^ 14-1. COL est défini comme un entier signé 32 bits dans XLCALL. H.
  
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une référence externe **xltypeRef** au bloc de cellules passé rectangulaire. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempActiveRef12** pour sélectionner les cellules A105:C110. 
  
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

