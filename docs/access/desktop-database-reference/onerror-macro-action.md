---
title: OnError, action de macro
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a9ff662ecd8c52c8caa8060e0c29a9a8f01440c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565239"
---
# <a name="onerror-macro-action"></a>OnError, action de macro

**S’applique à** : Access 2013, Office 2013

Utilisez l’action **SurErreur** pour indiquer ce qui doit se passer lorsqu’une erreur se produit dans une macro.

## <a name="setting"></a>Paramètre

L’action **SurErreur** possède les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Accédez à</p></td>
<td><p>Spécifie le comportement général lorsqu’une erreur se produit. Cliquez sur la flèche déroulante, puis sur l’un des paramètres suivants :</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Next</strong></p></td>
<td><p>Microsoft Office Access 2007 enregistre les détails de l’erreur dans l’objet <strong>MacroError</strong> mais n’arrête pas la macro. La macro passe à l’action suivante.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom macro</strong></p></td>
<td><p>Access arrête l’exécution de la macro active et exécute la macro dont le nom figure dans l’argument <strong>Nom de la macro</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Échec</strong></p></td>
<td><p>Access arrête l'exécution de la macro active et affiche un message d'erreur.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Nom macro</p></td>
<td><p>Si l’argument Aller à est définie sur Nom de macro, tapez le nom de la macro à utiliser pour la gestion des erreurs. Le nom que vous tapez doit correspondre à un nom dans la <strong>colonne Nom</strong> de macro de la macro en cours ; vous ne pouvez pas entrer le nom d’un autre objet macro. Dans l’exemple ci-dessous, la macro <strong>ErrorHandler</strong> est contenue dans le même objet macro que l’action <strong>OnError.</strong> Cet argument doit rester vide si l’argument Atteindre est défini sur <strong>Suivant</strong> ou sur <strong>Échec</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

- L’action **SurErreur** est généralement placée au début d’une macro, mais vous pouvez également la placer plus loin dans la macro. Les règles établies par cette action prendront effet dès exécution de l’action.

- Si vous définissez l'argument Atteindre sur **Échec**, Access se comporte de la même manière que si la macro ne contenait pas d'action **SurErreur**. Autrement dit, si une erreur se produit, Access arrête la macro et affiche un message d'erreur standard. Le paramètre **Échec** est principalement utilisé pour désactiver la gestion des erreurs établie précédemment dans une macro.

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
