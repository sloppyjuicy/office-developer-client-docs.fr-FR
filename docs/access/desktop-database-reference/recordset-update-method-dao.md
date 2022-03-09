---
title: Recordset.Update, méthode (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 738df3357538ea7daf9a227f8a0c380b0dff0af7
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464837"
---
# <a name="recordsetupdate-method-dao"></a>Recordset.Update, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* .Update(***UpdateType** _, _*_Force_**)

*expression* Variable qui représente un objet **Recordset**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>A <strong> <a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a> </strong> constante indiquant le type de mise à jour, comme spécifié dans les paramètres (espaces).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>A <strong>booléenne</strong> valeur indiquant forcer les modifications dans la base de données quelle que soit la si les données sous-jacentes a été modifiées par un autre utilisateur depuis ou non le <strong> <a href="recordset-addnew-method-dao.md">AddNew</a> </strong>, <strong> <a href="fields-delete-method-dao.md">Supprimer</a></strong>, ou <strong> <a href="recordset-edit-method-dao.md">modifier</a> </strong> appeler. Si <strong>vrai</strong>, les modifications sont forcées et les modifications apportées par d’autres utilisateurs sont simplement remplacées. Si <strong>faux</strong> (par défaut), les modifications apportées par un autre utilisateur alors que la mise à jour est en attente entraînera la mise à jour Échec pour ces modifications sont en conflit. Aucune erreur se produit, mais le <strong> <a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a> </strong> et <strong> <a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a> </strong> propriétés indique le nombre des conflits et les lignes concernées par conflits, respectivement (espaces).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez **mise à jour** pour enregistrer l’enregistrement actif et toutes les modifications apportées à celui-ci.

> [!IMPORTANT]
> Enregistrer les modifications apportées à l’enregistrement actif
> - Vous utilisez le **modifier** ou **AddNew** méthode, puis accéder à un autre enregistrement sans utiliser première **mise à jour**.
> - Vous utilisez **modifier** ou **AddNew**, puis utilisez **modifier** ou **AddNew** nouveau sans utiliser première **mise à jour**.
> - Vous définissez la **[signet](recordset-bookmark-property-dao.md)** propriété vers un autre enregistrement.
> - Vous fermez le **jeu d’enregistrements** sans utiliser première **mise à jour**.
> - Vous annulez la **modifier** opération à l’aide **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Pour modifier un enregistrement, utilisez la **modifier** méthode pour copier le contenu de l’enregistrement actif dans la mémoire tampon de copie. Si vous n’utilisez **modifier** tout d’abord, une erreur se produit lorsque vous utilisez **mise à jour** ou tenter de modifier la valeur du champ.

Dans un espace de travail ODBCDirect, vous pouvez effectuer par lot mises à jour, sous réserve la bibliothèque curseur prend en charge les mises à jour du lot et le **jeu d’enregistrements** a été ouvert avec l’option de verrouillage par lot optimiste.

Dans un espace de travail Microsoft Access, lorsque paramètre de propriété **LockEdits** de l’objet de **Recordset** est défini sur **True** (verrouillage pessimiste ) dans un environnement multi-utilisateur, l’enregistrement reste verrouillé à partir de l’heure de l’utilisation de **Edit** jusqu'à ce que la méthode **Update** soit exécutée ou que la modification soit terminée. Si la propriété **LockEdits** est définie sur **False** (verrouillage optimiste), l’enregistrement est verrouillé et comparé par rapport à l’enregistrement déjà modifié juste avant sa mise à jour dans la base de données. 

Si l’enregistrement a été modifié depuis que vous avez utilisé la méthode **Edit**, l’opération **Update** échoue. Les bases de données ODBC connectées au moteur de base de données Microsoft Access et aux bases de données ISAM installables utilisent toujours un verrouillage optimiste. Pour continuer l’opération **Update** avec vos modifications, utilisez à nouveau la méthode **Update**. Pour rétablir l’enregistrement tel que l’autre utilisateur l’avait modifié, actualisez l’enregistrement actif à l’aide de Move 0.

> [!NOTE]
> Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l’enregistrement dans la source de données sous-jacentes. Si non, une erreur « Autorisation refusée » doit se produire sur le **AddNew**, **supprimer**, ou **modifier** méthode appel dans un espace de travail Microsoft Access ou une erreur « Argument non valide » se produit sur la **mise à jour** appeler dans un espace de travail ODBCDirect.

## <a name="example"></a>Exemple

Cet exemple illustre la **mise à jour** méthode conjointement avec **modifier** méthode.

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


Cet exemple illustre la **mise à jour** méthode conjointement avec la **AddNew** méthode.

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


Cet exemple utilise la **BatchCollisionCount** propriété et le **mettre à jour** méthode démontre lot la mise à jour dans laquelle les conflits sont résolus en forçant la mise à jour du lot.

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


Cet exemple utilise la **AddNew** méthode permettant de créer un enregistrement avec le nom spécifié. La fonction AddName est requise pour exécuter cette procédure.

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
