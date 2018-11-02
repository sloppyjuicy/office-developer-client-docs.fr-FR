---
title: Propriété Recordset2.RecordStatus (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 178872a9-e361-f277-627d-f91b01ceb6d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845575(v=office.15)
ms:contentKeyID: 48543451
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fc80ac2ee1616c9203d2c178a2bd28decb771e2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920283"
---
# <a name="recordset2recordstatus-property-dao"></a>Propriété Recordset2.RecordStatus (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . RecordStatus

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

La valeur de la propriété **RecordStatus** détermine si l'enregistrement actif fera partie de la prochaine mise à jour par lot optimiste et de quelle manière.

Lorsqu'un utilisateur modifie un enregistrement, la propriété **RecordStatus** de cet enregistrement prend automatiquement la valeur **dbRecordModified**. De la même façon, si un enregistrement est ajouté ou supprimé, **RecordStatus** prend la valeur de la constante appropriée. Lorsque vous utilisez ensuite une méthode **[Update](recordset2-update-method-dao.md)** par lot, DAO soumet au serveur distant l'opération appropriée pour chaque enregistrement en fonction de la propriété **RecordStatus** de l'enregistrement.

## <a name="example"></a>Exemple

L'exemple ci-dessous fait appel aux propriétés **RecordStatus** et **DefaultCursorDriver** pour indiquer comment le suivi des modifications apportées à un objet **Recordset** local est effectué lors d'une mise à jour par lot. La fonction RecordStatusOutput est requise pour pouvoir exécuter cette procédure.

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

