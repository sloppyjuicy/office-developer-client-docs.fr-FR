---
title: Méthode Recordset.Update (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d81eaf181a87d6afc13dbf2908be307d120d349
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997020"
---
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="874e8-102">Méthode Recordset.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="874e8-102">Recordset.Update method (DAO)</span></span>

<span data-ttu-id="874e8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="874e8-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="874e8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="874e8-104">Syntax</span></span>

<span data-ttu-id="874e8-105">*expression* . Mise à jour (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="874e8-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="874e8-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="874e8-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="874e8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="874e8-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="874e8-108">Name</span><span class="sxs-lookup"><span data-stu-id="874e8-108">Name</span></span></p></th>
<th><p><span data-ttu-id="874e8-109">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="874e8-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="874e8-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="874e8-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="874e8-111">Description</span><span class="sxs-lookup"><span data-stu-id="874e8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="874e8-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="874e8-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="874e8-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="874e8-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="874e8-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="874e8-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="874e8-115">Constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> qui indique le type de mise à jour, comme spécifié dans les paramètres (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="874e8-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="874e8-116"><em>Force</em></span><span class="sxs-lookup"><span data-stu-id="874e8-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="874e8-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="874e8-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="874e8-118"><strong>Booléen</strong></span><span class="sxs-lookup"><span data-stu-id="874e8-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="874e8-p101">Valeur <strong>booléenne</strong> indiquant si les modifications doivent être forcées ou non dans la base de données, indépendamment du fait que les données sous-jacentes aient été modifiées par un autre utilisateur depuis l'appel de <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Si la valeur est <strong>True</strong>, les modifications sont forcées et les modifications apportées par d'autres utilisateurs sont tout simplement remplacées. Si la valeur est <strong>False</strong> (valeur par défaut), les modifications apportées par d'autres utilisateurs tandis que la mise à jour est en attente entraîneront l'échec de la mise à jour pour les modifications en conflit. Aucune erreur ne se produit, mais les propriétés <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> et <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> indiqueront le nombre de conflits et les lignes concernées par ces conflits, respectivement (espaces de travail ODBCDirect uniquement).  </span><span class="sxs-lookup"><span data-stu-id="874e8-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="874e8-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="874e8-123">Remarks</span></span>

<span data-ttu-id="874e8-124">Utilisez la méthode **Update** pour enregistrer l'enregistrement actif et les modifications que vous y avez effectuées.</span><span class="sxs-lookup"><span data-stu-id="874e8-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="874e8-125">[!IMPORTANTE] Les modifications apportées à l'enregistrement actif sont perdues dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="874e8-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="874e8-126">vous utilisez la méthode **Edit** ou **AddNew** et passez à un autre enregistrement sans utiliser au préalable la méthode **Update**;</span><span class="sxs-lookup"><span data-stu-id="874e8-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="874e8-127">vous utilisez la méthode **Edit** ou **AddNew**, puis vous réutilisez la méthode **Edit** ou **AddNew** sans utiliser au préalable la méthode **Update**</span><span class="sxs-lookup"><span data-stu-id="874e8-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="874e8-128">vous affectez la propriété **[Bookmark](recordset-bookmark-property-dao.md)** à un autre enregistrement ;</span><span class="sxs-lookup"><span data-stu-id="874e8-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="874e8-129">vous fermez l'objet **Recordset** sans utiliser au préalable la méthode **Update**;</span><span class="sxs-lookup"><span data-stu-id="874e8-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="874e8-130">vous annulez l'opération **Edit** par le biais de la méthode **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="874e8-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="874e8-p102">Pour modifier un enregistrement, utilisez la méthode **Edit** pour copier le contenu de l'enregistrement actif dans la mémoire tampon de la copie. Si vous n'utilisez pas d'abord la méthode **Edit**, une erreur se produit lorsque vous utilisez **Update** ou que vous tentez de modifier la valeur d'un champ.</span><span class="sxs-lookup"><span data-stu-id="874e8-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="874e8-133">Dans un espace de travail ODBCDirect, vous pouvez effectuer des mises à jour par lot, à condition que la bibliothèque de curseurs prenne en charge ce type d'opération et que l'objet **Recordset** ait été ouvert avec l'option de verrouillage par lot optimiste.</span><span class="sxs-lookup"><span data-stu-id="874e8-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="874e8-134">Dans un espace de travail Microsoft Access, lorsque la propriété **LockEdits** de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé du moment où la méthode **Edit** est utilisée jusqu'à l'exécution de la méthode **Update** ou l'annulation de la modification.</span><span class="sxs-lookup"><span data-stu-id="874e8-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="874e8-135">Si la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement tel qu'il était avant sa modification juste avant sa mise à jour dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="874e8-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="874e8-136">Si l'enregistrement a changé depuis l'utilisation de la méthode **Edit**, l'opération **Update** échoue.</span><span class="sxs-lookup"><span data-stu-id="874e8-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="874e8-137">Les bases de données ODBC et ISAM installables connectées au moteur de base de données Microsoft Access utilisent toujours un verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="874e8-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="874e8-138">Pour poursuivre l'opération **Update** avec vos modifications, utilisez à nouveau la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="874e8-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="874e8-139">Pour revenir à l’enregistrement en tant que l’autre utilisateur l’avait modifié, actualisez l’enregistrement actif en utilisant Move 0.</span><span class="sxs-lookup"><span data-stu-id="874e8-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="874e8-p105">[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l'enregistrement dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produit sur l'appel de méthode **AddNew**, **Delete** ou **Edit** dans un espace de travail Microsoft Access ou une erreur « Argument non valide » se produit sur l'appel **Update** dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="874e8-p105">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="874e8-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="874e8-142">Example</span></span>

<span data-ttu-id="874e8-143">Cet exemple illustre la méthode **Update** conjointement avec la méthode **Edit**.</span><span class="sxs-lookup"><span data-stu-id="874e8-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

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

<span data-ttu-id="874e8-144">Cet exemple illustre la méthode **Update** conjointement avec la méthode **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="874e8-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

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

<span data-ttu-id="874e8-145">Cet exemple illustre la propriété **BatchCollisionCount** et la méthode **Update** pour démontrer la mise à jour par lot lorsque les éventuels conflits sont résolus en forçant la mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="874e8-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

<span data-ttu-id="874e8-p106">Cet exemple utilise la méthode **AddNew** pour créer un enregistrement avec le nom spécifié. La fonction AddName est nécessaire pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="874e8-p106">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
