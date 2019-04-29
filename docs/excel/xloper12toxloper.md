---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- fonction XLOper12ToXLOper [Excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422907"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Routine de conversion utilisée pour convertir la nouvelle **XLOPER12** en l'ancien **XLOPER**.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Paramètres

_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la source **XLOPER12** à convertir. 
  
_pxloper_ (**LPXLOPER**)
  
Pointeur vers le **XLOPER** cible pour contenir la valeur convertie. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

**True** si la conversion a réussi **** , false dans le cas contraire. 
  
## <a name="remarks"></a>Remarques

Selon le type de **XLOPER12**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées dans le **XLOPER**cible. L'appelant est chargé de libérer de la mémoire associée à la copie si la conversion a réussi; **FreeXLOperT** peut être utilisé ou peut être réalisé directement à l'aide de la version **gratuite**.
  
Si la conversion échoue, l'appelant n'a pas besoin de libérer de la mémoire.
  
La conversion d'un **XLOPER12** en une structure **XLOPER** peut échouer lorsque la variable **XLOPER12** contient un tableau ou une référence trop grande ou une chaîne trop longue pour l' **XLOPER** à contenir. 
  
**XLOPER12** Les chaînes de caractères larges Unicode sont converties en chaînes d'octets **XLOPER** ASCII d'une façon qui dépend des paramètres régionaux. 
  
La **** **xltypeInt** XLOPER12 est un entier signé de 32 bits, tandis que le **XLOPER** **xltypeInt** est un entier signé 16 bits. Lorsqu'un entier **XLOPER12** fourni dépasse la limite d'un entier **XLOPER** , l'entier est converti en double de 8 octets et renvoyé dans un **XLOPER** de type **xltypeNum**. Il s'agit du seul cas où cette fonction modifie le type de l' **XLOPER**converti.
  
### <a name="example"></a>Exemple

Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction. 
  
## <a name="see-also"></a>Voir aussi

- [Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

