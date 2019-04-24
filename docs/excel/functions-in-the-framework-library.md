---
title: Fonctions dans la bibliothèque d'infrastructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions de la bibliothèque d'infrastructure [Excel 2007], fonctions [Excel 2007], bibliothèque de l'infrastructure
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304052"
---
# <a name="functions-in-the-framework-library"></a>Fonctions dans la bibliothèque d'infrastructure

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
La bibliothèque d'infrastructure a été créée pour faciliter l'écriture de XLL. Il inclut des fonctions simples pour ****/ la gestion de la mémoire de**XLOPER12** , la création d'une méthode **XLOPER**/ **** temporaire, qui appelle de façon fiable les fonctions de rappel Microsoft Excel (**Excel4**, **Excel4v** , * * Excel12 * *, * * Excel12v * *) et l'impression de chaînes de débogage sur un terminal attaché.
  
Les fonctions incluses dans cette bibliothèque permettent de simplifier une partie de code ressemblant à ce qui suit.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Le code simplifié ressemble à l'exemple suivant.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

Les fonctions suivantes sont incluses dans la bibliothèque d'infrastructure:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Fonctions utilisées avec XLOPER**|**Fonctions utilisées avec Xloper12**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[Revenue](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
L'utilisation de ces fonctions réduit le temps nécessaire à l'écriture d'une DLL ou d'une XLL. Le démarrage du développement à partir de l'exemple d'application générique réduit également le temps de développement. Utilisez GENERIC. C en tant que modèle pour vous aider à configurer l'infrastructure d'un XLL, puis remplacez le code existant par le vôtre.
  
Les fonctions de la bibliothèque **XLOPER**/ **** temporaire créent des valeurs **XLOPER**/ de**XLOPER12** à l'aide de la mémoire d'un tas local géré par la bibliothèque d'infrastructure. / Les **** valeurs de la**XLOPER12 XLOPER12** restent valides jusqu'à ce que vous appeliez la fonction **FreeAllTempMemory** ou l'une des fonctions **Excel** ou **Excel12f** . (Les fonctions **Excel** et **Excel12f** libèrent toutes les mémoires temporaires avant de renvoyer.) 
  
Pour utiliser les fonctions de la bibliothèque d'infrastructure, vous devez inclure le FRAMEWRK. H dans votre code C et ajoutez FRAMEWRK. C ou FRMWRK32. LIB dans votre projet de code.
  
## <a name="see-also"></a>Voir aussi

- [R�f�rence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)

