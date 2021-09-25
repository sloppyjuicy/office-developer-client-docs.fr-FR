---
title: Recordset2.CopyQueryDef, méthode (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: 36689ac0-f8a6-1f3e-4170-799141373777
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192474(v=office.15)
ms:contentKeyID: 48544170
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053073
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c130a63b7949dfb04f9470e0e2e4098042ea26c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596910"
---
# <a name="recordset2copyquerydef-method-dao"></a>Recordset2.CopyQueryDef, méthode (DAO)


**S’applique à** : Access 2013, Office 2013 

Renvoie un objet **[QueryDef](querydef-object-dao.md)** qui est une copie de l’objet **QueryDef** utilisé pour créer l’objet **[Recordset](recordset-object-dao.md)** représenté par l’espace réservé recordset (espaces de travail Microsoft Access uniquement). .

## <a name="syntax"></a>Syntaxe

*.* CopyQueryDef

*expression* Variable qui représente un **objet Recordset2.**

## <a name="return-value"></a>Valeur renvoyée

QueryDef

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **CopyQueryDef** pour créer un nouvel objet **QueryDef** qui est un doublon de l'objet **QueryDef** ayant servi à créer l'objet **Recordset**.

Si aucun objet **QueryDef** n'a servi à créer cet objet **Recordset**, une erreur se produit. Vous devez d'abord ouvrir un objet **Recordset** par le biais de la méthode **OpenRecordset** avant d'utiliser la méthode **CopyQueryDef**.

Cette méthode s'avère utile pour créer un objet **Recordset** à partir d'un objet **QueryDef**, et transmettre cet objet **Recordset** à une fonction ; la fonction doit recréer l'équivalent SQL de la requête, par exemple, pour la modifier d'une certaine manière.

## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **CopyQueryDef** pour créer une copie d'un objet **QueryDef** à partir d'un objet **Recordset** existant et comment modifier cette copie en ajoutant une clause à la propriété SQL. Lorsque vous créez un objet **QueryDef** permanent, il se peut que des espaces, des points-virgules ou des sauts de ligne soient ajoutés à la propriété SQL ; ces caractères supplémentaires doivent être supprimés pour pouvoir joindre de nouvelles clauses à l'instruction SQL.

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```     

<br/>

Cet exemple de code illustre une utilisation possible de CopyQueryNew().

```vb
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset2 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

