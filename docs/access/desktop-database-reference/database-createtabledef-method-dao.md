---
title: Méthode Database.CreateTableDef (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c986f0a96c14dac8a9ee4f3c7fded5a049fa451e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718489"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="3f0fc-102">Méthode Database.CreateTableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f0fc-102">Database.CreateTableDef method (DAO)</span></span>

<span data-ttu-id="3f0fc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f0fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f0fc-p101">Crée un objet **[TableDef](tabledef-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3f0fc-p101">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f0fc-106">Syntax</span></span>

<span data-ttu-id="3f0fc-107">*expression* . CreateTableDef (***nom***, ***attributs***, ***SourceTableName***, ***connecter***)</span><span class="sxs-lookup"><span data-stu-id="3f0fc-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span></span>

<span data-ttu-id="3f0fc-108">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="3f0fc-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f0fc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f0fc-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f0fc-110">Nom</span><span class="sxs-lookup"><span data-stu-id="3f0fc-110">Name</span></span></p></th>
<th><p><span data-ttu-id="3f0fc-111">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="3f0fc-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3f0fc-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="3f0fc-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="3f0fc-113">Description</span><span class="sxs-lookup"><span data-stu-id="3f0fc-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f0fc-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="3f0fc-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-115">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3f0fc-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f0fc-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f0fc-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-p102"><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>TableDef</strong>. Consultez la propriété <strong><a href="tabledef-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms d’objets <strong>TableDef</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f0fc-119"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="3f0fc-119"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3f0fc-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f0fc-121"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="3f0fc-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-p103">Constante ou combinaison de constantes spécifiant une ou plusieurs caractéristiques du nouvel objet <strong>TableDef</strong>. Pour plus d'informations, consultez la propriété <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="3f0fc-p103">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f0fc-124"><em>SourceTableName</em></span><span class="sxs-lookup"><span data-stu-id="3f0fc-124"><em>SourceTableName</em></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3f0fc-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f0fc-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f0fc-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-p104"><strong>Variant</strong> (sous-type <strong>String</strong>) qui comprend le nom d’une table d’une base de données externe représentant la source des données d’origine. La chaîne source devient la valeur affectée à la propriété <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> du nouvel objet <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data. The source string becomes the <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f0fc-129"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="3f0fc-129"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-130">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3f0fc-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f0fc-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f0fc-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f0fc-p105"><strong>Variant</strong> (sous-type <strong>String</strong>) contenant des informations sur la source d’une base de données ouverte, une base de données utilisée dans une requête directe ou une table liée. Consultez la propriété <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> pour plus d’informations sur les chaînes de connexion valides.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-p105">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table. See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="3f0fc-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f0fc-134">Return value</span></span>

<span data-ttu-id="3f0fc-135">TableDef</span><span class="sxs-lookup"><span data-stu-id="3f0fc-135">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="3f0fc-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f0fc-136">Remarks</span></span>

<span data-ttu-id="3f0fc-p106">Si vous omettez un ou plusieurs arguments facultatifs avec la méthode **CreateTableDef**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou redéfinir la propriété correspondante avant d'ajouter le nouvel objet à la collection. Après l'ajout de l'objet, il est toujours possible de modifier certaines de ses propriétés. Pour plus d'informations, consultez les rubriques des différentes propriétés.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-p106">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its properties. See the individual property topics for more details.</span></span>

<span data-ttu-id="3f0fc-140">Si le nom fait référence à un objet qui est déjà membre de la collection, ou si vous spécifiez une propriété non valide dans l’objet **TableDef** ou **[Field](field-object-dao.md)** que vous ajoutez, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](tabledefs-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="3f0fc-140">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or **[Field](field-object-dao.md)** object you're appending, a run-time error occurs when you use the **[Append](tabledefs-append-method-dao.md)** method.</span></span> <span data-ttu-id="3f0fc-141">En outre, vous ne pouvez pas ajouter d'objet **TableDef** à la collection **TableDefs** avant d'avoir défini au moins un objet **Field** pour l'objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-141">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="3f0fc-142">Pour supprimer un objet **TableDef** de la collection **[TableDefs](tabledefs-collection-dao.md)**, appelez la méthode **[Delete](tabledefs-delete-method-dao.md)** sur la collection.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-142">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="3f0fc-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f0fc-143">Example</span></span>

<span data-ttu-id="3f0fc-144">Cet exemple crée un objet **TableDef** dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-144">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="3f0fc-p108">Cet exemple utilise les méthodes **CreateTableDef** et **FillCache** ainsi que les propriétés **CacheSize**, **CacheStart** et **SourceTableName** pour énumérer deux fois les enregistrements dans une table liée. Ensuite, il énumère également deux fois les enregistrements avec un cache de 50 enregistrements. Enfin, il affiche les statistiques de performance pour les deux exécutions, avec et sans mise en cache, dans la table liée.</span><span class="sxs-lookup"><span data-stu-id="3f0fc-p108">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
