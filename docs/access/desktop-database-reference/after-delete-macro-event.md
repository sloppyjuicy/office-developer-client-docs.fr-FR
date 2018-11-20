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
ms.openlocfilehash: 8f72083201fefffc5dfff4627cd3b54c1449e083
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026056"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="ad956-102">After Delete, événement de macro</span><span class="sxs-lookup"><span data-stu-id="ad956-102">After Delete macro event</span></span>

<span data-ttu-id="ad956-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad956-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad956-104">L'événement **Après suppression** se produit après la suppression d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ad956-104">The **After Delete** event occurs after a record is deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="ad956-105">[!REMARQUE] L'événement **Après suppression** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="ad956-105">The **After Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad956-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ad956-106">Remarks</span></span>

<span data-ttu-id="ad956-p101">Utilisez l'événement **Après suppression** pour effectuer toute action souhaitée lors de la suppression d'un enregistrement. L'événement **Après suppression** peut par exemple servir à appliquer des règles professionnelles ou des flux de travail, à mettre à jour un total agrégé et à envoyer des notifications.</span><span class="sxs-lookup"><span data-stu-id="ad956-p101">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted. Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="ad956-109">Lorsque l'événement **Après suppression** se produit, les valeurs contenues dans l'enregistrement supprimé sont toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="ad956-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="ad956-110">Vous souhaiterez peut-être utiliser une valeur supprimée pour incrémenter ou décrémenter un total, créer un journal d’audit ou comparer à une valeur existante dans un argument *ConditionWhere* .</span><span class="sxs-lookup"><span data-stu-id="ad956-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="ad956-p103">Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction If pour déterminer si le champ PaidInFull a été modifié.</span><span class="sxs-lookup"><span data-stu-id="ad956-p103">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="ad956-113">Vous pouvez accéder à une valeur dans l'enregistrement supprimé en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="ad956-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="ad956-114">Par exemple, pour accéder à la valeur du champ QuantityInStock dans l'enregistrement supprimé, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="ad956-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="ad956-115">Les valeurs contenues dans l'enregistrement supprimé sont supprimées de manière définitive lorsque l'événement **Après suppression** se termine.</span><span class="sxs-lookup"><span data-stu-id="ad956-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="ad956-116">Les commandes suivantes de la macro peuvent être utilisées dans l’événement **Après suppression** .</span><span class="sxs-lookup"><span data-stu-id="ad956-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad956-117">Type de commande</span><span class="sxs-lookup"><span data-stu-id="ad956-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="ad956-118">Commande</span><span class="sxs-lookup"><span data-stu-id="ad956-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad956-119">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="ad956-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="ad956-120"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-120"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-121">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="ad956-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="ad956-122"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-122"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-123">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="ad956-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="ad956-124"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-124"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-125">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="ad956-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="ad956-126"><a href="createrecord-data-block.md">Action de macro CréerEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="ad956-126"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-127">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="ad956-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="ad956-128"><a href="editrecord-data-block.md">Action de macro ModifierEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="ad956-128"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-129">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="ad956-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="ad956-130"><a href="foreachrecord-data-block.md">Action de macro PourChaqueEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="ad956-130"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-131">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="ad956-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="ad956-132"><a href="lookuprecord-data-block.md">Bloc de données RechercherEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="ad956-132"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-133">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-135">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-136"><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-136"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-137">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-138"><a href="deleterecord-macro-action.md">DeleteRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-138"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-139">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-141">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-142"><a href="logevent-macro-action.md">LogEvent, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-142"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-143">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-144"><a href="onerror-macro-action.md">OnError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-144"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-145">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-146"><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-146"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-147">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-148"><a href="rundatamacro-macro-action.md">RunDataMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-148"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-149">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-150"><a href="sendemail-macro-action.md">SendEmail, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-150"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-151">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-152"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-152"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-153">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-154"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-154"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad956-155">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-156"><a href="stopallmacros-macro-action.md">StopAllMacros, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-156"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad956-157">Action de données</span><span class="sxs-lookup"><span data-stu-id="ad956-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="ad956-158"><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="ad956-158"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad956-159">Pour créer une macro de données qui capture l'événement **Après suppression**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="ad956-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="ad956-160">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après suppression**.</span><span class="sxs-lookup"><span data-stu-id="ad956-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="ad956-161">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après suppression**.</span><span class="sxs-lookup"><span data-stu-id="ad956-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="ad956-162">Une macro de données vide s'affiche dans le concepteur de macros.</span><span class="sxs-lookup"><span data-stu-id="ad956-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="ad956-163">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad956-163">Example</span></span>

<span data-ttu-id="ad956-p104">L'exemple de code suivant utilise l'événement **Après suppression** pour effectuer un traitement lorsqu'un enregistrement est supprimé de la table Donations. Lorsqu'un enregistrement est supprimé, le montant d'un don est soustrait du champ DonationsReceived dans la table DonationsReceived et du champ TotalDonatedField dans la table Donors.</span><span class="sxs-lookup"><span data-stu-id="ad956-p104">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="ad956-166">**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le concepteurs de macros.**</span><span class="sxs-lookup"><span data-stu-id="ad956-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="ad956-167">Pour afficher cet exemple dans le concepteur de macros, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="ad956-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="ad956-168">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après suppression**.</span><span class="sxs-lookup"><span data-stu-id="ad956-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="ad956-169">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après suppression**.</span><span class="sxs-lookup"><span data-stu-id="ad956-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="ad956-170">Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="ad956-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="ad956-171">Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.</span><span class="sxs-lookup"><span data-stu-id="ad956-171">Activate the macro designer window and then press CTRL+V.</span></span>

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
