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
localization_priority: Priority
ms.openlocfilehash: c84a737d08b791bfe560bfe6af6bcc59a14d2678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297220"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="2e361-102">After Insert, événement macro</span><span class="sxs-lookup"><span data-stu-id="2e361-102">After Insert macro event</span></span>

<span data-ttu-id="2e361-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e361-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e361-104">L'événement **AfterInsert** se produit après l'ajout d'un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2e361-104">The **After Insert** event occurs after a record is added.</span></span>

> [!NOTE]
> <span data-ttu-id="2e361-105">Le **après insérer** événement est disponible uniquement dans les Macros de données.</span><span class="sxs-lookup"><span data-stu-id="2e361-105">The **After Insert** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e361-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e361-106">Remarks</span></span>

<span data-ttu-id="2e361-p101">Utilisez le **après insérer** événement effectuez les actions que vous voulez se produisent lors de l’ajout d’un enregistrement à une table. Utilisations courantes pour la **après insérer** incluent l’application des règles métier, flux de travail, la mise à jour une agrégation total et envoi de notifications.</span><span class="sxs-lookup"><span data-stu-id="2e361-p101">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table. Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="2e361-109">Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé.</span><span class="sxs-lookup"><span data-stu-id="2e361-109">You can use the *Updated("**Field Name**")* function to determine whether a field has changed.</span></span> <span data-ttu-id="2e361-110">L’exemple de code suivant montre comment utiliser un **si** instruction à déterminer déterminer si le champ PaidInFull a été modifié.</span><span class="sxs-lookup"><span data-stu-id="2e361-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="2e361-111">Le tableau suivant répertorie les commandes de macro qui peuvent être utilisées dans la**après insérer** événement.</span><span class="sxs-lookup"><span data-stu-id="2e361-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e361-112">Type de commande</span><span class="sxs-lookup"><span data-stu-id="2e361-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="2e361-113">Commande</span><span class="sxs-lookup"><span data-stu-id="2e361-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e361-114">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="2e361-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2e361-115"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-116">Flux de programme</span><span class="sxs-lookup"><span data-stu-id="2e361-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2e361-117"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-118">Flux de programme</span><span class="sxs-lookup"><span data-stu-id="2e361-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2e361-119"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-120">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="2e361-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2e361-121"><a href="createrecord-data-block.md">CreateRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-121"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-122">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="2e361-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2e361-123"><a href="editrecord-data-block.md">EditRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-123"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-124">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="2e361-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2e361-125"><a href="foreachrecord-data-block.md">ForEachRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-125"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-126">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="2e361-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2e361-127"><a href="lookuprecord-data-block.md">LookupRecord, bloc de données</a></span><span class="sxs-lookup"><span data-stu-id="2e361-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-128">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-130">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-131"><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-132">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-133"><a href="deleterecord-macro-action.md">DeleteRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-134">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-136">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-137"><a href="logevent-macro-action.md">LogEvent, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-138">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-139"><a href="onerror-macro-action.md">OnError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-140">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-141"><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-142">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-143"><a href="rundatamacro-macro-action.md">RunDataMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-144">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-145"><a href="sendemail-macro-action.md">SendEmail, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-146">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-147"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-148">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-149"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e361-150">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-151"><a href="stopallmacros-macro-action.md">StopAllMacros, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e361-152">Action de données</span><span class="sxs-lookup"><span data-stu-id="2e361-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2e361-153"><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="2e361-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2e361-154">Pour créer une macro de données qui capture les **après insérer** événement, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="2e361-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="2e361-155">Ouvrez la table pour laquelle vous voulez capturer la **après insérer** événement.</span><span class="sxs-lookup"><span data-stu-id="2e361-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="2e361-156">Sur la **tableau** sous l’onglet le **après les événements** groupe, cliquez sur **après insérer**.</span><span class="sxs-lookup"><span data-stu-id="2e361-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="2e361-157">Une macro de données vide s’affiche dans le Concepteur de macros.</span><span class="sxs-lookup"><span data-stu-id="2e361-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="2e361-158">Exemple</span><span class="sxs-lookup"><span data-stu-id="2e361-158">Example</span></span>

<span data-ttu-id="2e361-p103">Le code suivant exemple utilise la **après insérer** événement pour effectuer certaines traitement quand un enregistrement est ajouté à la table Donations. Lors de l’ajout d’un enregistrement, la quantité du don figure dans le champ DonationsReceived dans le tableau campagnes et TotalDonatedField dans la table de donateurs.</span><span class="sxs-lookup"><span data-stu-id="2e361-p103">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="2e361-161">**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le Concepteur de macros.**</span><span class="sxs-lookup"><span data-stu-id="2e361-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="2e361-162">Pour consulter cet exemple dans le Concepteur de macros, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2e361-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="2e361-163">Ouvrez la table pour laquelle vous voulez capturer la **après insérer** événement.</span><span class="sxs-lookup"><span data-stu-id="2e361-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="2e361-164">Sur la **tableau** sous l’onglet le **après les événements** groupe, cliquez sur **après insérer**.</span><span class="sxs-lookup"><span data-stu-id="2e361-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="2e361-165">Sélectionnez le code dans l’exemple de code suivant et appuyez sur CTRL + C pour copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="2e361-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="2e361-166">Activer la fenêtre Concepteur de macro, puis appuyez sur CTRL + V.</span><span class="sxs-lookup"><span data-stu-id="2e361-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
