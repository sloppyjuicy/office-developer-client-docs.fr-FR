---
title: Méthode Database.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c66e6d3297359b3f3584932d8a1faa5dbee0fd7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469573"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="0139e-102">Méthode Database.Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="0139e-102">Database.Execute Method (DAO)</span></span>

<span data-ttu-id="0139e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0139e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0139e-104">Exécute une requête Action ou une instruction SQL sur l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="0139e-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0139e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0139e-105">Syntax</span></span>

<span data-ttu-id="0139e-106">*expression* . Execute (***requête***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="0139e-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="0139e-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="0139e-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0139e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0139e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0139e-109">Name</span><span class="sxs-lookup"><span data-stu-id="0139e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0139e-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="0139e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0139e-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="0139e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0139e-112">Description</span><span class="sxs-lookup"><span data-stu-id="0139e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0139e-113">Query</span><span class="sxs-lookup"><span data-stu-id="0139e-113">Query</span></span></p></td>
<td><p><span data-ttu-id="0139e-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0139e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0139e-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0139e-116">Options</span><span class="sxs-lookup"><span data-stu-id="0139e-116">Options</span></span></p></td>
<td><p><span data-ttu-id="0139e-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="0139e-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="0139e-118"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0139e-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="0139e-119">Remarks</span></span>

<span data-ttu-id="0139e-120">Vous pouvez utiliser l’une des constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** suivantes pour les options.</span><span class="sxs-lookup"><span data-stu-id="0139e-120">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0139e-121">Constant</span><span class="sxs-lookup"><span data-stu-id="0139e-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="0139e-122">Description</span><span class="sxs-lookup"><span data-stu-id="0139e-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0139e-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-124">Refuse les autorisations d'accès en écriture aux autres utilisateurs (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="0139e-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0139e-125"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-126">(Option par défaut) Exécute les mises à jour incohérentes (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="0139e-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0139e-127"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-128">Exécute les mises à jour cohérentes (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="0139e-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0139e-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-p101">Exécute une requête SQL directe. Si elle est définie, cette option transmet l'instruction SQL à une base de données ODBC pour traitement (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="0139e-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0139e-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-133">Annule les mises à jour si une erreur se produit (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="0139e-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0139e-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-135">Génère une erreur d'exécution si un autre utilisateur modifie les données que vous-même êtes en train de modifier (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="0139e-135">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0139e-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-137">Exécute la requête en mode asynchrone (objets ODBCDirect Connection et QueryDef uniquement).</span><span class="sxs-lookup"><span data-stu-id="0139e-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0139e-138"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="0139e-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="0139e-139">Exécute l'instruction sans appeler préalablement la fonction API ODBC SQLPrepare (objets ODBCDirect Connection et QueryDef uniquement).</span><span class="sxs-lookup"><span data-stu-id="0139e-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="0139e-p102">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0139e-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="0139e-p103">[!REMARQUE] Les constantes **dbConsistent** et **dbInconsistent** s'excluent mutuellement. Vous pouvez utiliser l'une ou l'autre, mais jamais les deux en même temps dans une instance donnée d' **OpenRecordset**. L'utilisation de **dbConsistent** et **dbInconsistent** génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="0139e-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="0139e-p104">La méthode **Execute** est valide uniquement pour les requêtes action. Si vous utilisez **Execute** avec un autre type de requête, une erreur est générée. Dans la mesure où une requête Action ne renvoie aucun enregistrement, **Execute** ne renvoie pas d'objet **Recordset**. (L'exécution d'une requête SQL directe dans un espace de travail ODBCDirect ne renvoie pas d'erreur si aucun objet **Recordset** n'est renvoyé.)</span><span class="sxs-lookup"><span data-stu-id="0139e-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="0139e-p105">Utilisez la propriété **RecordsAffected** de l'objet **Connection**, **Database** ou **QueryDef** pour déterminer le nombre d'enregistrements affectés par le dernier appel de la méthode **Execute**. **RecordsAffected** contient, par exemple, le nombre d'enregistrements supprimés, mis à jour ou insérés lors de l'exécution d'une requête Action. Lorsque vous utilisez la méthode **Execute** pour exécuter une requête, la propriété **RecordsAffected** de l'objet **QueryDef** a pour valeur le nombre d'enregistrements affectés.</span><span class="sxs-lookup"><span data-stu-id="0139e-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="0139e-p106">Dans un espace de travail Microsoft Access, si vous fournissez une instruction SQL avec une syntaxe correcte et disposez des autorisations appropriées, la méthode **Execute** n'échoue pas même si aucune ligne n'a pu être modifiée ou supprimée. Par conséquent, utilisez toujours l'option **dbFailOnError** avec la méthode **Execute** pour exécuter une requête Suppression ou Mise à jour. Cette option génère une erreur d'exécution et annule toutes les modifications implémentées si l'un des enregistrements affectés est verrouillé et ne peut être mis à jour, ni supprimé.</span><span class="sxs-lookup"><span data-stu-id="0139e-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="0139e-p107">Dans les versions antérieures du moteur de base de données Microsoft Jet, les instructions SQL étaient automatiquement incorporées dans des transactions implicites. Si une partie d'une instruction exécutée avec **dbFailOnError** échouait, toute l'instruction était annulée. Pour améliorer les performances, ces transactions implicites ont été supprimées à partir de la version 3.5. Si vous mettez à jour un code DAO plus ancien, envisagez d'utiliser des transactions explicites avec les instructions **Execute**.</span><span class="sxs-lookup"><span data-stu-id="0139e-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="0139e-p108">Pour obtenir de meilleures performances dans un espace de travail Microsoft Access, en particulier dans un environnement multi-utilisateur, imbriquez la méthode **Execute** dans une transaction. Utilisez la méthode **BeginTrans** sur l'objet **Workspace** actif, puis utilisez la méthode **Execute** et terminez la transaction en appelant la méthode **CommitTrans** sur l'objet **Workspace**. Cette opération permet d'enregistrer les modifications sur disque et de libérer tous les verrous appliqués pendant l'exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="0139e-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="0139e-162">Exemple</span><span class="sxs-lookup"><span data-stu-id="0139e-162">Example</span></span>

<span data-ttu-id="0139e-p109">Cet exemple illustre l'exécution de la méthode **Execute** à partir d'un objet **QueryDef** et d'un objet **Database**. Les procédures ExecuteQueryDef et PrintOutput sont nécessaires à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0139e-p109">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

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
     Debug.Print " " & rstTemp!LastName & _ 
     ", " & rstTemp!Country 
     rstTemp.MoveNext 
     Loop 
     
    End Sub
```
