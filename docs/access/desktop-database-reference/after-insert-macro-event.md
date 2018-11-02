---
title: After Insert, événement de macro
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
ms.openlocfilehash: 4dc9d509dedfb74769c84f44a6237b9f6354dc16
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921683"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="1998a-102">After Insert, événement de macro</span><span class="sxs-lookup"><span data-stu-id="1998a-102">After Insert macro event</span></span>


<span data-ttu-id="1998a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1998a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1998a-104">L'événement **Après insertion** se produit après l'ajout d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1998a-104">The **After Insert** event occurs after a record is added.</span></span>


> [!NOTE]
> <span data-ttu-id="1998a-105">[!REMARQUE] L'événement **Après insertion** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="1998a-105">The **After Insert** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="1998a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1998a-106">Remarks</span></span>

<span data-ttu-id="1998a-p101">Utilisez l'événement **Après insertion** pour effectuer toute action souhaitée lorsqu'un enregistrement est ajouté à une table. L'événement **Après insertion** peut par exemple servir à appliquer des règles professionnelles ou des flux de travail, à mettre à jour un total agrégé et à envoyer des notifications.</span><span class="sxs-lookup"><span data-stu-id="1998a-p101">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table. Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="1998a-p102">Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1998a-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="1998a-111">Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Après insertion**.</span><span class="sxs-lookup"><span data-stu-id="1998a-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1998a-112">Type de commande</span><span class="sxs-lookup"><span data-stu-id="1998a-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="1998a-113">Commande</span><span class="sxs-lookup"><span data-stu-id="1998a-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1998a-114">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="1998a-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="1998a-115"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-116">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="1998a-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="1998a-117"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-118">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="1998a-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="1998a-119"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-120">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="1998a-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1998a-121"><a href="createrecord-data-block.md">Action de macro CréerEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="1998a-121"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-122">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="1998a-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1998a-123"><a href="editrecord-data-block.md">Action de macro ModifierEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="1998a-123"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-124">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="1998a-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1998a-125"><a href="foreachrecord-data-block.md">Action de macro PourChaqueEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="1998a-125"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-126">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="1998a-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1998a-127"><a href="lookuprecord-data-block.md">Bloc de données RechercherEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="1998a-127"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-128">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-130">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-131"><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-132">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-133"><a href="deleterecord-macro-action.md">DeleteRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-134">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-136">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-137"><a href="logevent-macro-action.md">LogEvent, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-138">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-139"><a href="onerror-macro-action.md">OnError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-140">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-141"><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-142">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-143"><a href="rundatamacro-macro-action.md">RunDataMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-144">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-145"><a href="sendemail-macro-action.md">SendEmail, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-146">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-147"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-148">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-149"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1998a-150">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-151"><a href="stopallmacros-macro-action.md">StopAllMacros, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1998a-152">Action de données</span><span class="sxs-lookup"><span data-stu-id="1998a-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1998a-153"><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="1998a-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1998a-154">Pour créer une macro de données qui capture l'événement **Après insertion**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="1998a-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="1998a-155">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après insertion**.</span><span class="sxs-lookup"><span data-stu-id="1998a-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="1998a-156">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après insertion**.</span><span class="sxs-lookup"><span data-stu-id="1998a-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="1998a-157">Une macro de données vide s'affiche dans le concepteur de macros</span><span class="sxs-lookup"><span data-stu-id="1998a-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="1998a-158">Exemple</span><span class="sxs-lookup"><span data-stu-id="1998a-158">Example</span></span>

<span data-ttu-id="1998a-p103">L'exemple de code suivant utilise l'événement **Après suppression** pour effectuer un traitement lorsqu'un enregistrement est ajouté à la table Donations. Lorsqu'un enregistrement est ajouté, le montant du don est ajouté au champ DonationsReceived dans la table Campaigns et au champ TotalDonatedField dans la table Donors.</span><span class="sxs-lookup"><span data-stu-id="1998a-p103">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="1998a-161">**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le concepteurs de macros.**</span><span class="sxs-lookup"><span data-stu-id="1998a-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="1998a-162">Pour afficher cet exemple dans le concepteur de macros, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1998a-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="1998a-163">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après insertion**.</span><span class="sxs-lookup"><span data-stu-id="1998a-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="1998a-164">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après insertion**.</span><span class="sxs-lookup"><span data-stu-id="1998a-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="1998a-165">Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1998a-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="1998a-166">Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.</span><span class="sxs-lookup"><span data-stu-id="1998a-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
