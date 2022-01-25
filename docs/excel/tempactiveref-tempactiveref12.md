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
- fonction tempactiveref [excel 2007],TempActiveRef12 function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
ms.openlocfilehash: 56ac8a96bb3a9dea883f6929e07defef1f99484f
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199723"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque d’infrastructure qui crée une **xlOPER** /  **XLOPER12** temporaire contenant une référence externe à un bloc rectangulaire de cellules sur la feuille active. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Paramètres

 _rwFirst_
  
Ligne de début de la référence.
  
 _rwLast_
  
Ligne de fin de la référence.
  
Les arguments de ligne sont basés sur zéro afin que la ligne 1 soit passée en tant que 0. Dans Microsoft Office Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 65 535 = 2^16 - 1 et est la valeur maximale qui peut être prise par un nombre total WORD. À partir Excel 2007 exécutant un manuel, la valeur maximale est 1 048 575 = 2^20 - 1. RW est défini comme un integer signé 32 bits dans XLCALL.H.
  
 _colFirst_
  
Numéro de colonne de début de la référence.
  
 _colLast_
  
Numéro de colonne de fin de la référence.
  
Les arguments de colonne sont basés sur zéro afin que la colonne A soit passée sous la valeur 0. Dans Excel 2003 et versions antérieures, et à partir de Excel 2007 exécutant un livre de travail en mode de compatibilité, la valeur maximale est 255 = 2^8 - 1 et est la valeur maximale qui peut être prise par un nombre d’nombres byTE. À partir Excel 2007 exécutant un manuel, la valeur maximale est 16 383 = 2^14 - 1. Col est défini comme un integer signé 32 bits dans XLCALL.H.
  
## <a name="return-value"></a>Valeur renvoyée

Renvoie une **référence externe xltypeRef** à un bloc rectangulaire de cellules transmises. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la **fonction TempActiveRef12** pour sélectionner les cellules A105:C110. 
  
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

