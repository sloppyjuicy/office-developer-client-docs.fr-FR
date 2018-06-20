---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- fonction xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782224"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour retourner un handle pour les données enregistrées par la [fonction xlDefineBinaryName](xldefinebinaryname.md). Données avec un nom défini binaire sont enregistrées avec le classeur et est accessible par un nom à tout moment. Pour plus d’informations, voir « Binaire » nom Limitation d’étendue dans [Problèmes connus dans le développement de XLL Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Paramètres

_pxRes_ (**xltypeBigData** ou **xltypeErr**)
  
Structure Bigdata spécifiant que les données récupérées ou une erreur est les données n’a pas pu être récupéré ou le nom n’est pas défini. Lorsque la fonction retourne, le membre **hdata** de la **XLOPER**/ **XLOPER12** contient un handle pour les données nommées.  _pxRes_ doit être libéré dans un appel à **xlFree** n’est plus nécessaire. 
  
_pxName_ (**xltypeStr**)
  
Chaîne spécifiant le nom des données.
  
## <a name="remarks"></a>Remarques

Microsoft Excel possède le handle de mémoire retourné dans **hdata**. Dans Windows, le handle est le handle de mémoire globale (alloué par la fonction **GlobalAlloc** ). 
  
## <a name="see-also"></a>Voir aussi

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

