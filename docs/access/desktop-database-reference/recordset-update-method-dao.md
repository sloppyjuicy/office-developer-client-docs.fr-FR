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
# <a name="recordsetupdate-method-dao"></a>Méthode Recordset.Update (DAO)

**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour (***UpdateType***, ***Force***)

*expression* Variable qui représente un objet **Recordset** .

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
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> qui indique le type de mise à jour, comme spécifié dans les paramètres (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Booléen</strong></p></td>
<td><p>Valeur <strong>booléenne</strong> indiquant si les modifications doivent être forcées ou non dans la base de données, indépendamment du fait que les données sous-jacentes aient été modifiées par un autre utilisateur depuis l'appel de <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset-edit-method-dao.md">Edit</a></strong>. Si la valeur est <strong>True</strong>, les modifications sont forcées et les modifications apportées par d'autres utilisateurs sont tout simplement remplacées. Si la valeur est <strong>False</strong> (valeur par défaut), les modifications apportées par d'autres utilisateurs tandis que la mise à jour est en attente entraîneront l'échec de la mise à jour pour les modifications en conflit. Aucune erreur ne se produit, mais les propriétés <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> et <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> indiqueront le nombre de conflits et les lignes concernées par ces conflits, respectivement (espaces de travail ODBCDirect uniquement).  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez la méthode **Update** pour enregistrer l'enregistrement actif et les modifications que vous y avez effectuées.

> [!IMPORTANT]
> [!IMPORTANTE] Les modifications apportées à l'enregistrement actif sont perdues dans les cas suivants :
> - vous utilisez la méthode **Edit** ou **AddNew** et passez à un autre enregistrement sans utiliser au préalable la méthode **Update**;
> - vous utilisez la méthode **Edit** ou **AddNew**, puis vous réutilisez la méthode **Edit** ou **AddNew** sans utiliser au préalable la méthode **Update**
> - vous affectez la propriété **[Bookmark](recordset-bookmark-property-dao.md)** à un autre enregistrement ;
> - vous fermez l'objet **Recordset** sans utiliser au préalable la méthode **Update**;
> - vous annulez l'opération **Edit** par le biais de la méthode **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Pour modifier un enregistrement, utilisez la méthode **Edit** pour copier le contenu de l'enregistrement actif dans la mémoire tampon de la copie. Si vous n'utilisez pas d'abord la méthode **Edit**, une erreur se produit lorsque vous utilisez **Update** ou que vous tentez de modifier la valeur d'un champ.

Dans un espace de travail ODBCDirect, vous pouvez effectuer des mises à jour par lot, à condition que la bibliothèque de curseurs prenne en charge ce type d'opération et que l'objet **Recordset** ait été ouvert avec l'option de verrouillage par lot optimiste.

Dans un espace de travail Microsoft Access, lorsque la propriété **LockEdits** de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé du moment où la méthode **Edit** est utilisée jusqu'à l'exécution de la méthode **Update** ou l'annulation de la modification. Si la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement tel qu'il était avant sa modification juste avant sa mise à jour dans la base de données. 

Si l'enregistrement a changé depuis l'utilisation de la méthode **Edit**, l'opération **Update** échoue. Les bases de données ODBC et ISAM installables connectées au moteur de base de données Microsoft Access utilisent toujours un verrouillage optimiste. Pour poursuivre l'opération **Update** avec vos modifications, utilisez à nouveau la méthode **Update**. Pour revenir à l’enregistrement en tant que l’autre utilisateur l’avait modifié, actualisez l’enregistrement actif en utilisant Move 0.

> [!NOTE]
> [!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l'enregistrement dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produit sur l'appel de méthode **AddNew**, **Delete** ou **Edit** dans un espace de travail Microsoft Access ou une erreur « Argument non valide » se produit sur l'appel **Update** dans un espace de travail ODBCDirect.

## <a name="example"></a>Exemple

Cet exemple illustre la méthode **Update** conjointement avec la méthode **Edit**.

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

Cet exemple illustre la méthode **Update** conjointement avec la méthode **AddNew**.

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

Cet exemple illustre la propriété **BatchCollisionCount** et la méthode **Update** pour démontrer la mise à jour par lot lorsque les éventuels conflits sont résolus en forçant la mise à jour par lot.

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

Cet exemple utilise la méthode **AddNew** pour créer un enregistrement avec le nom spécifié. La fonction AddName est nécessaire pour exécuter cette procédure.

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
