---
title: StopMacro Macro Action
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a918fd128456450c21b5a36e74b7266df661cb75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470797"
---
# <a name="stopmacro-macro-action"></a>StopMacro Macro Action

**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l’action **ArrêtMacro** pour arrêter la macro en cours d’exécution.

## <a name="setting"></a>Paramètre

L’action **ArrêtMacro** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Vous utilisez généralement cette action quand une condition rend nécessaire pour arrêter la macro. Vous pouvez utiliser une expression conditionnelle dans la ligne d'action de la macro contenant cette action. Lorsque l’expression a la valeur **True** (– 1), Microsoft Access arrête la macro.

Par exemple, vous pouvez créer une macro qui ouvre un formulaire affichant les totaux de la commande quotidienne pour la date entrée dans la boîte de dialogue personnalisée. Vous pouvez utiliser une expression conditionnelle pour vous assurer que le contrôle de **Date de la commande** dans la boîte de dialogue contient une date valide. Le cas contraire, l’action de **contrôle zonemessage** peut afficher un message d’erreur et l’action **ArrêtMacro** arrêter la macro.

Si la macro a utilisé les actions **écho** ou **avertissements** pour désactiver l’écho ou l’affichage des messages système, l’action **ArrêtMacro** automatiquement réactive les.

Cette action n'est pas disponible dans les modules Visual Basic pour Applications (VBA).

## <a name="example"></a>Exemple

La macro suivante illustre l'utilisation de l'action **SurErreur**. Dans cet exemple, l'action **SurErreur** spécifie qu'Access exécute une macro de gestion des erreurs personnalisée nommée GestionnaireErreur lorsqu'une erreur se produit. Lorsqu’une erreur se produit, le submacro CatchErrors est appelée. Si le numéro d’erreur est 2102, un message s’affiche et l’exécution de la macro est interrompue. Sinon, un message décrivant l’erreur s’affiche et la macro est interrompue de sorte que vous pouvez effectuer des opérations de dépannage. Cette macro affiche une zone de message qui fait référence à l'objet **MacroError** pour afficher des informations sur l'erreur.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
