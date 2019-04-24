---
title: Fonctions dans le fichier DLL générique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll générique [Excel 2007], fonctions, fonctions [Excel 2007], DLL générique
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304087"
---
# <a name="functions-in-the-generic-dll"></a>Fonctions dans le fichier DLL générique

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Le dossier `\EXAMPLES\GENERIC\` contient les fichiers de projet Microsoft Visual Studio et les fichiers de code source nécessaires à la compilation de l'exemple de dll Generic. XLL. Vous pouvez utiliser ce projet comme modèle pour écrire vos propres XLL Microsoft Excel. Le code source de ce projet illustre de nombreuses fonctionnalités de l'API C Excel. 
  
Lorsque vous chargez GENERIC. xll, il crée un menu **générique** avec quatre commandes: 
  
- **Boîte de dialogue** -affiche une boîte de dialogue Microsoft Excel. 
    
- **Danse** : déplace la sélection jusqu'à ce que vous appuyiez sur la touche **Échap** . 
    
- **Boîte de dialogue Native** : affiche une boîte de dialogue Windows. 
    
- **Exit** -décharge Generic. XLL et supprime le menu **générique** . 
    
GENERIC. xll fournit également trois fonctions de feuille de calcul, func1, FuncSum et FuncFib, qui peuvent être utilisées chaque fois que GENERIC. xll est chargé. GENERIC. xll peut être chargé à l'aide du gestionnaire de compléments ou il est chargé s'il était actif à l'extrémité normale de la dernière session Excel.
  
Ce projet utilise la bibliothèque d'infrastructure (FRMWRK32. lib).
  
## <a name="in-this-section"></a>Contenu de cette section

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

