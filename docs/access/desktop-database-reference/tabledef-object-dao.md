---
title: Objet TableDef (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef0a7c167321a45249fb022e0987a5f8d6364ea0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469123"
---
# <a name="tabledef-object-dao"></a><span data-ttu-id="e2d64-102">Objet TableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="e2d64-102">TableDef Object (DAO)</span></span>

<span data-ttu-id="e2d64-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2d64-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e2d64-104">Un objet **TableDef** représente la définition stockée d'une table de base ou d'une table liée (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="e2d64-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d64-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2d64-105">Remarks</span></span>

<span data-ttu-id="e2d64-p101">Vous manipulez une définition de table à l'aide d'un objet **TableDef**, de ses méthodes et de ses propriétés. Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e2d64-p101">You manipulate a table definition using a **TableDef** object and its methods and properties. For example, you can:</span></span>

- <span data-ttu-id="e2d64-108">Examiner la structure de champ et d'index d'une table locale, liée ou externe dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="e2d64-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="e2d64-109">Utiliser les propriétés **Connect** et **SourceTableName** pour définir ou renvoyer des informations sur les tables liées et utiliser la méthode **RefreshLink** pour mettre à jour les connexions aux tables liées.</span><span class="sxs-lookup"><span data-stu-id="e2d64-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="e2d64-110">Utiliser les propriétés **ValidationRule** et **ValidationText** pour définir ou renvoyer les conditions de validation.</span><span class="sxs-lookup"><span data-stu-id="e2d64-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="e2d64-111">Utilisez la méthode **OpenRecordset** pour créer une table, feuille de réponse dynamique, dynamique, instantané ou objet **Recordset** de type avant uniquement, en fonction de la définition de table.</span><span class="sxs-lookup"><span data-stu-id="e2d64-111">Use the **OpenRecordset** method to create a table–, dynaset–, dynamic–, snapshot–, or forward–only–type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="e2d64-112">Pour les tables de base, la propriété **RecordCount** contient le nombre d'enregistrements dans la table de base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e2d64-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="e2d64-113">Tables liées, **la propriété RecordCount** est toujours -1.</span><span class="sxs-lookup"><span data-stu-id="e2d64-113">For linked tables, the **RecordCount** property setting is always –1.</span></span>

<span data-ttu-id="e2d64-114">Pour créer un objet **TableDef**, utilisez la méthode **[CreateTableDef](database-createtabledef-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="e2d64-115">Pour ajouter un champ à une table</span><span class="sxs-lookup"><span data-stu-id="e2d64-115">To add a field to a table</span></span>

1.  <span data-ttu-id="e2d64-116">Assurez-vous que les objets **[Recordset](recordset-object-dao.md)** basés sur la table sont tous fermés.</span><span class="sxs-lookup"><span data-stu-id="e2d64-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="e2d64-117">Utilisez la méthode **CreateField** pour créer une variable d'objet **Field** et définir ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2d64-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="e2d64-118">Utilisez la méthode **Append** pour ajouter l'objet **Field** à la collection **Fields** de l'objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="e2d64-119">Vous pouvez supprimer un objet **Field** à partir d'une collection **TableDefs** si aucun index ne lui est attribué, mais vous perdrez les données du champ.</span><span class="sxs-lookup"><span data-stu-id="e2d64-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="e2d64-120">Pour créer une table prête pour de nouveaux enregistrements dans une base de données</span><span class="sxs-lookup"><span data-stu-id="e2d64-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="e2d64-121">Utilisez la méthode **CreateTableDef** pour créer un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="e2d64-122">Définissez ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2d64-122">Set its properties.</span></span>

3.  <span data-ttu-id="e2d64-123">Pour chaque champ de la table, utilisez la méthode **CreateField** pour créer une variable d'objet **Field** et définir ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2d64-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="e2d64-124">Utilisez la méthode **Append** pour ajouter les champs à la collection **Fields** de l'objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="e2d64-125">Utilisez la méthode **Append** pour ajouter le nouvel objet **TableDef** à la collection **TableDefs** de l'objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="e2d64-126">Une table liée est connectée à la base de données via les propriétés **SourceTableName** et **Connect** de l'objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="e2d64-127">Pour lier une table à une base de données</span><span class="sxs-lookup"><span data-stu-id="e2d64-127">To link a table to a database</span></span>

1.  <span data-ttu-id="e2d64-128">Utilisez la méthode **CreateTableDef** pour créer un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="e2d64-129">Définissez les propriétés **Connect** et **SourceTableName** (et éventuellement, la propriété **Attributes** ).</span><span class="sxs-lookup"><span data-stu-id="e2d64-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="e2d64-130">Utilisez la méthode **Append** pour ajouter cet objet à la collection **TableDefs** d'un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="e2d64-131">Pour faire référence à un objet **TableDef** dans une collection par son nombre ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2d64-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="e2d64-132">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="e2d64-132">**TableDefs**(0)</span></span>

<span data-ttu-id="e2d64-133">**TableDefs** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="e2d64-133">**TableDefs**("name")</span></span>

<span data-ttu-id="e2d64-134">**TableDefs**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="e2d64-134">**TableDefs**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="e2d64-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="e2d64-135">Example</span></span>

<span data-ttu-id="e2d64-p103">Cet exemple crée un objet **TableDef** et l'ajoute à la collection **TableDefs** de l'objet de la base de données Northwind. Il énumère ensuite les collections **TableDefs** et **Properties** du nouvel objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e2d64-p103">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="e2d64-138">Cet exemple crée un objet **TableDef** dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="e2d64-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

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
         If prpLoop <> "" Then Debug.Print "  " & _ 
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
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

<span data-ttu-id="e2d64-p104">L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="e2d64-p104">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="e2d64-142">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e2d64-142">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
