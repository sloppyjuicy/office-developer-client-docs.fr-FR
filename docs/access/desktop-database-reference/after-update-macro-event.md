---
title: Après MAJ, événement de macro
TOCTitle: After Update Macro Event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6c4e854e13527f0c20551950aa49dde30cdae9ab
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862260"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="4431a-102">Après MAJ, événement de macro</span><span class="sxs-lookup"><span data-stu-id="4431a-102">After Update Macro Event</span></span>


<span data-ttu-id="4431a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4431a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4431a-104">L'événement **Après MAJ** se produit après la modification d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4431a-104">The **After Update** event occurs after a record is changed.</span></span>


> [!NOTE]
> <span data-ttu-id="4431a-105">[!REMARQUE] L'événement **Après MAJ** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="4431a-105">The **After Update** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="4431a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4431a-106">Remarks</span></span>

<span data-ttu-id="4431a-p101">Utilisez l'événement **Après MAJ** pour effectuer toute action souhaitée lorsqu'un enregistrement est modifié. L'événement **Après MAJ** peut par exemple servir à appliquer des règles professionnelles, à mettre à jour un total agrégé et à envoyer des notifications.</span><span class="sxs-lookup"><span data-stu-id="4431a-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="4431a-p102">Vous pouvez utiliser la fonction **Updated("*Nom de champ*")** pour déterminer si un champ a changé. L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.</span><span class="sxs-lookup"><span data-stu-id="4431a-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="4431a-111">Vous pouvez accéder à la valeur précédente dans un champ en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="4431a-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="4431a-112">Par exemple, pour accéder à la valeur précédente du champ QuantityInStock, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="4431a-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="4431a-113">Les valeurs précédentes sont supprimées de manière définitive lorsque l'événement **Après MAJ** se termine.</span><span class="sxs-lookup"><span data-stu-id="4431a-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="4431a-114">Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="4431a-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4431a-115">Type de commande</span><span class="sxs-lookup"><span data-stu-id="4431a-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="4431a-116">Commande</span><span class="sxs-lookup"><span data-stu-id="4431a-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4431a-117">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="4431a-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="4431a-118"><a href="comment-macro-statement.md">Instruction de Macro commentaire</a></span><span class="sxs-lookup"><span data-stu-id="4431a-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-119">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="4431a-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="4431a-120"><a href="group-macro-statement.md">Group, instruction de Macro</a></span><span class="sxs-lookup"><span data-stu-id="4431a-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-121">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="4431a-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="4431a-122"><a href="if-then-else-macro-block.md">If... Procédez comme suit... Autre bloc de Macro</a></span><span class="sxs-lookup"><span data-stu-id="4431a-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-123">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="4431a-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="4431a-124"><a href="createrecord-data-block.md">Action de Macro CréerEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="4431a-124"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-125">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="4431a-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="4431a-126"><a href="editrecord-data-block.md">Action de Macro ModifierEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="4431a-126"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-127">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="4431a-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="4431a-128"><a href="foreachrecord-data-block.md">Action de Macro PourChaqueEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="4431a-128"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-129">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="4431a-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="4431a-130"><a href="lookuprecord-data-block.md">LookupRecord, bloc de données</a></span><span class="sxs-lookup"><span data-stu-id="4431a-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-131">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-132"><a href="cancelrecordchange-macro-action.md">Action de Macro AnnulerModificationEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="4431a-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-133">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-134"><a href="clearmacroerror-macro-action.md">Action de Macro EffacerMacroErreur</a></span><span class="sxs-lookup"><span data-stu-id="4431a-134"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-135">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-136"><a href="deleterecord-macro-action.md">Action de Macro DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="4431a-136"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-137">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-138"><a href="exitforeachrecord-macro-action.md">Action de Macro QuitterPourChaqueEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="4431a-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-139">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-140"><a href="logevent-macro-action.md">Action de Macro LogEvent</a></span><span class="sxs-lookup"><span data-stu-id="4431a-140"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-141">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-142"><a href="onerror-macro-action.md">Action de Macro SurErreur</a></span><span class="sxs-lookup"><span data-stu-id="4431a-142"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-143">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-144"><a href="raiseerror-macro-action.md">Action de Macro Déclenchererreur</a></span><span class="sxs-lookup"><span data-stu-id="4431a-144"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-145">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-146"><a href="rundatamacro-macro-action.md">Action de Macro ExécuterMacroDonnées</a></span><span class="sxs-lookup"><span data-stu-id="4431a-146"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-147">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-148"><a href="sendemail-macro-action.md">Action de Macro SendEmail</a></span><span class="sxs-lookup"><span data-stu-id="4431a-148"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-149">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-150"><a href="setfield-macro-action.md">Action de Macro SetField</a></span><span class="sxs-lookup"><span data-stu-id="4431a-150"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-151">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-152"><a href="setlocalvar-macro-action.md">Action de Macro DéfinirVarLocale</a></span><span class="sxs-lookup"><span data-stu-id="4431a-152"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4431a-153">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-154"><a href="stopallmacros-macro-action.md">Action de Macro ArrêtToutesMacros</a></span><span class="sxs-lookup"><span data-stu-id="4431a-154"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4431a-155">Action de données</span><span class="sxs-lookup"><span data-stu-id="4431a-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4431a-156"><a href="stopmacro-macro-action.md">Action de Macro ArrêtMacro</a></span><span class="sxs-lookup"><span data-stu-id="4431a-156"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4431a-157">Pour créer une macro de données qui capture l'événement **Après MAJ**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4431a-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="4431a-158">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="4431a-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="4431a-159">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="4431a-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="4431a-160">Une macro de données vide s'affiche dans le concepteur de macros</span><span class="sxs-lookup"><span data-stu-id="4431a-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="4431a-161">Exemple</span><span class="sxs-lookup"><span data-stu-id="4431a-161">Example</span></span>

<span data-ttu-id="4431a-162">L'exemple de code suivant utilise l'événement **Après MAJ** pour exécuter une macro de données nommée qui ajoute un enregistrement à la table Comment chaque fois que l'état d'un problème est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4431a-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="4431a-163">**Cliquez ici pour afficher une copie de la macro que vous pouvez coller dans le concepteurs de macros.**</span><span class="sxs-lookup"><span data-stu-id="4431a-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="4431a-164">Pour afficher cet exemple dans le concepteur de macros, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4431a-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="4431a-165">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="4431a-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="4431a-166">Sous l'onglet **Table**, dans le groupe **Événements Après**, cliquez sur **Après MAJ**.</span><span class="sxs-lookup"><span data-stu-id="4431a-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="4431a-167">Sélectionnez le code ci-dessous et appuyez sur Ctrl+C pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="4431a-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="4431a-168">Activez la fenêtre du concepteur de macros, puis appuyez sur Ctrl+V.</span><span class="sxs-lookup"><span data-stu-id="4431a-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

