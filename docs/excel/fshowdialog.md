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
ms.localizationpriority: medium
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 69c4ba0fc535df6787683a42d49441f97c4bebe4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552247"
---
# <a name="fshowdialog"></a>fShowDialog

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l’utilisateur qui charge et affiche un exemple de boîte de dialogue Windows native. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Paramètres

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

