---
title: StopMacro, action de macro
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308497"
---
# <a name="stopmacro-macro-action"></a>StopMacro, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **ArrêterMacro** pour arrêter la macro en cours d’exécution.

## <a name="setting"></a>Paramètre

**L’action StopMacro** ne comprend aucun argument.

## <a name="remarks"></a>Remarques

Cette action est généralement utilisée lorsqu’une condition rend nécessaire l’arrêt de la macro. Vous pouvez utiliser une expression conditionnelle dans la ligne d'action de la macro contenant cette action. Lorsque l’expression est évaluée à **True** (–1), Microsoft Access arrête la macro.

Par exemple, vous pouvez créer une macro qui ouvre un formulaire affichant les totaux de commande quotidiens de la date entrée dans une boîte de dialogue personnalisée. Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle **Date** de commande de la boîte de dialogue contient une date valide. Si ce n’est pas le cas, l’action **MessageBox** peut afficher un message d’erreur et l’action **ArrêterMacro** peut arrêter la macro.

Si la macro a utilisé les actions **Écho** ou **SetWarnings** pour désactiver l’écho ou l’affichage des messages système, l’action **ArrêterMacro** les réensaie automatiquement.

Cette action n'est pas disponible dans les modules Visual Basic pour Applications (VBA).

## <a name="example"></a>Exemple

La macro suivante illustre l'utilisation de l'action **SurErreur**. Dans cet exemple, l'action **SurErreur** spécifie qu'Access exécute une macro de gestion des erreurs personnalisée nommée GestionnaireErreur lorsqu'une erreur se produit. Lorsqu’une erreur se produit, le sous-macro CatchErrors est appelé. Si le numéro d’erreur est 2102, un message spécifique s’affiche et l’exécution des macros est interrompue. Dans le cas contraire, un message décrivant l’erreur s’affiche et la macro est suspendue afin que vous pouvez effectuer un dépannage supplémentaire. Cette macro affiche une zone de message qui fait référence à l'objet **MacroError** pour afficher des informations sur l'erreur.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
