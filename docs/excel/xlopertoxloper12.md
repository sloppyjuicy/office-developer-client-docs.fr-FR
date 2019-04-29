---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- fonction xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404595"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Routine de conversion utilisée pour convertir une ancienne forme **XLOPER** en une nouvelle **XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Paramètres

_pxloper_ (**LPXLOPER**)
  
Pointeur vers le **XLOPER** source à convertir. 
  
_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la cible **XLOPER12** cible pour contenir la valeur convertie. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

**True** si la conversion a réussi **** , false dans le cas contraire. 
  
## <a name="remarks"></a>Remarques

Selon le type de l' **XLOPER**, cette fonction alloue une nouvelle mémoire tampon de mémoire pour les valeurs converties, qui sont pointées dans le **XLOPER12**cible. L'appelant est chargé de libérer de la mémoire associée à la copie si la conversion a réussi; **FreeXLOper12T** peut être utilisé ou peut être réalisé directement à l'aide de **Free**.
  
Si la conversion échoue, l'appelant n'a pas besoin de libérer de la mémoire.
  
En règle générale, la conversion d'une structure **XLOPER** en une expression **XLOPER12** est possible. En revanche, la conversion d'un **XLOPER12** en une structure **XLOPER** peut échouer lorsque la variable **XLOPER12** contient un tableau ou une référence trop grande ou une chaîne trop longue pour l' **XLOPER** à contenir. 
  
**XLOPER** Les chaînes d'octets ASCII sont **** converties en chaînes de caractères larges Unicode et conformes aux paramètres régionaux. 
  
### <a name="example"></a>Exemple

Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction. 
  

