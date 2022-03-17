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
ms.localizationpriority: medium
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
ms.openlocfilehash: d8598a1ad47ddb493a4723c8946cc86e7661a136
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519992"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Routine de conversion utilisée pour convertir de l’ancienne **XLOPER** vers la **nouvelle XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Paramètres

_pxloper_ (**LPXLOPER**)
  
Pointeur vers la **XLOPER** source à convertir.
  
_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la **xlOPER12** cible pour contenir la valeur convertie.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

**TRUE** si la conversion a réussi, **FALSE dans le** cas contraire.
  
## <a name="remarks"></a>Remarques

Selon le type de **XLOPER**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties, qui sont pointées vers la **xlOPER12 cible**. L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est réussie . **FreeXLOper12T** peut être utilisé ou peut être effectué directement à l’aide **de la gratuité**.
  
Si la conversion échoue, l’appelant n’a pas besoin de libérer de mémoire.
  
En règle générale, la conversion de **toute XLOPER** en **XLOPER12** est possible. En revanche, la conversion d’une **xlOPER12** en **XLOPER** peut échouer lorsque la **XLOPER12** contient un tableau ou une référence trop grand ou une chaîne trop longue pour que la **XLOPER** contienne.
  
**XLOPER** Les chaînes d’byte ASCII sont converties en chaînes à caractères larges **XLOPER12** Unicode d’une manière qui dépend des paramètres régionaux.
  
### <a name="example"></a>Exemple

Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction.
  