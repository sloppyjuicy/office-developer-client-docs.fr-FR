---
title: Fonctions dans la bibliothèque d’infrastructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417545"
---
# <a name="functions-in-the-framework-library"></a>Fonctions dans la bibliothèque d’infrastructure

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
La bibliothèque Framework a été créée pour faciliter l’écriture de XL. Il inclut des fonctions simples pour la gestion de la mémoire **XLOPER** XLOPER12, la création temporaire de XLOPER XLOPER12 , l’appel robuste des fonctions de rappel /   Microsoft Excel  /  (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) et l’impression de chaînes de débogage sur un terminal attaché.
  
Les fonctions incluses dans cette bibliothèque facilitent la simplification d’un élément de code qui ressemble à ce qui suit.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Le code simplifié ressemble à l’exemple suivant.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

Les fonctions suivantes sont incluses dans la bibliothèque Framework :
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Fonctions utilisées avec xlOPERs**|**Fonctions utilisées avec XLOPER12s**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
L’utilisation de ces fonctions réduit le temps nécessaire à l’écriture d’une DLL ou d’une XLL. Le démarrage du développement à partir de l’exemple d’application GENERIC raccourcit également le temps de développement. Utilisez GENERIC. C en tant que modèle pour vous aider à configurer l’infrastructure d’une XLL, puis à remplacer le code existant par le vôtre.
  
Les fonctions **XLOPER** /  **XLOPER12** temporaires créent des valeurs  /  **XLOPER XLOPER12** à l’aide de la mémoire d’un tas local géré par la bibliothèque Framework. Les **valeurs XLOPER** XLOPER12 restent valides jusqu’à ce que vous appeliez la fonction /   **FreeAllTempMemory** ou l’une des fonctions **Excel** **ou Excel12f.** (Les **fonctions Excel** et **Excel12f** libèrent toute la mémoire temporaire avant de revenir.) 
  
Pour utiliser les fonctions de la bibliothèque Framework, vous devez inclure FRAMEWRK. Fichier H dans votre code C et ajoutez frameWRK. C ou FRMWRK32. Fichiers LIB dans votre projet de code.
  
## <a name="see-also"></a>Voir aussi

- [Référence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)

