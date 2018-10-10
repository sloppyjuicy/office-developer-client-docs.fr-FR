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
ms.openlocfilehash: d3438392976051f744f3a449b02cce6aa1c23e8b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470097"
---
# <a name="querydefexecute-method-dao"></a>Méthode QueryDef.Execute (DAO)

**S’applique à**: Access 2013 | Office 2013

Exécute une instruction SQL au niveau de l'objet spécifié.

## <a name="syntax"></a>Syntaxe

*expression* . Exécuter (***Options***)

*expression* Variable qui représente un objet **QueryDef** .

### <a name="parameters"></a>Paramètres

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
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’une des constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** suivantes pour les Options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Refuse les autorisations d'accès en écriture aux autres utilisateurs (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Option par défaut) Exécute les mises à jour incohérentes (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Exécute les mises à jour cohérentes (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Exécute une requête SQL directe. Si elle est définie, cette option transmet l'instruction SQL à une base de données ODBC pour traitement (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Annule les mises à jour si une erreur se produit (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Génère une erreur d'exécution si un autre utilisateur modifie les données que vous-même êtes en train de modifier (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Exécute la requête en mode asynchrone (objets ODBCDirect Connection et QueryDef uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Exécute l'instruction sans appeler préalablement la fonction API ODBC SQLPrepare (objets ODBCDirect Connection et QueryDef uniquement).</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.

> [!NOTE]
> [!REMARQUE] Les constantes **dbConsistent** et **dbInconsistent** s'excluent mutuellement. Vous pouvez utiliser l'une ou l'autre dans une instance donnée d' **OpenRecordset**, mais pas les deux à la fois. L'utilisation simultanée de **dbConsistent** et **dbInconsistent** entraîne une erreur.

Utilisez la propriété **[RecordsAffected](querydef-recordsaffected-property-dao.md)** de l'objet **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** pour déterminer le nombre d'enregistrements affectés par la méthode **[Execute](querydef-execute-method-dao.md)** la plus récente. Par exemple, **RecordsAffected** contient le nombre d'enregistrements supprimés, mis à jour ou insérés lors de l'exécution d'une requête Action. Lorsque vous utilisez la méthode **Execute** pour exécuter une requête, la valeur de la propriété **RecordsAffected** de l'objet **QueryDef** correspond au nombre d'enregistrements affectés.

Dans un espace de travail Microsoft Access, si vous fournissez une instruction SQL correcte du point de vue syntaxique et que vous détenez les autorisations appropriées, la méthode **Execute** n'échouera pas, même si aucune ligne ne peut être modifiée ou supprimée. Par conséquent, utilisez toujours l'option **dbFailOnError** lorsque vous vous servez de la méthode **Execute** pour exécuter une requête Mise à jour ou Suppression. Cette option génère une erreur d'exécution et annule toutes les modifications accomplies dans le cas où certains enregistrements affectés sont verrouillés et ne peuvent pas être mis à jour ou supprimés.

Dans les versions antérieures du moteur de base de données Microsoft Jet, les instructions SQL étaient automatiquement incorporées dans des transactions implicites. Si une partie d'une instruction exécutée avec **dbFailOnError** échouait, l'instruction était entièrement annulée. Dans un souci d'amélioration des performances, ces transactions implicites ont été supprimées à compter de la version 3.5. Si vous mettez à jour un code DAO plus ancien, envisagez l'utilisation de transactions explicites autour des instructions **Execute**.

Pour des performances optimales dans un espace de travail Microsoft Access, plus particulièrement dans un environnement multi-utilisateur, imbriquez la méthode **Execute** à l'intérieur d'une transaction. Appliquez la méthode **[BeginTrans](workspace-begintrans-method-dao.md)** à l'objet **[Workspace](workspace-object-dao.md)** actif, utilisez ensuite la méthode **Execute**, puis terminez la transaction en appliquant la méthode **[CommitTrans](workspace-committrans-method-dao.md)** à l'objet **Workspace**. Cette procédure a pour effet d'enregistrer les modifications sur disque et de libérer les verrous placés pendant l'exécution de la requête.

## <a name="example"></a>Exemple

Cet exemple illustre l'exécution de la méthode **Execute** à partir d'un objet **QueryDef** et d'un objet **Database**. Les procédures ExecuteQueryDef et PrintOutput sont nécessaires à l'exécution de cette procédure.

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

L'exemple suivant montre comment exécuter une requête avec paramètres. La collection Parameters est utilisée pour définir le paramètre Organization de la requête myActionQuery avant l'exécution de cette dernière.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
