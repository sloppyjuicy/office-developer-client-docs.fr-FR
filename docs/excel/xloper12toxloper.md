---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- fonction xloper12toxloper [excel 2007]
ms.localizationpriority: medium
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
ms.openlocfilehash: 0118c1f801542a631586cc0a4eae79339902b64a
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523541"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Routine de conversion utilisée pour convertir de la nouvelle **XLOPER12** à l’ancienne **XLOPER**.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Paramètres

_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la source **XLOPER12** à convertir.
  
_pxloper_ (**LPXLOPER**)
  
Pointeur vers la **XLOPER cible** pour contenir la valeur convertie.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

**TRUE** si la conversion a réussi, **FALSE dans le** cas contraire.
  
## <a name="remarks"></a>Remarques

Selon le type de **XLOPER12**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées vers la **XLOPER cible**. L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est réussie . **FreeXLOperT peut** être utilisé, ou vous pouvez le faire directement à l’aide de **la gratuité**.
  
Si la conversion échoue, l’appelant n’a pas besoin de libérer de mémoire.
  
La conversion d’une **xlOPER12** en **XLOPER** peut échouer lorsque la **XLOPER12** contient un tableau ou une référence trop grand ou une chaîne trop longue pour que la **XLOPER** contienne.
  
**XLOPER12** Les chaînes unicode à caractères larges sont converties en chaînes d’byte **XLOPER** ASCII d’une manière qui dépend des paramètres régionaux.
  
**XlOPER12** **xltypeInt** est un integer signé 32 bits, tandis que **xlOPER** **xltypeInt** est un integer signé 16 bits. Lorsqu’un nombre integer **XLOPER12** fourni dépasse la limite d’un nombre integer **XLOPER** , l’integer est converti en un double de 8 caractères et renvoyé dans une **XLOPER** de type **xltypeNum**. Il s’agit du seul cas dans lequel cette fonction modifie le type de la **XLOPER convertie**.
  
### <a name="example"></a>Exemple

Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)
