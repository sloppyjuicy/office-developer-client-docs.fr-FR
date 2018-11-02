---
title: Méthode Recordset2.CopyQueryDef (DAO)
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
ms.openlocfilehash: 8ea2bd660679b093ad031b6ce4d5f3c64b335893
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929789"
---
# <a name="recordset2copyquerydef-method-dao"></a>Méthode Recordset2.CopyQueryDef (DAO)


**S’applique à**: Access 2013, Office 2013 

Renvoie un objet **[QueryDef](querydef-object-dao.md)** qui est une copie de l' **objet QueryDef** utilisé pour créer l’objet **[Recordset](recordset-object-dao.md)** représenté par l’espace réservé du jeu d’enregistrements (espaces de travail Microsoft Access uniquement). .

## <a name="syntax"></a>Syntaxe

*expression* . CopyQueryDef

*expression* Variable qui représente un objet **Recordset2** .

### <a name="return-value"></a>Valeur renvoyée

Objet QueryDef

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **CopyQueryDef** pour créer un nouvel objet **QueryDef** qui est un doublon de l'objet **QueryDef** utilisé pour créer l'objet **Recordset**.

Si vous n'avez pas utilisé un objet **QueryDef** pour créer cet objet **Recordset**, une erreur se produit. Vous devez d'abord ouvrir un objet **Recordset** avec la méthode **OpenRecordset** avant d'utiliser la méthode **CopyQueryDef**.

Cette méthode est utile lorsque vous créez un objet **Recordset** à partir d'un objet **QueryDef**, que vous passez l'objet **Recordset** à une fonction et que la fonction doit recréer l'équivalent SQL de la requête, par exemple pour la modifier.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **CopyQueryDef** pour créer une copie d'un objet **QueryDef** à partir d'un objet **Recordset** existant et modifie la copie en ajoutant une clause à la propriété SQL. Lorsque vous créez un objet **QueryDef** permanent, les espaces, les points-virgules ou les sauts de ligne peuvent être ajoutés à la propriété SQL ; ces caractères supplémentaires doivent être supprimés avant de pouvoir attacher de nouvelles clauses à l'instruction SQL.

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

Cet exemple illustre une utilisation possible de CopyQueryNew().

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

