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
ms.openlocfilehash: b37fb96ddfeaabc97c6f445f8951876e8026fbfe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703957"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="4c6a1-102">Before Change, événement de macro</span><span class="sxs-lookup"><span data-stu-id="4c6a1-102">Before Change macro event</span></span>

<span data-ttu-id="4c6a1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c6a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c6a1-104">L'événement **Avant la modification** se produit lorsqu'un enregistrement change, mais avant la validation de la modification.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="4c6a1-105">[!REMARQUE] L'événement **Avant la modification** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6a1-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4c6a1-106">Remarks</span></span>

<span data-ttu-id="4c6a1-p101">Utilisez l'événement **Avant la modification** pour effectuer toute action souhaitée avant qu'un enregistrement soit modifié. **Avant la modification** s'utilise couramment pour effectuer une validation et pour déclencher des messages d'erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-p101">Use the **Before Change** event to perform any actions that you want to occur before a record is changed. The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="4c6a1-109">Vous pouvez utiliser la fonction de **mise à jour («*Nom de champ*»)** pour déterminer si un champ a été modifié.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="4c6a1-110">L’exemple de code suivant montre comment utiliser une instruction **If** pour déterminer si le champ PaidInFull a été modifié.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="4c6a1-p103">Utilisez la propriété **EstInsertion** pour déterminer si l'événement **Avant la modification** a été déclenché par la création d'un enregistrement ou par la modification d'un enregistrement existant. La propriété **EstInsertion** a la valeur **True** si l'événement a été déclenché par un nouvel enregistrement, **False** si l'événement a été déclenché par la modification d'un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-p103">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record. They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="4c6a1-113">L'exemple de code suivant illustre la syntaxe d'utilisation de la propriété **EstInsertion**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="4c6a1-114">Vous pouvez accéder à la valeur précédente dans un champ en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="4c6a1-115">Par exemple, pour accéder à la valeur précédente du champ QuantityInStock, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="4c6a1-116">Les valeurs précédentes sont supprimées de manière définitive lorsque l'événement **Avant la modification** se termine.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="4c6a1-p104">Vous pouvez annuler l'événement **Avant la modification** à l'aide de l'action **DéclencherErreur**. Lorsqu'une erreur est levée, les modifications contenues dans l'événement **Avant la modification** sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-p104">You can cancel the **Before Change** event by using the **RaiseError** action. When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="4c6a1-119">Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l’événement **Avant la modification**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-119">The following table lists macro commands that can be used in the**Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c6a1-120">Type de commande</span><span class="sxs-lookup"><span data-stu-id="4c6a1-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="4c6a1-121">Commande</span><span class="sxs-lookup"><span data-stu-id="4c6a1-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c6a1-122">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="4c6a1-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-123"><a href="comment-macro-statement.md">Comment, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6a1-124">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="4c6a1-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-125"><a href="group-macro-statement.md">Group, instruction de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-125"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6a1-126">Déroulement de programme</span><span class="sxs-lookup"><span data-stu-id="4c6a1-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-127"><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-127"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6a1-128">Bloc de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-129"><a href="lookuprecord-data-block.md">Action de macro RechercherEnregistrement</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-129"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6a1-130">Action de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-131"><a href="clearmacroerror-macro-action.md">ClearMacroError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6a1-132">Action de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-133"><a href="onerror-macro-action.md">OnError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-133"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6a1-134">Action de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-135"><a href="raiseerror-macro-action.md">RaiseError, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-135"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6a1-136">Action de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-137"><a href="setfield-macro-action.md">SetField, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-137"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6a1-138">Action de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-139"><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-139"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6a1-140">Action de données</span><span class="sxs-lookup"><span data-stu-id="4c6a1-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="4c6a1-141"><a href="stopmacro-macro-action.md">StopMacro, action de macro</a></span><span class="sxs-lookup"><span data-stu-id="4c6a1-141"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4c6a1-142">Pour créer une macro de données qui capture l'événement **Avant la modification**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4c6a1-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="4c6a1-143">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Avant la modification**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="4c6a1-144">Sous l'onglet **Table**, dans le groupe **Événements Avant**, cliquez sur **Avant la modification**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="4c6a1-145">Une macro de données vide s'affiche dans le concepteur de macros</span><span class="sxs-lookup"><span data-stu-id="4c6a1-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="4c6a1-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c6a1-146">Example</span></span>

<span data-ttu-id="4c6a1-147">L’exemple de code suivant utilise l’événement **Avant la modification** pour valider les champs de statut.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="4c6a1-148">Une erreur est levée si une valeur incorrecte est stockée dans le champ Resolution.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

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

<span data-ttu-id="4c6a1-149">Pour afficher cet exemple dans le concepteur de macros, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="4c6a1-150">Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Avant la modification**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="4c6a1-151">Sous l'onglet **Table**, dans le groupe **Événements Avant**, cliquez sur **Avant la modification**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="4c6a1-152">Sélectionnez le code dans l’exemple de code suivant et appuyez sur **CTRL + C** pour le copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="4c6a1-153">Activer la fenêtre du Concepteur de macros, puis appuyez sur **CTRL + V**.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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

<span data-ttu-id="4c6a1-154">L’exemple suivant montre comment utiliser l’action Déclenchererreur pour annuler l’événement de macro de données avant la modification.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="4c6a1-155">Lorsque le champ AssignedTo est mis à jour, un bloc de données RechercherEnregistrement permet de déterminer si le technicien affecté est actuellement affecté à une demande de service en cours.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="4c6a1-156">Si cela est vrai, puis l’événement avant la modification est annulée et l’enregistrement n’est pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4c6a1-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="4c6a1-157">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4c6a1-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
