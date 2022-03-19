---
title: After Insert, événement macro
TOCTitle: After Insert macro event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: a6e53c52a22b87d48aa0e2317d8f865db7762114
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629320"
---
# <a name="after-insert-macro-event"></a>After Insert, événement macro

**S’applique à** : Access 2013, Office 2013

L'événement **AfterInsert** se produit après l'ajout d'un nouvel enregistrement.

> [!NOTE]
> Le **après insérer** événement est disponible uniquement dans les Macros de données.

## <a name="remarks"></a>Remarques

Utilisez le **après insérer** événement effectuez les actions que vous voulez se produisent lors de l’ajout d’un enregistrement à une table. Utilisations courantes pour la **après insérer** incluent l’application des règles métier, flux de travail, la mise à jour une agrégation total et envoi de notifications.

Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Le tableau suivant répertorie les commandes de macro qui peuvent être utilisées dans la **après insérer** événement.

<table>
<colgroup>
<col />
<col />
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
<td><p>Flux de programme</p></td>
<td><p><a href="group-macro-statement.md">Group, instruction de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Flux de programme</p></td>
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


Pour créer une macro de données qui capture les **après insérer** événement, procédez comme suit.

1.  Ouvrez la table pour laquelle vous voulez capturer la **après insérer** événement.

2.  Sur la **tableau** sous l’onglet le **après les événements** groupe, cliquez sur **après insérer**.

Une macro de données vide s’affiche dans le Concepteur de macros.

## <a name="example"></a>Exemple

Le code suivant exemple utilise la **après insérer** événement pour effectuer certaines traitement quand un enregistrement est ajouté à la table Donations. Lors de l’ajout d’un enregistrement, la quantité du don figure dans le champ DonationsReceived dans le tableau campagnes et TotalDonatedField dans la table de donateurs.

**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le Concepteur de macros.**

Pour consulter cet exemple dans le Concepteur de macros, procédez comme suit :

1.  Ouvrez la table pour laquelle vous voulez capturer la **après insérer** événement.

2.  Sur la **tableau** sous l’onglet le **après les événements** groupe, cliquez sur **après insérer**.

3.  Sélectionnez le code dans l’exemple de code suivant et appuyez sur CTRL + C pour copier dans le Presse-papiers.

4.  Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.

<!-- end list -->

```xml
    <DataMacros> 
      <DataMacro Event="AfterInsert"> 
        <Statements> 
          <Comment>This data macro increments the DonationsReceived field in Campaigns and theAmountCollected field in Pledges </Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Donations].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]+[varAmount]</Argument> 
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
              <Condition>Not (IsNull([DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Donations].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]+[varAmount]</Argument> 
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


```vb
    SetLocalVar 
                  Name   varAmount 
            Expression   =[Amount] 
     
    If   Not (IsNull([CampaignID]))   Then 
     
         For Each Record In   Campaigns 
            Where Condition   =[ID]=[Donations].[CampaignID] 
                      Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [DonationsReceived] 
                                Value   =[DonationsReceived]+[varAmount] 
                End EditRecord 
    End If 
     
    If   Not (IsNull([DonorID]))   Then 
     
         For Each Record In  Donors 
            WhereCondition   =[ID]=[Donations].[DonorID] 
                     Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [TotalDonated] 
                                Value   =[TotalDonated]+[varAmount] 
                 End EditRecord 
    End If
```
