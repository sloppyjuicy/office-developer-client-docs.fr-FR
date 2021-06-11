---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fonction fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433590"
---
# <a name="fshowdialog"></a>fShowDialog

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l’utilisateur qui charge et affiche un exemple de boîte de dialogue Windows native. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parameters

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction retourne l’integer zéro pour indiquer l’achèvement réussi
  
## <a name="remarks"></a>Remarques

Les étapes d’affichage de la boîte Windows dialogue native sont les suivantes :
  
1. Obtenez le Microsoft Excel principal Windows à **l’aide de GetHwnd**.
    
2. Hook the Excel main window using **HookExcelWindow**.
    
3. Afficher la boîte de dialogue à l’aide **de DialogBox**.
    
4. Unhook the Excel main window using **UnhookExcelWindow**.
    
### <a name="example"></a>Exemple

Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

