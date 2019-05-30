---
title: Before Change, événement de macro
TOCTitle: Before Change macro event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a180068e805ae11883822ebf26f924e10d34bac5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538115"
---
# <a name="before-change-macro-event"></a>Before Change, événement de macro

**S’applique à** : Access 2013, Office 2013

L’événement **Avant la modification** se produit lorsqu’un enregistrement change, mais avant la validation de la modification.

> [!NOTE]
> L’événement **Avant la modification** est disponible uniquement dans les macros de données.

## <a name="remarks"></a>Remarques

Utilisez l’événement **Avant la modification** pour effectuer toute action souhaitée avant qu’un enregistrement soit modifié. **Avant la modification** s’utilise couramment pour effectuer une validation et pour déclencher des messages d’erreur personnalisés.

Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Utilisez la propriété **EstInsertion** pour déterminer si l'événement **Avant la modification** a été déclenché par la création d'un enregistrement ou par la modification d'un enregistrement existant. La propriété **EstInsertion** a la valeur **True** si l'événement a été déclenché par un nouvel enregistrement, **False** si l'événement a été déclenché par la modification d'un enregistrement existant.

L'exemple de code suivant illustre la syntaxe d'utilisation de la propriété **EstInsertion**.

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

Vous pouvez accéder à la valeur précédente dans un champ en utilisant la syntaxe suivante.

```vb
    [Old].[Field Name]
```

Par exemple, pour accéder à la valeur précédente du champ QuantityInStock, utilisez la syntaxe suivante.

```vb
    [Old].[QuantityInStock]
```

Les valeurs précédentes sont supprimées de manière définitive lorsque l'événement **Avant la modification** se termine.

Vous pouvez annuler l’événement **Avant la modification** à l’aide de l’action **DéclencherErreur**. Lorsqu’une erreur est levée, les modifications contenues dans l’événement **Avant la modification** sont ignorées.

Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Avant la modification**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de commande</p></th>
<th><p>Command</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Déroulement de programme</p></td>
<td><p><a href="comment-macro-statement.md">Comment, instruction de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Déroulement de programme</p></td>
<td><p><a href="group-macro-statement.md">Group, instruction de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Déroulement de programme</p></td>
<td><p><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Bloc de données</p></td>
<td><p><a href="lookuprecord-data-block.md">RechercherEnregistrement, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="onerror-macro-action.md">OnError, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="setfield-macro-action.md">SetField, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></p></td>
</tr>
</tbody>
</table>


Pour créer une macro de données qui capture l’événement **Avant la modification**, procédez comme suit :

1.  Ouvrez la table pour laquelle vous souhaitez capturer l’événement **Avant la modification**.

2.  Sous l’onglet **Table**, dans le groupe **Événements Avant**, cliquez sur **Avant la modification**.

Une macro de données vide s’affiche dans le concepteur de macros

## <a name="example"></a>Exemple

L’exemple de code suivant utilise l’événement **avant la modification** pour valider les champs d’État. Une erreur est levée si une valeur incorrecte est stockée dans le champ Resolution.

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

Pour afficher cet exemple dans le concepteur de macros, procédez comme suit.

1.  Ouvrez la table pour laquelle vous souhaitez capturer l’événement **Avant la modification**.

2.  Sous l’onglet **Table**, dans le groupe **Événements Avant**, cliquez sur **Avant la modification**.

3.  Sélectionnez le code dans l’exemple de code suivant, puis appuyez sur **Ctrl + C** pour le copier dans le presse-papiers.

4.  Activez la fenêtre du concepteur de macros, puis appuyez sur **Ctrl + V**.



```xml
<DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

L’exemple suivant montre comment utiliser l’action Déclenchererreur pour annuler l’événement de macro avant la modification des données. Lorsque le champ AffectéÀ est mis à jour, un bloc de données RechercherEnregistrement est utilisé pour déterminer si le technicien affecté est actuellement affecté à une demande de service ouverte. Si la valeur est true, l’événement avant la modification est annulé et l’enregistrement n’est pas mis à jour.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
