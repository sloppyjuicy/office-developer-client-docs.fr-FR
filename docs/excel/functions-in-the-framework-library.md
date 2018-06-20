---
title: Fonctions de la bibliothèque Framework
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions de la bibliothèque Framework [excel 2007], fonctions [Excel 2007], bibliothèque Framework
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782139"
---
# <a name="functions-in-the-framework-library"></a>Fonctions de la bibliothèque Framework

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
La bibliothèque Framework a été créée pour faciliter l’écriture de XLL plus faciles. Il inclut des fonctions de gestion **XLOPER**simples/ mémoire**XLOPER12** , création temporaire **XLOPER**/ **XLOPER12**, stricte appeler les fonctions de rappel de Microsoft Excel (**Excel 4**, **Excel4v** ** Excel12 **, ** Excel12v **) et l’impression de débogage des chaînes dans un terminal attaché.
  
Les fonctions incluses dans cette bibliothèque de simplifier un morceau de code qui se présente comme suit.
  
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

Les fonctions suivantes sont incluses dans la bibliothèque Framework :
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Fonctions utilisées avec XLOPER**|**Fonctions utilisées avec XLOPER12s**|
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
   
Utilisation de ces fonctions réduit la quantité de temps nécessaire pour écrire une DLL ou XLL. Démarrer le développement de l’application exemple générique réduit également le temps de développement. Utilisez générique. C en tant que modèle pour aider à configurer le cadre d’une solution XLL et remplacez le code existant avec vos propres.
  
Le temporaire **XLOPER**/ fonctions**XLOPER12** créent **XLOPER**/ **XLOPER12** valeurs à l’aide de la mémoire à partir d’un segment de mémoire local géré par la bibliothèque de Framework. Le **XLOPER**/ **XLOPER12** valeurs restent valides jusqu'à ce que vous appelez la fonction **FreeAllTempMemory** ou une des fonctions **Excel** ou **Excel12f** . (Les fonctions **Excel** et **Excel12f** gratuit toute la mémoire temporaire avant de retourner). 
  
Pour utiliser les fonctions de bibliothèque Framework, vous devez inclure le FRAMEWRK. H du fichier dans votre code C et ajoutez le FRAMEWRK. C ou FRMWRK32. Fichiers LIB à votre projet de code.
  
## <a name="see-also"></a>Voir aussi

- [R�f�rence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)

