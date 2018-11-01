---
title: Après insertion, événement de macro
TOCTitle: After Insert Macro Event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 171c7b11db6fa79c6b69f3517abaddf052c96da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880725"
---
# <a name="after-insert-macro-event"></a>Après insertion, événement de macro


**S’applique à**: Access 2013, Office 2013

L'événement **Après insertion** se produit après l'ajout d'un enregistrement.


> [!NOTE]
> [!REMARQUE] L'événement **Après insertion** est disponible uniquement dans les macros de données.



## <a name="remarks"></a>Notes

Utilisez l'événement **Après insertion** pour effectuer toute action souhaitée lorsqu'un enregistrement est ajouté à une table. L'événement **Après insertion** peut par exemple servir à appliquer des règles professionnelles ou des flux de travail, à mettre à jour un total agrégé et à envoyer des notifications.

Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Après insertion**.

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
<td><p><a href="comment-macro-statement.md">Instruction de Macro commentaire</a></p></td>
</tr>
<tr class="even">
<td><p>Déroulement de programme</p></td>
<td><p><a href="group-macro-statement.md">Group, instruction de Macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Déroulement de programme</p></td>
<td><p><a href="if-then-else-macro-block.md">If... Procédez comme suit... Autre bloc de Macro</a></p></td>
</tr>
<tr class="even">
<td><p>Bloc de données</p></td>
<td><p><a href="createrecord-data-block.md">Action de Macro CréerEnregistrement</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloc de données</p></td>
<td><p><a href="editrecord-data-block.md">Action de Macro ModifierEnregistrement</a></p></td>
</tr>
<tr class="even">
<td><p>Bloc de données</p></td>
<td><p><a href="foreachrecord-data-block.md">Action de Macro PourChaqueEnregistrement</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloc de données</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord, bloc de données</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Action de Macro AnnulerModificationEnregistrement</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Action de Macro EffacerMacroErreur</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="deleterecord-macro-action.md">Action de Macro DeleteRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Action de Macro QuitterPourChaqueEnregistrement</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="logevent-macro-action.md">Action de Macro LogEvent</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="onerror-macro-action.md">Action de Macro SurErreur</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="raiseerror-macro-action.md">Action de Macro Déclenchererreur</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="rundatamacro-macro-action.md">Action de Macro ExécuterMacroDonnées</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="sendemail-macro-action.md">Action de Macro SendEmail</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="setfield-macro-action.md">Action de Macro SetField</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="setlocalvar-macro-action.md">Action de Macro DéfinirVarLocale</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="stopallmacros-macro-action.md">Action de Macro ArrêtToutesMacros</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="stopmacro-macro-action.md">Action de Macro ArrêtMacro</a></p></td>
</tr>
</tbody>
</table>


Pour créer une macro de données qui capture l'événement **Après insertion**, procédez comme suit.

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après insertion**.

2.  Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après insertion**.

Une macro de données vide s'affiche dans le concepteur de macros

## <a name="example"></a>Exemple

L'exemple de code suivant utilise l'événement **Après suppression** pour effectuer un traitement lorsqu'un enregistrement est ajouté à la table Donations. Lorsqu'un enregistrement est ajouté, le montant du don est ajouté au champ DonationsReceived dans la table Campaigns et au champ TotalDonatedField dans la table Donors.

**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le concepteurs de macros.**

Pour afficher cet exemple dans le concepteur de macros, procédez comme suit :

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après insertion**.

2.  Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après insertion**.

3.  Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.

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

<br/>

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
