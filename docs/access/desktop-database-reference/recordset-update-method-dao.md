---
title: Recordset.Update, méthode (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 9f73dfc49a6ec99b726a052c588c032783010081
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307524"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="69fbe-102">Recordset.Update, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="69fbe-102">Recordset.Update Method (DAO)</span></span>

<span data-ttu-id="69fbe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69fbe-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="69fbe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69fbe-104">Syntax</span></span>

<span data-ttu-id="69fbe-105">*expression* .Update(***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="69fbe-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="69fbe-106">*expression* Variable représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="69fbe-106">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="69fbe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69fbe-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69fbe-108">Nom</span><span class="sxs-lookup"><span data-stu-id="69fbe-108">Name</span></span></p></th>
<th><p><span data-ttu-id="69fbe-109">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="69fbe-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="69fbe-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="69fbe-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="69fbe-111">Description</span><span class="sxs-lookup"><span data-stu-id="69fbe-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69fbe-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="69fbe-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="69fbe-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="69fbe-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="69fbe-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="69fbe-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="69fbe-115">A <strong> <a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a> </strong> constante indiquant le type de mise à jour, comme spécifié dans les paramètres (espaces).</span><span class="sxs-lookup"><span data-stu-id="69fbe-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69fbe-116"><em>Force</em></span><span class="sxs-lookup"><span data-stu-id="69fbe-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="69fbe-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="69fbe-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="69fbe-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="69fbe-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="69fbe-p101">A <strong>booléenne</strong> valeur indiquant forcer les modifications dans la base de données quelle que soit la si les données sous-jacentes a été modifiées par un autre utilisateur depuis ou non le <strong> <a href="recordset-addnew-method-dao.md">AddNew</a> </strong>, <strong> <a href="fields-delete-method-dao.md">Supprimer</a></strong>, ou <strong> <a href="recordset-edit-method-dao.md">modifier</a> </strong> appeler. Si <strong>vrai</strong>, les modifications sont forcées et les modifications apportées par d’autres utilisateurs sont simplement remplacées. Si <strong>faux</strong> (par défaut), les modifications apportées par un autre utilisateur alors que la mise à jour est en attente entraînera la mise à jour Échec pour ces modifications sont en conflit. Aucune erreur se produit, mais le <strong> <a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a> </strong> et <strong> <a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a> </strong> propriétés indique le nombre des conflits et les lignes concernées par conflits, respectivement (espaces).</span><span class="sxs-lookup"><span data-stu-id="69fbe-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="69fbe-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="69fbe-123">Remarks</span></span>

<span data-ttu-id="69fbe-124">Utilisez **mise à jour** pour enregistrer l’enregistrement actif et toutes les modifications apportées à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="69fbe-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69fbe-125">Enregistrer les modifications apportées à l’enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="69fbe-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="69fbe-126">Vous utilisez le **modifier** ou **AddNew** méthode, puis accéder à un autre enregistrement sans utiliser première **mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="69fbe-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="69fbe-127">Vous utilisez **modifier** ou **AddNew**, puis utilisez **modifier** ou **AddNew** nouveau sans utiliser première **mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="69fbe-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="69fbe-128">Vous définissez la \*\* [signet](recordset-bookmark-property-dao.md) \*\* propriété vers un autre enregistrement.</span><span class="sxs-lookup"><span data-stu-id="69fbe-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="69fbe-129">Vous fermez le **jeu d’enregistrements** sans utiliser première **mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="69fbe-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="69fbe-130">Vous annulez la **modifier** opération à l’aide \*\* [CancelUpdate](recordset-cancelupdate-method-dao.md)\*\*.</span><span class="sxs-lookup"><span data-stu-id="69fbe-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="69fbe-p102">Pour modifier un enregistrement, utilisez la **modifier** méthode pour copier le contenu de l’enregistrement actif dans la mémoire tampon de copie. Si vous n’utilisez **modifier** tout d’abord, une erreur se produit lorsque vous utilisez **mise à jour** ou tenter de modifier la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="69fbe-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="69fbe-133">Dans un espace de travail ODBCDirect, vous pouvez effectuer par lot mises à jour, sous réserve la bibliothèque curseur prend en charge les mises à jour du lot et le **jeu d’enregistrements** a été ouvert avec l’option de verrouillage par lot optimiste.</span><span class="sxs-lookup"><span data-stu-id="69fbe-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="69fbe-134">Dans un espace de travail Microsoft Access, lorsque le **jeu d’enregistrements** d’objet **LockEdits** paramètre de la propriété est **vrai** (verrouillage pessimiste) dans un environnement multi-utilisateurs, l’enregistrement reste verrouillé à partir du moment **modifier** sert jusqu'à ce que le **mise à jour** méthode est exécutée ou la modification est annulée.</span><span class="sxs-lookup"><span data-stu-id="69fbe-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="69fbe-135">Si le **LockEdits** paramètre de la propriété est **faux** (verrouillage optimiste), l’enregistrement est verrouillé et par rapport à l’enregistrement déjà modifiée juste avant qu’il est mis à jour dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="69fbe-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="69fbe-136">Si l’enregistrement a changé, car vous avez utilisé le **modifier** méthode, le **mise à jour** opération échoue.</span><span class="sxs-lookup"><span data-stu-id="69fbe-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="69fbe-137">Base de données Microsoft Access connectées moteur ODBC et bases de données ISAM toujours utilisent le verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="69fbe-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="69fbe-138">Pour continuer la **mise à jour** opération avec vos modifications, utilisez la **mise à jour** méthode nouveau.</span><span class="sxs-lookup"><span data-stu-id="69fbe-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="69fbe-139">Pour revenir à l’enregistrement tel que l’autre utilisateur l’a modifié, actualisez l’enregistrement actif à l’aide de la commande Move 0.</span><span class="sxs-lookup"><span data-stu-id="69fbe-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="69fbe-p105">Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l’enregistrement dans la source de données sous-jacentes. Si non, une erreur « Autorisation refusée » doit se produire sur le **AddNew**, **supprimer**, ou **modifier** méthode appel dans un espace de travail Microsoft Access ou une erreur « Argument non valide » se produit sur la **mise à jour** appeler dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="69fbe-p105">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="69fbe-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="69fbe-142">Example</span></span>

<span data-ttu-id="69fbe-143">Cet exemple illustre la **mise à jour** méthode conjointement avec **modifier** méthode.</span><span class="sxs-lookup"><span data-stu-id="69fbe-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

```vb
    Sub UpdateX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .Edit 
     ' Store original data. 
     strOldFirst = !FirstName 
     strOldLast = !LastName 
     ' Change data in edit buffer. 
     !FirstName = "Linda" 
     !LastName = "Kobara" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "Edit in progress:" & vbCr & _ 
     " Original data = " & strOldFirst & " " & _ 
     strOldLast & vbCr & " Data in buffer = " & _ 
     !FirstName & " " & !LastName & vbCr & vbCr & _ 
     "Use Update to replace the original data with " & _ 
     "the buffered data in the Recordset?" 
     
     If MsgBox(strMessage, vbYesNo) = vbYes Then 
     .Update 
     Else 
     .CancelUpdate 
     End If 
     
     ' Show the resulting data. 
     MsgBox "Data in recordset = " & !FirstName & " " & _ 
     !LastName 
     
     ' Restore original data because this is a demonstration. 
     If Not (strOldFirst = !FirstName And _ 
     strOldLast = !LastName) Then 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="69fbe-144">Cet exemple illustre la **mise à jour** méthode conjointement avec la **AddNew** méthode.</span><span class="sxs-lookup"><span data-stu-id="69fbe-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

```vb
    Sub UpdateX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .AddNew 
     !FirstName = "Bill" 
     !LastName = "Sornsin" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "AddNew in progress:" & vbCr & _ 
     " Data in buffer = " & !FirstName & " " & _ 
     !LastName & vbCr & vbCr & _ 
     "Use Update to save buffer to recordset?" 
     
     If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
     .Update 
     ' Go to the new record and show the resulting data. 
     .Bookmark = .LastModified 
     MsgBox "Data in recordset = " & !FirstName & _ 
     " " & !LastName 
     ' Delete new data because this is a demonstration. 
     .Delete 
     Else 
     .CancelUpdate 
     MsgBox "No new record added." 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="69fbe-145">Cet exemple utilise la **BatchCollisionCount** propriété et le **mettre à jour** méthode démontre lot la mise à jour dans laquelle les conflits sont résolus en forçant la mise à jour du lot.</span><span class="sxs-lookup"><span data-stu-id="69fbe-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="69fbe-p106">Cet exemple utilise la **AddNew** méthode permettant de créer un enregistrement avec le nom spécifié. La fonction AddName est requise pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="69fbe-p106">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
