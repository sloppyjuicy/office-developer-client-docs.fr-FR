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
# <a name="after-update-macro-event"></a><span data-ttu-id="c9226-102">After Update, événement de macro</span><span class="sxs-lookup"><span data-stu-id="c9226-102">After Update macro event</span></span>

<span data-ttu-id="c9226-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9226-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9226-104">L'événement **Après MAJ** se produit après la modification d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c9226-104">The **After Update** event occurs after a record is changed.</span></span>

> [!NOTE]
> <span data-ttu-id="c9226-105">L’événement **Après MAJ** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="c9226-105">The **After Update** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9226-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9226-106">Remarks</span></span>

<span data-ttu-id="c9226-p101">Utilisez l’événement **Après MAJ** pour effectuer toute action souhaitée lorsqu’un enregistrement est modifié. L’événement **Après MAJ** peut par exemple servir à appliquer des règles professionnelles, à mettre à jour un total agrégé et à envoyer des notifications.</span><span class="sxs-lookup"><span data-stu-id="c9226-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="c9226-109">Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé.</span><span class="sxs-lookup"><span data-stu-id="c9226-109">You can use the *Updated("**Field Name**")* function to determine whether a field has changed.</span></span> <span data-ttu-id="c9226-110">L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.</span><span class="sxs-lookup"><span data-stu-id="c9226-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="c9226-111">Vous pouvez accéder à la valeur précédente dans un champ en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="c9226-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="c9226-112">Par exemple, pour accéder à la valeur précédente du champ QuantityInStock, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="c9226-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="c9226-113">Les valeurs précédentes sont supprimées de manière définitive lorsque l'événement **Après MAJ** se termine.</span><span class="sxs-lookup"><span data-stu-id="c9226-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="c9226-114">Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="c9226-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9226-115">Type de commande</span><span class="sxs-lookup"><span data-stu-id="c9226-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="c9226-116">Command</span><span class="sxs-lookup"><span data-stu-id="c9226-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9226-117">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="c9226-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="c9226-118"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-119">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="c9226-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="c9226-120"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-121">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="c9226-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="c9226-122"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-123">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="c9226-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c9226-124"><a href="createrecord-data-block.md">CreateRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-124"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-125">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="c9226-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c9226-126"><a href="editrecord-data-block.md">EditRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-126"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-127">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="c9226-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c9226-128"><a href="foreachrecord-data-block.md">ForEachRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-128"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-129">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="c9226-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c9226-130"><a href="lookuprecord-data-block.md">LookupRecord, bloc de données</a></span><span class="sxs-lookup"><span data-stu-id="c9226-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-131">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-133">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-134"><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-135">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-136"><a href="deleterecord-macro-action.md">DeleteRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-137">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-139">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-140"><a href="logevent-macro-action.md">LogEvent, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-141">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-142"><a href="onerror-macro-action.md">OnError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-143">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-144"><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-145">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-146"><a href="rundatamacro-macro-action.md">RunDataMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-147">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-148"><a href="sendemail-macro-action.md">SendEmail, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-149">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-150"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-151">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-152"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9226-153">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-154"><a href="stopallmacros-macro-action.md">StopAllMacros, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9226-155">Action de données</span><span class="sxs-lookup"><span data-stu-id="c9226-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c9226-156"><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="c9226-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9226-157">Pour créer une macro de données qui capture l'événement **Après MAJ**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c9226-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="c9226-158">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="c9226-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="c9226-159">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="c9226-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="c9226-160">Une macro de données vide s’affiche dans le concepteur de macros</span><span class="sxs-lookup"><span data-stu-id="c9226-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="c9226-161">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9226-161">Example</span></span>

<span data-ttu-id="c9226-162">L’exemple de code suivant utilise l’événement **Après MAJ** pour exécuter une macro de données nommée qui ajoute un enregistrement à la table Comment chaque fois que l’état d’un problème est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c9226-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="c9226-163">**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le Concepteur de macros.**</span><span class="sxs-lookup"><span data-stu-id="c9226-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="c9226-164">Pour afficher cet exemple dans le concepteur de macros, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c9226-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="c9226-165">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="c9226-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="c9226-166">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="c9226-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="c9226-167">Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="c9226-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="c9226-168">Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.</span><span class="sxs-lookup"><span data-stu-id="c9226-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

