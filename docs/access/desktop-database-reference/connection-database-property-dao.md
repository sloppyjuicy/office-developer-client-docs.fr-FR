---
title: Connection.Database Property (DAO)
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
ms.openlocfilehash: cb23c07e9949da5fe104df83e9dc9e02c435b19b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887501"
---
# <a name="connectiondatabase-property-dao"></a><span data-ttu-id="522ea-102">Connection.Database Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="522ea-102">Connection.Database Property (DAO)</span></span>


<span data-ttu-id="522ea-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="522ea-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="syntax"></a><span data-ttu-id="522ea-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="522ea-104">Syntax</span></span>

<span data-ttu-id="522ea-105">*expression* . Base de données</span><span class="sxs-lookup"><span data-stu-id="522ea-105">*expression* .Database</span></span>

<span data-ttu-id="522ea-106">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="522ea-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="522ea-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="522ea-107">Remarks</span></span>

<span data-ttu-id="522ea-p101">Pour un objet **[Connection](connection-object-dao.md)**, utilisez la propriété **Database** pour obtenir une référence à un objet **Database** correspondant à l'objet **Connection**. Dans DAO, un objet **Connection** et l'objet **Database** correspondant représentent deux références de variable d'objet différentes au même objet. Grâce à la propriété **Database** d'un objet **Connection** et à la propriété **[Connection](database-connection-property-dao.md)** d'un objet **Database**, il est plus simple de modifier la connexion à une source de données ODBC via le moteur de base de données Microsoft Access afin d'utiliser ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="522ea-p101">On a **[Connection](connection-object-dao.md)** object, use the **Database** property to obtain a reference to a **Database** object that corresponds to the **Connection**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **Database** property of a **Connection** object and the **[Connection](database-connection-property-dao.md)** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

## <a name="example"></a><span data-ttu-id="522ea-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="522ea-111">Example</span></span>

<span data-ttu-id="522ea-112">L'exemple ci-dessous utilise la propriété **Database** pour indiquer comment le code servant à accéder aux données ODBC via le moteur de base de données Microsoft Access peut être converti pour utiliser des objets Connection ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="522ea-112">This example uses the **Database** property to show how code that used to access ODBC data through the Microsoft Access database engine can be converted to use ODBCDirect Connection objects.</span></span>

<span data-ttu-id="522ea-113">La procédure OldDatabaseCode utilise une source de données reliée au moteur de base de données Microsoft Access pour accéder à une base de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="522ea-113">The OldDatabaseCode procedure uses a Microsoft Access database engine-connected data source to access an ODBC database.</span></span>

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

<span data-ttu-id="522ea-p102">L'exemple NewDatabaseCode ouvre un objet **Connection** dans un espace de travail ODBCDirect. Il attribue ensuite la propriété **Database** de l'objet **Connection** à une variable d'objet portant le même nom que la source de données de l'ancienne procédure. Le code ultérieur ne doit être modifié que s'il utilise des fonctionnalités spécifiques des espaces de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="522ea-p102">The NewDatabaseCode example opens a **Connection** object in an ODBCDirect workspace. It then assigns the **Database** property of the **Connection** object to an object variable with the same name as the data source in the old procedure. None of the subsequent code has to be changed as long as it doesn't use any features specific to Microsoft Access workspaces.</span></span>

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

