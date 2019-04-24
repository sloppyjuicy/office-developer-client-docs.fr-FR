---
title: Recordset2. index, propriété (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307300"
---
# <a name="recordset2index-property-dao"></a><span data-ttu-id="42188-102">Recordset2. index, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="42188-102">Recordset2.Index property (DAO)</span></span>

<span data-ttu-id="42188-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42188-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42188-104">Définit ou renvoie une valeur qui indique le nom de l'objet **[Index](index-object-dao.md)** actif dans un objet **[Recordset](recordset-object-dao.md)** de type table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="42188-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="42188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42188-105">Syntax</span></span>

<span data-ttu-id="42188-106">*expression* . Évaluer</span><span class="sxs-lookup"><span data-stu-id="42188-106">*expression* .Index</span></span>

<span data-ttu-id="42188-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="42188-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="42188-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="42188-108">Remarks</span></span>

<span data-ttu-id="42188-p101">Les enregistrements des tables de base ne sont pas stockés dans un ordre précis. La définition de la propriété **Index** modifie l'ordre des enregistrements renvoyés par la base de données, elle n'a aucune incidence sur l'ordre en fonction duquel ils sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="42188-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="42188-p102">L'objet **Index** spécifié doit déjà être défini. Si vous attribuez à la propriété **Index** un objet **Index** qui n'existe pas ou si la propriété **Index** n'est pas définie lorsque vous appelez la méthode **[Seek](recordset2-seek-method-dao.md)**, une erreur piégeable se produit.</span><span class="sxs-lookup"><span data-stu-id="42188-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset2-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="42188-113">Examinez la collection **Indexes** d'un objet **TableDef** pour identifier les objets **Index** disponibles pour des objets **Recordset** de type table créés à partir de cet objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="42188-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="42188-114">Pour créer un nouvel index pour la table, créez un objet **Index**, définissez ses propriétés, ajoutez-le à la collection **Indexes** de l'objet **TableDef** sous-jacent puis rouvrez l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="42188-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="42188-115">Les enregistrements renvoyés à partir d'un objet **Recordset** de type table peuvent être uniquement classés en fonction des index définis pour l'objet **TableDef** sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="42188-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="42188-116">Pour trier les enregistrements d'une autre manière, vous pouvez ouvrir un objet Recordset de type feuille de réponse dynamique, instantané \*\*\*\* ou avant uniquement à l'aide d'une instruction SQL avec une clause ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="42188-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="42188-p104">Il n'est pas nécessaire de créer des index pour les tables. Dans le cas de tables volumineuses et non indexées, l'accès à un enregistrement spécifique ou la création d'un objet **Recordset** peut demander du temps. D'autre part, la création d'un nombre excessif d'index ralentit les opérations de mise à jour, d'ajout et de suppression car tous les index sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="42188-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="42188-120">Les enregistrements non indexés et lus à partir de tables sont renvoyés sans ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="42188-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="42188-121">La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** présent dans l'objet **Index** détermine l'ordre des enregistrements et, par conséquent, les techniques d'accès à utiliser pour cet index.</span><span class="sxs-lookup"><span data-stu-id="42188-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="42188-122">Un index unique permet d'optimiser la recherche d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="42188-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="42188-123">Les index n'ont aucune incidence sur l'ordre physique d'une table de base. Ils affectent uniquement la procédure d'accès aux enregistrements utilisée par l'objet **Recordset** de type table lors de la sélection d'un index particulier ou de l'ouverture de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="42188-123">Indexes don't affect the physical order of a base tableindexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>

## <a name="example"></a><span data-ttu-id="42188-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="42188-124">Example</span></span>

<span data-ttu-id="42188-125">Cet exemple utilise la propriété **Index** pour définir plusieurs ordres de tri des enregistrements d'un objet **Recordset** de type table.</span><span class="sxs-lookup"><span data-stu-id="42188-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="42188-126">Cet exemple illustre la méthode **Seek** qui permet à l'utilisateur de rechercher un produit en fonction d'un numéro d'identification.</span><span class="sxs-lookup"><span data-stu-id="42188-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
