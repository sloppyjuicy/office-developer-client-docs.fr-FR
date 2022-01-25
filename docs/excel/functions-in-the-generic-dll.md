---
title: Fonctions dans le fichier DLL générique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
ms.localizationpriority: medium
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
ms.openlocfilehash: a255eac7d7c84313d8d958aa85369dd1fc7f27aa
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199583"
---
# <a name="functions-in-the-generic-dll"></a>Fonctions dans le fichier DLL générique

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Le dossier contient les Microsoft Visual Studio de projet et les fichiers de code source nécessaires pour compiler l’exemple `\EXAMPLES\GENERIC\` DLL GENERIC.xll. Vous pouvez utiliser ce projet comme modèle pour écrire votre propre Microsoft Excel XL. Le code source de ce projet illustre de nombreuses fonctionnalités de l’API Excel C. 
  
Lorsque vous chargez GENERIC.xll, il crée un menu **générique** avec quatre commandes : 
  
- **Boîte** de dialogue : affiche une boîte Microsoft Excel dialogue. 
    
- **Dépôt** : déplace la sélection jusqu’à ce que vous appuyiez sur la **touche ÉCHAP.** 
    
- **Boîte de dialogue** native : affiche une boîte Windows dialogue. 
    
- **Exit** : décharge GENERIC.xll et supprime le menu **générique.** 
    
GENERIC.xll fournit également trois fonctions de feuille de calcul, Func1, FuncSum et FuncFib, qui peuvent être utilisées chaque fois que GENERIC.xll est chargé. GENERIC.xll peut être chargé à l’aide du Gestionnaire de Excel.
  
Ce projet utilise la bibliothèque d’infrastructure (FRMWRK32.lib).
  
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

