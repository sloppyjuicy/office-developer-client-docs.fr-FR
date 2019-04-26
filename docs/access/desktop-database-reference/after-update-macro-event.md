---
title: After Update, événement de macro
TOCTitle: After Update macro event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a96b46fcc78c4f93887e487f52091a77da6c0d2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297185"
---
# <a name="after-update-macro-event"></a>After Update, événement de macro

**S’applique à** : Access 2013, Office 2013

L'événement **Après MAJ** se produit après la modification d'un enregistrement.

> [!NOTE]
> L’événement **Après MAJ** est disponible uniquement dans les macros de données.

## <a name="remarks"></a>Remarques

Utilisez l’événement **Après MAJ** pour effectuer toute action souhaitée lorsqu’un enregistrement est modifié. L’événement **Après MAJ** peut par exemple servir à appliquer des règles professionnelles, à mettre à jour un total agrégé et à envoyer des notifications.

Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Vous pouvez accéder à la valeur précédente dans un champ en utilisant la syntaxe suivante.

`[Old].[Field Name]`

Par exemple, pour accéder à la valeur précédente du champ QuantityInStock, utilisez la syntaxe suivante.

`[Old].[QuantityInStock]`

Les valeurs précédentes sont supprimées de manière définitive lorsque l'événement **Après MAJ** se termine.

Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Après MAJ**.

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
<td><p><a href="createrecord-data-block.md">CreateRecord, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloc de données</p></td>
<td><p><a href="editrecord-data-block.md">EditRecord, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Bloc de données</p></td>
<td><p><a href="foreachrecord-data-block.md">ForEachRecord, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloc de données</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord, bloc de données</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="deleterecord-macro-action.md">DeleteRecord, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">ExitForEachRecord, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="logevent-macro-action.md">LogEvent, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="onerror-macro-action.md">OnError, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="rundatamacro-macro-action.md">RunDataMacro, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="sendemail-macro-action.md">SendEmail, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="setfield-macro-action.md">SetField, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="stopallmacros-macro-action.md">StopAllMacros, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></p></td>
</tr>
</tbody>
</table>


Pour créer une macro de données qui capture l'événement **Après MAJ**, procédez comme suit :

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après MAJ**.

2.  Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après MAJ**.

Une macro de données vide s’affiche dans le concepteur de macros

## <a name="example"></a>Exemple

L’exemple de code suivant utilise l’événement **Après MAJ** pour exécuter une macro de données nommée qui ajoute un enregistrement à la table Comment chaque fois que l’état d’un problème est mis à jour.

**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le Concepteur de macros.**

Pour afficher cet exemple dans le concepteur de macros, procédez comme suit :

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après MAJ**.

2.  Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après MAJ**.

3.  Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.

4.  Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.

<!-- end list -->

```xml
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterUpdate"> 
        <Statements> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Status")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Status changed to &quot; &amp; [Status]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Resolution")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Issue resolved as &quot; &amp; [Resolution]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
``` 

<br/>

```vb
If  Updated("Status")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
         prmComment   ="--Status Changes to "&[Status] 
          prmUserID   =[ChangedByUserID] 
End If 
 
If   Updated("Resolution")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
          prmUserID   =[ChangedByUserID] 
         prmComment   ="--Issue Resolved as "&[Status] 
End If 
```

