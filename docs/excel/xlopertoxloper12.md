---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- fonction xlopertoxloper12 [excel 2007]
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
  
Routine de conversion utilisée pour convertir de l’ancienne **XLOPER** vers la **nouvelle XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameters

_pxloper_ (**LPXLOPER**)
  
Pointeur vers la **XLOPER** source à convertir. 
  
_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la **xlOPER12** cible pour contenir la valeur convertie. 
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

**TRUE** si la conversion a réussi, FALSE dans **le** cas contraire. 
  
## <a name="remarks"></a>Remarques

Selon le type de **XLOPER**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées vers la **xlOPER12 cible.** L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est réussie ; **FreeXLOper12T** peut être utilisé, ou vous pouvez le faire directement à l’aide **de la gratuité.**
  
Si la conversion échoue, l’appelant n’a pas besoin de libérer de mémoire.
  
En règle générale, la conversion de **toute XLOPER** en **XLOPER12** est possible. En revanche, la conversion d’une **xlOPER12** en **XLOPER** peut échouer lorsque la **XLOPER12** contient un tableau ou une référence trop grand ou une chaîne trop longue pour que la **XLOPER** contienne. 
  
**XLOPER** Les chaînes d’byte ASCII sont converties en chaînes à caractères larges **XLOPER12** Unicode d’une manière qui dépend des paramètres régionaux. 
  
### <a name="example"></a>Exemple

Consultez le  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` fichier pour le code de cette fonction. 
  

