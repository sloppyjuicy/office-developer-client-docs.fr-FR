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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782254"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Routine de conversion utilisée pour convertir l' ancien **XLOPER** vers le nouveau **XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Paramètres

_pxloper_ (**LPXLOPER**)
  
Pointeur vers la source **XLOPER** à convertir. 
  
_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la cible **XLOPER12** contenant la valeur convertie. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

**TRUE** si la conversion a réussi, **FALSE** dans le cas contraire. 
  
## <a name="remarks"></a>Remarques

Selon le type de l' **élément XLOPER**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties qui pointent sur la cible **XLOPER12**. L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est un succès ; **FreeXLOper12T** peut être utilisé, ou elle peut être effectuée directement à l’aide **disponible**.
  
En cas d’échec de la conversion, l’appelant n’a pas besoin libérer de la mémoire.
  
En règle générale, la conversion à partir de n’importe quel **XLOPER** un **XLOPER12** est possible. En revanche, conversion d’un **XLOPER12** vers un **XLOPER** peut échouer lorsque le **XLOPER12** contient un tableau ou référence qui est trop grande ou une chaîne qui est trop longue pour le **XLOPER** contenir. 
  
**XLOPER** Chaînes d’octets ASCII sont convertis en chaînes de caractères larges **XLOPER12** Unicode d’une manière qui dépend des paramètres régionaux. 
  
### <a name="example"></a>Exemple

Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction. 
  

