---
title: Submacro, instruction de macro
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 722ec31b62f3a2e028fd076b52d6e526de8efca0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589091"
---
# <a name="submacro-macro-statement"></a>Submacro, instruction de macro

**S’applique à** : Access 2013, Office 2013

**L’instruction Submacro** définit une macro distincte dans la fenêtre Concepteur de macros.

## <a name="setting"></a>Paramètre

L’instruction **Submacro** utilise les arguments suivants.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatoire</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nom</p></td>
<td><p>Oui</p></td>
<td><p>Chaîne qui apparaît comme nom de la macro.</p></td>
</tr>
</tbody>
</table>


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
