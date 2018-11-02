---
title: Propriété QueryDef.Prepare (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f1d587501cb9a3279db055b9eee27d765e002a03
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925939"
---
# <a name="querydefprepare-property-dao"></a>Propriété QueryDef.Prepare (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Préparer

*expression* Variable qui représente un objet **QueryDef** .

## <a name="remarks"></a>Remarques

La propriété **Prepare** permet soit de créer une procédure stockée temporaire à partir de la requête et de l'exécuter ensuite, soit d'exécuter la requête directement. Par défaut, la propriété **Prepare** est définie sur **dbQPrepare**. Toutefois, vous pouvez la définir sur **dbQUnprepare** pour empêcher toute préparation de la requête. Dans ce cas, elle est exécutée à l'aide de l'API **SQLExecDirect**.

La création d'une procédure stockée peut ralentir l'opération initiale, mais augmente les performances de toutes les références ultérieures à la requête. Toutefois, certaines requêtes ne peuvent pas être exécutées sous la forme d'une procédure stockée. Dans ce cas, vous devez définir la propriété **Prepare** sur **dbQUnprepare**.

Si **Prepare** est définie sur **dbQPrepare**, il peut être remplacé lors de la requête est exécutée en définissant l’argument options de la méthode **[Execute](querydef-execute-method-dao.md)** sur **dbExecDirect**.


> [!NOTE]
> <P>[!REMARQUE] L'API <STRONG>SQLPrepare</STRONG> ODBC est invoqué dès que la propriété DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> est définie. Par conséquent, pour améliorer les performances à l'aide de l'option <STRONG>dbQUnprepare</STRONG>, vous devez définir la propriété <STRONG>Prepare</STRONG> avant de définir la propriété <STRONG>SQL</STRONG>.</P>



## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Prepare** pour spécifier qu'une requête doit être exécutée directement plutôt que de passer par la création préalable d'une procédure stockée sur le serveur.

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```

