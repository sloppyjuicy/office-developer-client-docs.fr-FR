---
title: Méthode QueryDef.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 55a3f8a345ffa6669ef721395be4cb1286f2696b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997391"
---
# <a name="querydefexecute-method-dao"></a><span data-ttu-id="16221-102">Méthode QueryDef.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="16221-102">QueryDef.Execute method (DAO)</span></span>

<span data-ttu-id="16221-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16221-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16221-104">Exécute une instruction SQL au niveau de l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="16221-104">Executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="16221-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16221-105">Syntax</span></span>

<span data-ttu-id="16221-106">*expression* . Exécuter (***Options***)</span><span class="sxs-lookup"><span data-stu-id="16221-106">*expression* .Execute(***Options***)</span></span>

<span data-ttu-id="16221-107">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="16221-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="16221-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16221-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16221-109">Name</span><span class="sxs-lookup"><span data-stu-id="16221-109">Name</span></span></p></th>
<th><p><span data-ttu-id="16221-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="16221-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="16221-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="16221-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="16221-112">Description</span><span class="sxs-lookup"><span data-stu-id="16221-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16221-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="16221-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="16221-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="16221-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="16221-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="16221-115"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="16221-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="16221-116">Remarks</span></span>

<span data-ttu-id="16221-117">Vous pouvez utiliser l’une des constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** suivantes pour les Options.</span><span class="sxs-lookup"><span data-stu-id="16221-117">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for Options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16221-118">Constant</span><span class="sxs-lookup"><span data-stu-id="16221-118">Constant</span></span></p></th>
<th><p><span data-ttu-id="16221-119">Description</span><span class="sxs-lookup"><span data-stu-id="16221-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16221-120"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="16221-120"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-121">Refuse les autorisations d'accès en écriture aux autres utilisateurs (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="16221-121">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16221-122"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="16221-122"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-123">(Option par défaut) Exécute les mises à jour incohérentes (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="16221-123">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16221-124"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="16221-124"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-125">Exécute les mises à jour cohérentes (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="16221-125">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16221-126"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="16221-126"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-p101">Exécute une requête SQL directe. Si elle est définie, cette option transmet l'instruction SQL à une base de données ODBC pour traitement (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="16221-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16221-129"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="16221-129"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-130">Annule les mises à jour si une erreur se produit (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="16221-130">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16221-131"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="16221-131"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-132">Génère une erreur d'exécution si un autre utilisateur modifie les données que vous-même êtes en train de modifier (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="16221-132">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16221-133"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="16221-133"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-134">Exécute la requête en mode asynchrone (objets ODBCDirect Connection et QueryDef uniquement).</span><span class="sxs-lookup"><span data-stu-id="16221-134">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16221-135"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="16221-135"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="16221-136">Exécute l'instruction sans appeler préalablement la fonction API ODBC SQLPrepare (objets ODBCDirect Connection et QueryDef uniquement).</span><span class="sxs-lookup"><span data-stu-id="16221-136">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="16221-p102">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="16221-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="16221-p103">[!REMARQUE] Les constantes **dbConsistent** et **dbInconsistent** s'excluent mutuellement. Vous pouvez utiliser l'une ou l'autre dans une instance donnée d' **OpenRecordset**, mais pas les deux à la fois. L'utilisation simultanée de **dbConsistent** et **dbInconsistent** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="16221-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="16221-p104">Utilisez la propriété **[RecordsAffected](querydef-recordsaffected-property-dao.md)** de l'objet **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** pour déterminer le nombre d'enregistrements affectés par la méthode **[Execute](querydef-execute-method-dao.md)** la plus récente. Par exemple, **RecordsAffected** contient le nombre d'enregistrements supprimés, mis à jour ou insérés lors de l'exécution d'une requête Action. Lorsque vous utilisez la méthode **Execute** pour exécuter une requête, la valeur de la propriété **RecordsAffected** de l'objet **QueryDef** correspond au nombre d'enregistrements affectés.</span><span class="sxs-lookup"><span data-stu-id="16221-p104">Use the **[RecordsAffected](querydef-recordsaffected-property-dao.md)** property of the **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)**, or **[QueryDef](querydef-object-dao.md)** object to determine the number of records affected by the most recent **[Execute](querydef-execute-method-dao.md)** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="16221-p105">Dans un espace de travail Microsoft Access, si vous fournissez une instruction SQL correcte du point de vue syntaxique et que vous détenez les autorisations appropriées, la méthode **Execute** n'échouera pas, même si aucune ligne ne peut être modifiée ou supprimée. Par conséquent, utilisez toujours l'option **dbFailOnError** lorsque vous vous servez de la méthode **Execute** pour exécuter une requête Mise à jour ou Suppression. Cette option génère une erreur d'exécution et annule toutes les modifications accomplies dans le cas où certains enregistrements affectés sont verrouillés et ne peuvent pas être mis à jour ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="16221-p105">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="16221-p106">Dans les versions antérieures du moteur de base de données Microsoft Jet, les instructions SQL étaient automatiquement incorporées dans des transactions implicites. Si une partie d'une instruction exécutée avec **dbFailOnError** échouait, l'instruction était entièrement annulée. Dans un souci d'amélioration des performances, ces transactions implicites ont été supprimées à compter de la version 3.5. Si vous mettez à jour un code DAO plus ancien, envisagez l'utilisation de transactions explicites autour des instructions **Execute**.</span><span class="sxs-lookup"><span data-stu-id="16221-p106">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="16221-p107">Pour des performances optimales dans un espace de travail Microsoft Access, plus particulièrement dans un environnement multi-utilisateur, imbriquez la méthode **Execute** à l'intérieur d'une transaction. Appliquez la méthode **[BeginTrans](workspace-begintrans-method-dao.md)** à l'objet **[Workspace](workspace-object-dao.md)** actif, utilisez ensuite la méthode **Execute**, puis terminez la transaction en appliquant la méthode **[CommitTrans](workspace-committrans-method-dao.md)** à l'objet **Workspace**. Cette procédure a pour effet d'enregistrer les modifications sur disque et de libérer les verrous placés pendant l'exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="16221-p107">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **[BeginTrans](workspace-begintrans-method-dao.md)** method on the current **[Workspace](workspace-object-dao.md)** object, then use the **Execute** method, and complete the transaction by using the **[CommitTrans](workspace-committrans-method-dao.md)** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="16221-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="16221-155">Example</span></span>

<span data-ttu-id="16221-p108">Cet exemple illustre l'exécution de la méthode **Execute** à partir d'un objet **QueryDef** et d'un objet **Database**. Les procédures ExecuteQueryDef et PrintOutput sont nécessaires à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="16221-p108">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

```vb
    Sub ExecuteX() 
     
       Dim dbsNorthwind As Database 
       Dim strSQLChange As String 
       Dim strSQLRestore As String 
       Dim qdfChange As QueryDef 
       Dim rstEmployees As Recordset 
       Dim errLoop As Error 
     
       ' Define two SQL statements for action queries. 
       strSQLChange = "UPDATE Employees SET Country = " & _ 
          "'United States' WHERE Country = 'USA'" 
       strSQLRestore = "UPDATE Employees SET Country = " & _ 
          "'USA' WHERE Country = 'United States'" 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Create temporary QueryDef object. 
       Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
          strSQLChange) 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "SELECT LastName, Country FROM Employees", _ 
          dbOpenForwardOnly) 
     
       ' Print report of original data. 
       Debug.Print _ 
          "Data in Employees table before executing the query" 
       PrintOutput rstEmployees 
        
       ' Run temporary QueryDef. 
       ExecuteQueryDef qdfChange, rstEmployees 
        
       ' Print report of new data. 
       Debug.Print _ 
          "Data in Employees table after executing the query" 
       PrintOutput rstEmployees 
     
       ' Run action query to restore data. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       dbsNorthwind.Execute strSQLRestore, dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstEmployees.Requery 
     
       ' Print report of restored data. 
       Debug.Print "Data after executing the query " & _ 
          "to restore the original information" 
       PrintOutput rstEmployees 
     
       rstEmployees.Close 
        
       Exit Sub 
        
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
       rstTemp As Recordset) 
     
       Dim errLoop As Error 
        
       ' Run the specified QueryDef object. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       qdfTemp.Execute dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstTemp.Requery 
        
       Exit Sub 
     
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
       ' Enumerate Recordset. 
       Do While Not rstTemp.EOF 
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

<span data-ttu-id="16221-p109">L'exemple suivant montre comment exécuter une requête avec paramètres. La collection Parameters est utilisée pour définir le paramètre Organization de la requête myActionQuery avant l'exécution de cette dernière.</span><span class="sxs-lookup"><span data-stu-id="16221-p109">The following example shows how to execute a parameter query. The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="16221-160">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="16221-160">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
