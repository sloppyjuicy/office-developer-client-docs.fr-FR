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
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782239"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Permet de convertir le nouveau **XLOPER12** l' ancienne **XLOPER**routine de conversion.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Paramètres

_pxloper12_ (**LPXLOPER12**)
  
Pointeur vers la source **XLOPER12** à convertir. 
  
_pxloper_ (**LPXLOPER**)
  
Pointeur vers la cible **XLOPER** contenant la valeur convertie. 
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

**TRUE** si la conversion a réussi, **FALSE** dans le cas contraire. 
  
## <a name="remarks"></a>Remarques

Selon le type de la **XLOPER12**, cette fonction alloue une nouvelle mémoire tampon pour les valeurs converties qui pointent sur la cible **XLOPER**. L’appelant est chargé de libérer la mémoire associée à la copie si la conversion est un succès ; **FreeXLOperT** peut être utilisé, ou elle peut être effectuée directement à l’aide de **libre**.
  
En cas d’échec de la conversion, l’appelant n’a pas besoin libérer de la mémoire.
  
Conversion d’un **XLOPER12** vers un **XLOPER** peut échouer lorsque le **XLOPER12** contient un tableau ou référence qui est trop grande ou une chaîne qui est trop longue pour le **XLOPER** contenir. 
  
**XLOPER12** Chaînes de caractères larges Unicode sont convertis en chaînes d’octets ASCII **XLOPER** dans un façon dépendant des paramètres régionaux. 
  
Le **XLOPER12** **xltypeInt** est un entier signé 32 bits, alors que le **XLOPER** **xltypeInt** est un nombre entier signé de 16 bits. Lorsqu’un entier **XLOPER12** fourni dépasse la limite d’un nombre entier **XLOPER** , l’entier est converti en un double de 8 octets et renvoyé dans un **XLOPER** de type **xltypeNum**. Il s’agit du seul cas dans lequel cette fonction modifie le type de la convertie **XLOPER**.
  
### <a name="example"></a>Exemple

Consultez le fichier `\SAMPLES\FRAMEWRK\FRAMEWRK.C` pour le code de cette fonction. 
  
## <a name="see-also"></a>Voir aussi

- [Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

