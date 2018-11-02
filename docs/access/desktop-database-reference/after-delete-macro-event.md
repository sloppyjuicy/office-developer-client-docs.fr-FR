---
title: After Delete, événement de macro
TOCTitle: After Delete macro event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 943f16c5bb1f1525c8da36938fa6beb2e6f71444
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929796"
---
# <a name="after-delete-macro-event"></a>After Delete, événement de macro


**S’applique à**: Access 2013, Office 2013

L'événement **Après suppression** se produit après la suppression d'un enregistrement.


> [!NOTE]
> [!REMARQUE] L'événement **Après suppression** est disponible uniquement dans les macros de données.



## <a name="remarks"></a>Notes

Utilisez l'événement **Après suppression** pour effectuer toute action souhaitée lors de la suppression d'un enregistrement. L'événement **Après suppression** peut par exemple servir à appliquer des règles professionnelles ou des flux de travail, à mettre à jour un total agrégé et à envoyer des notifications.

Lorsque l'événement **Après suppression** se produit, les valeurs contenues dans l'enregistrement supprimé sont toujours disponibles. Vous souhaiterez peut-être utiliser une valeur supprimée pour incrémenter ou décrémenter un total, créer un journal d’audit ou comparer à une valeur existante dans un argument *ConditionWhere* .

Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction If pour déterminer si le champ PaidInFull a été modifié.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Vous pouvez accéder à une valeur dans l'enregistrement supprimé en utilisant la syntaxe suivante.

`[Old].[Field Name]`

Par exemple, pour accéder à la valeur du champ QuantityInStock dans l'enregistrement supprimé, utilisez la syntaxe suivante.

`[Old].[QuantityInStock]`

Les valeurs contenues dans l'enregistrement supprimé sont supprimées de manière définitive lorsque l'événement **Après suppression** se termine.

Les commandes suivantes de la macro peuvent être utilisées dans l’événement **Après suppression** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de commande</p></th>
<th><p>Commande</p></th>
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
<td><p><a href="createrecord-data-block.md">Action de macro CréerEnregistrement</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloc de données</p></td>
<td><p><a href="editrecord-data-block.md">Action de macro ModifierEnregistrement</a></p></td>
</tr>
<tr class="even">
<td><p>Bloc de données</p></td>
<td><p><a href="foreachrecord-data-block.md">Action de macro PourChaqueEnregistrement</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloc de données</p></td>
<td><p><a href="lookuprecord-data-block.md">Bloc de données RechercherEnregistrement</a></p></td>
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


Pour créer une macro de données qui capture l'événement **Après suppression**, procédez comme suit.

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après suppression**.

2.  Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après suppression**.

Une macro de données vide s'affiche dans le concepteur de macros.

## <a name="example"></a>Exemple

L'exemple de code suivant utilise l'événement **Après suppression** pour effectuer un traitement lorsqu'un enregistrement est supprimé de la table Donations. Lorsqu'un enregistrement est supprimé, le montant d'un don est soustrait du champ DonationsReceived dans la table DonationsReceived et du champ TotalDonatedField dans la table Donors.

**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le concepteurs de macros.**

Pour afficher cet exemple dans le concepteur de macros, procédez comme suit.

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après suppression**.

2.  Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après suppression**.

3.  Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.

4.  Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterDelete"> 
        <Statements> 
          <Comment>Initialize a variable and assign the old</Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Old].[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Old].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Collapsed="true" Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Old].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
```

<br/>

```vb
    SetLocalVar 
                    Name    varAmount 
              Expression   =[Old].[Amount] 
     
    If   Not(IsNull([Old].[CampaignID]]))   Then 
     
         For Each Record In     Campaigns 
            Where Condition     =[ID]=[Old].[CampaignID] 
                      Alias 
            EditRecord 
                      Alias 
                  SetField   ([DonationsReceived], [DonationsReceived] - [varAmount]) 
            End EditRecord 
     
    End If 
     
    If   Not(IsNull([Old].[DonorID]]))   Then 
     
         For Each Record In    Donors 
            Where Condition     =[ID]=[Old].[DonorID] 
                      Alias 
            EditRecord 
                      Alias 
     
              SetField 
                             Name   [TotalDonated] 
                            Value   =[TotalDonated]-[varAmount] 
            End EditRecord 
    End If
```
