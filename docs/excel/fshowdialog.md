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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782135"
---
# <a name="fshowdialog"></a>fShowDialog

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple définies par l’utilisateur de commande qui charge et affiche une boîte de dialogue Windows native exemple. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La fonction retour entier entre zéro pour indiquer la réussite de l’opération
  
## <a name="remarks"></a>Remarques

Les étapes pour afficher la boîte de dialogue Windows native sont les suivantes :
  
1. Obtenir le handle Windows principal Microsoft Excel à l’aide de **GetHwnd**.
    
2. Connecter la fenêtre principale de Excel à l’aide de **HookExcelWindow**.
    
3. Afficher la boîte de dialogue à l’aide de **DialogBox**.
    
4. Décrocher la fenêtre principale de Excel à l’aide de **UnhookExcelWindow**.
    
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

