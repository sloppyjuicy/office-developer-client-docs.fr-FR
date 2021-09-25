---
title: Connection.Database, propriété (DAO)
TOCTitle: Database Property
ms:assetid: cf871353-0ea4-f995-6e0e-812af443daf9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834675(v=office.15)
ms:contentKeyID: 48547809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053581
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: eaca7976e417d61ef8d70f0d60aa2438f89072ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586039"
---
# <a name="connectiondatabase-property-dao"></a>Connection.Database, propriété (DAO)


**S’applique à** : Access 2013, Office 2013



## <a name="syntax"></a>Syntaxe

*expression* . Database

*expression* Variable qui représente un objet **Connection**.

## <a name="remarks"></a>Remarques

Pour un objet **[Connection](connection-object-dao.md)**, utilisez la propriété **Database** pour obtenir une référence à un objet **Database** correspondant à l'objet **Connection**. Dans DAO, un objet **Connection** et l'objet **Database** correspondant représentent deux références de variable d'objet différentes au même objet. Grâce à la propriété **Database** d'un objet **Connection** et à la propriété **[Connection](database-connection-property-dao.md)** d'un objet **Database**, il est plus simple de modifier la connexion à une source de données ODBC via le moteur de base de données Microsoft Access afin d'utiliser ODBCDirect.

## <a name="example"></a>Exemple

L'exemple ci-dessous utilise la propriété **Database** pour indiquer comment le code servant à accéder aux données ODBC via le moteur de base de données Microsoft Access peut être converti pour utiliser des objets Connection ODBCDirect.

La procédure OldDatabaseCode utilise une source de données reliée au moteur de base de données Microsoft Access pour accéder à une base de données ODBC.

```vb
    Sub OldDatabaseCode() 
     
     Dim wrkMain As Workspace 
     Dim dbsPubs As Database 
     Dim prpLoop As Property 
     
     ' Create a Workspace object. 
     Set wrkMain = CreateWorkspace("", "admin", "", dbUseJet) 
     
     ' Open a Database object based on information in 
     ' the connect string. 
     
     'Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set dbsPubs = wrkMain.OpenDatabase("Publishers", _ 
     dbDriverNoPrompt, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Enumerate the Properties collection of the Database 
     ' object. 
     With dbsPubs 
     Debug.Print "Database properties for " & _ 
     .Name & ":" 
     
     On Error Resume Next 
     For Each prpLoop In .Properties 
     If prpLoop.Name = "Connection" Then 
     ' Property actually returns a Connection object. 
     Debug.Print " Connection[.Name] = " & _ 
     .Connection.Name 
     Else 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop 
     End If 
     Next prpLoop 
     On Error GoTo 0 
     
     End With 
     
     dbsPubs.Close 
     wrkMain.Close 
     
    End Sub 
```

L'exemple NewDatabaseCode ouvre un objet **Connection** dans un espace de travail ODBCDirect. Il attribue ensuite la propriété **Database** de l'objet **Connection** à une variable d'objet portant le même nom que la source de données de l'ancienne procédure. Le code ultérieur ne doit être modifié que s'il utilise des fonctionnalités spécifiques des espaces de travail Microsoft Access.

```vb 
Sub NewDatabaseCode() 
 
 Dim wrkMain As Workspace 
 Dim conPubs As Connection 
 Dim dbsPubs As Database 
 Dim prpLoop As Property 
 
 ' Create ODBCDirect Workspace object instead of Microsoft 
 ' Access Workspace object. 
 Set wrkMain = CreateWorkspace("", "admin", "", dbUseODBC) 
 
 ' Open Connection object based on information in 
 ' the connect string. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 ' Assign the Database property to the same object 
 ' variable as in the old code. 
 Set dbsPubs = conPubs.Database 
 
 ' Enumerate the Properties collection of the Database 
 ' object. From this point on, the code is the same as the 
 ' old example. 
 With dbsPubs 
 Debug.Print "Database properties for " & _ 
 .Name & ":" 
 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 .Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 End With 
 
 dbsPubs.Close 
 wrkMain.Close 
 
End Sub 
 
```

