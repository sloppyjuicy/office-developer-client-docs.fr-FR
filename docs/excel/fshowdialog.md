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
ms.openlocfilehash: f1afb592448978c230ccc2eb2a3b9a57fb274c55
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198897"
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

Les étapes à suivre pour afficher la boîte de Windows de dialogue native sont les suivantes :
  
1. Obtenez le Microsoft Excel principal Windows à **l’aide de GetHwnd**.
    
2. Hook the Excel main window using **HookExcelWindow**.
    
3. Afficher la boîte de dialogue à l’aide **de DialogBox**.
    
4. Unhook the Excel main window using **UnhookExcelWindow**.
    
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

