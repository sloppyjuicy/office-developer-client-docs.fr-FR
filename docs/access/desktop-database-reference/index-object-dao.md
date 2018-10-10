---
title: Objet index - accès aux données (DAO) des objets
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e45356a09a6a625381ef9a39d40e7349234460ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471010"
---
# <a name="index-object-dao"></a><span data-ttu-id="29539-102">Index Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="29539-102">Index Object (DAO)</span></span>

<span data-ttu-id="29539-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="29539-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="29539-p101">Les objets **Index** déterminent l'ordre des enregistrements accessibles depuis les tables de base de données et indiquent si les enregistrements en double sont acceptés ou pas, ce qui optimise l'accès aux données. Dans le cas d'une base de données externe, les objets **Index** décrivent les index définis pour les tables externes (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="29539-p101">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="29539-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="29539-106">Remarks</span></span>

<span data-ttu-id="29539-p102">Le moteur de base de données Microsoft Access utilise des index pour joindre des tables et crée des objets **[Recordset](recordset-object-dao.md)**. Les index déterminent l'ordre selon lequel les objets **Recordset** de type table renvoient des enregistrements. Toutefois, ils n'indiquent pas l'ordre dans lequel le moteur de base de données Microsoft Access stocke les enregistrements dans la table de base, ni celui dans lequel les autres types d'objet **Recordset** renvoient les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="29539-p102">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects. Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="29539-109">Grâce à un objet **Index**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="29539-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="29539-110">Utiliser la propriété **Required** pour indiquer que les objets **[Field](field-object-dao.md)** de l'index nécessitent des valeurs qui ne sont pas Null, puis utiliser la propriété **IgnoreNulls** pour déterminer si les valeurs Null contiennent des entrées d'index.</span><span class="sxs-lookup"><span data-stu-id="29539-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="29539-111">Utiliser les propriétés **Primary** et **Unique** pour déterminer l'ordre et le caractère unique de l'objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="29539-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="29539-p103">Le moteur de base de données Microsoft Access gère automatiquement tous les index de table de base. Il met à jour les index lorsque vous ajoutez, modifiez ou supprimez des enregistrements de la table de base. Après avoir créé la base de données, utilisez régulièrement la méthode **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** pour actualiser les statistiques relatives à l'index.</span><span class="sxs-lookup"><span data-stu-id="29539-p103">The Microsoft Access database engine maintains all base table indexes automatically. It updates indexes whenever you add, change, or delete records from the base table. Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="29539-p104">Lorsque vous accédez à un objet **Recordset** de type table, vous indiquez l'ordre des enregistrements à l'aide de la propriété **Index** de l'objet. Définissez cette propriété sur le paramètre **Name** d'un objet **Index** existant dans la collection **Indexes**. Cette collection figure dans l'objet **[TableDef](tabledef-object-dao.md)** sous-jacent à l'objet **Recordset** que vous remplissez.</span><span class="sxs-lookup"><span data-stu-id="29539-p104">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection. This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <P><span data-ttu-id="29539-p105">[!REMARQUE] Vous ne devez pas créer d'index pour une table. Toutefois, dans le cas d'une table volumineuse non indexée, l'accès à un enregistrement spécifique ou le traitement de jointures peuvent durer longtemps. Inversement, la présence d'un nombre d'index trop important peut ralentir la mise à jour de la base de données lors de la modification de chaque index de table.</span><span class="sxs-lookup"><span data-stu-id="29539-p105">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time. Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span></P>

<span data-ttu-id="29539-120">La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **Field** de l'index détermine l'ordre des enregistrements renvoyés ainsi que les techniques d'accès à utiliser pour cet index.</span><span class="sxs-lookup"><span data-stu-id="29539-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="29539-p106">Chaque objet **Field** de la collection **Fields** d'un objet **Index** constitue un composant de l'index. Pour définir un nouvel objet **Index**, paramétrez ses propriétés avant de l'ajouter à une collection. L'objet **Index** pourra ainsi être utilisé ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="29539-p106">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index. To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <P><span data-ttu-id="29539-123">[!REMARQUE] Vous ne pouvez modifier le paramètre de propriété <STRONG>Name</STRONG> d'un objet <STRONG>Index</STRONG> que si le paramètre <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> de l'objet conteneur <STRONG>TableDef</STRONG> a la valeur <STRONG>True</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="29539-123">You can modify the <STRONG>Name</STRONG> property setting of an existing <STRONG>Index</STRONG> object only if the <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> property setting of the containing <STRONG>TableDef</STRONG> object is <STRONG>True</STRONG>.</span></span></P>

<span data-ttu-id="29539-p107">Si vous indiquez une clé primaire pour une table, le moteur de base de données Microsoft Access la définit automatiquement comme index primaire. Il s'agit d'un ou plusieurs champs qui identifient de manière unique tous les enregistrements d'une table dans un ordre prédéfini. Le champ d'index primaire devant être unique, le moteur de base de données Microsoft Access attribue automatiquement la valeur **True** à la propriété **Unique** de l'objet **Index**. Si l'index primaire comprend plusieurs champs, chaque champ peut contenir des valeurs en double, mais la combinaison de valeurs de tous les champs indexés doit être unique. Un index primaire est constitué d'une clé correspondant à la table et comprend toujours les mêmes champs que la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="29539-p107">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index. A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**. If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique. A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29539-p108">[!IMPORTANTE] Assurez-vous que les données sont conformes aux attributs du nouvel index. Si l'index impose des valeurs uniques, veillez à ce que les enregistrements de données ne contiennent aucune valeur en double. En effet, le moteur de base de données Microsoft Access ne peut pas créer l'index s'il existe des valeurs en double. Une erreur interceptable se produit lorsque vous tentez d'utiliser la méthode Append sur le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="29539-p108">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="29539-p109">Lors de la création d'une relation qui applique l'intégrité référentielle, le moteur de base de données Microsoft Access crée automatiquement un index à l'aide de la propriété **Foreign**, définie comme clé étrangère dans la table de référence. Une fois une relation de table définie, le moteur de base de données Microsoft Access empêche tout ajout ou toute modification dans la base de données contraire à cette relation. Si vous définissez la propriété **Attributes** de l'objet **[Relation](relation-object-dao.md)** afin d'autoriser les mises à jour en cascade et les suppressions en cascade, le moteur de base de données Microsoft Access met à jour ou supprime automatiquement les enregistrements des tables liées.</span><span class="sxs-lookup"><span data-stu-id="29539-p109">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table. After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship. If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="29539-135">Utilisez la méthode **CreateIndex** sur un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="29539-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="29539-136">Utilisez la méthode **CreateField** sur l'objet **Index** pour créer un objet **Field** pour chaque champ (colonne) à inclure dans l'objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="29539-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="29539-137">Définissez les propriétés **Index** requises.</span><span class="sxs-lookup"><span data-stu-id="29539-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="29539-138">Ajoutez l'objet **Field** à la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="29539-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="29539-139">Ajoutez l'objet **Index** à la collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="29539-139">Append the **Index** object to the **Indexes** collection.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="29539-140">[!REMARQUE] La propriété <STRONG>Clustered</STRONG> est ignorée pour les bases de données qui utilisent le moteur de base de données Microsoft Access, qui ne prend pas en charge les index cluster.</span><span class="sxs-lookup"><span data-stu-id="29539-140">The <STRONG>Clustered</STRONG> property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span></P>



## <a name="example"></a><span data-ttu-id="29539-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="29539-141">Example</span></span>

<span data-ttu-id="29539-p110">Cet exemple crée un nouvel objet **Index**, l'ajoute à la collection **Indexes** de la **TableDef** Employees, puis énumère la collection **Indexes** de la **TableDef**. Enfin, il énumère un objet **Recordset**, d'abord à l'aide de l' **Index** primaire, ensuite à l'aide du nouvel objet **Index**. La procédure IndexOutput est requise pour exécuter cette opération.</span><span class="sxs-lookup"><span data-stu-id="29539-p110">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="29539-p111">Cet exemple utilise la méthode **CreateIndex** pour créer deux nouveaux objets **Index** et les ajouter à la collection **Indexes** de l'objet **TableDef** Employees. Il énumère ensuite la collection **Indexes** de l'objet **TableDef**, la collection **Fields** des nouveaux objets **Index**, et la collection Properties des nouveaux objets **Index**. La fonction CreateIndexOutput est requise pour exécuter cette opération.</span><span class="sxs-lookup"><span data-stu-id="29539-p111">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
