---
title: Fonctions de la DLL générique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll générique [excel 2007], fonctions, [Excel 2007], DLL générique
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782144"
---
# <a name="functions-in-the-generic-dll"></a>Fonctions de la DLL générique

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Le dossier `\EXAMPLES\GENERIC\` contient les fichiers de projet Microsoft Visual Studio et des fichiers de code source qui sont nécessaires pour compiler l’exemple de DLL GENERIC.xll. Vous pouvez utiliser ce projet comme modèle pour écrire vos propres solutions de XLL Microsoft Excel. Le code source dans ce projet illustre de nombreuses fonctionnalités de l’API C Excel. 
  
Lorsque vous chargez GENERIC.xll, il crée un nouveau menu **générique** avec quatre commandes : 
  
- **Boîte de dialogue** - affiche une boîte de dialogue Microsoft Excel. 
    
- **Danse** - déplace la sélection jusqu'à ce que vous appuyez sur la touche **ÉCHAP** . 
    
- **Boîte de dialogue native** - affiche une boîte de dialogue Windows. 
    
- **Exit** - GENERIC.xll décharge et supprime le menu **générique** . 
    
GENERIC.xll fournit également trois fonctions de feuille de calcul, Func1, FuncSum et FuncFib, qui peut être utilisé chaque fois que GENERIC.xll est chargé. GENERIC.xll peuvent être chargés à l’aide du Gestionnaire de compléments, ou elle est chargée si elle a été actif à la fin de la dernière session Excel normale.
  
Ce projet utilise la bibliothèque framework (FRMWRK32.lib).
  
## <a name="in-this-section"></a>Dans cette section

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

