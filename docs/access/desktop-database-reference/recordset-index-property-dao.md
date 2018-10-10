---
title: Recordset.Index Property (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 01a19fd621d8124616872bebc54c6ac9482ffe08
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472023"
---
# <a name="recordsetindex-property-dao"></a><span data-ttu-id="fb849-102">Recordset.Index Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb849-102">Recordset.Index Property (DAO)</span></span>

<span data-ttu-id="fb849-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb849-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fb849-104">Définit ou renvoie une valeur qui indique le nom de l'objet **[Index](index-object-dao.md)** actif d'un objet **[Recordset](recordset-object-dao.md)** de type table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="fb849-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb849-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb849-105">Syntax</span></span>

<span data-ttu-id="fb849-106">*expression* . Index</span><span class="sxs-lookup"><span data-stu-id="fb849-106">*expression* .Index</span></span>

<span data-ttu-id="fb849-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="fb849-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb849-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb849-108">Remarks</span></span>

<span data-ttu-id="fb849-p101">Les enregistrements des tables de base ne sont stockés dans aucun ordre particulier. Le fait de définir la propriété **Index** modifie l'ordre des enregistrements renvoyés de la base de données ; cela n'affecte par l'ordre dans lequel les enregistrements sont stockés.</span><span class="sxs-lookup"><span data-stu-id="fb849-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="fb849-p102">L'objet **Index** spécifié doit déjà être défini. Si vous définissez la propriété **Index** d'un objet **Index** qui n'existe pas ou si la propriété **Index** n'est pas définie lorsque vous utilisez la méthode **[Seek](recordset-seek-method-dao.md)**, une erreur capturable survient.</span><span class="sxs-lookup"><span data-stu-id="fb849-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="fb849-113">Examinez la collection **Indexes** d'un objet **TableDef** pour déterminer les objets **Index** disponibles pour les objets **Recordset** de type table créés à partir de cet objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="fb849-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="fb849-114">Vous pouvez créer un nouvel index pour la table en créant un nouvel objet **Index**, définissant ses propriétés, l'ajoutant à la collection **Indexes** de l'objet **TableDef** sous-jacent et en rouvrant l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fb849-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="fb849-115">Les enregistrements renvoyés d'un objet **Recordset** de type table peuvent être classés uniquement par les index définis pour l'objet **TableDef** sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="fb849-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="fb849-116">Pour trier les enregistrements d’une autre façon, vous pouvez ouvrir un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique à l’aide d’une instruction SQL avec une clause ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="fb849-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> - <span data-ttu-id="fb849-p104">Vous n'avez pas à créer d'index pour les tables. Avec des grandes tables non indexées, l'accès à un enregistrement spécifique ou la création d'un objet **Recordset** peut prendre du temps. Toutefois, la création d'un nombre trop important d'index ralentit les opérations de mise à jour, d'ajout et de suppression car tous les index sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fb849-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="fb849-120">Les enregistrements lus à partir des tables non indexées sont retournés sans ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="fb849-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="fb849-121">La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** de l'objet **Index** détermine l'ordre des enregistrements et, par conséquent, les techniques d'accès à utiliser pour cet index.</span><span class="sxs-lookup"><span data-stu-id="fb849-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="fb849-122">Un index unique permet d'optimiser la recherche d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="fb849-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="fb849-123">Index n’affectent pas l’ordre physique d’une table de base, une incidence sur les index uniquement la manière dont les enregistrements sont accessibles par l’objet **Recordset** de type table lorsqu’un index particulier est choisi ou lorsque **l’objet Recordset** est ouvert.</span><span class="sxs-lookup"><span data-stu-id="fb849-123">Indexes don't affect the physical order of a base table, indexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>


## <a name="example"></a><span data-ttu-id="fb849-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb849-124">Example</span></span>

<span data-ttu-id="fb849-125">Cet exemple utilise la propriété **Index** pour définir des ordres d'enregistrements différents pour un objet **Recordset** de type table.</span><span class="sxs-lookup"><span data-stu-id="fb849-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
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

<span data-ttu-id="fb849-126">Cet exemple démontre la méthode **Seek** en permettant à l'utilisateur de rechercher un produit en fonction d'un numéro d'identification.</span><span class="sxs-lookup"><span data-stu-id="fb849-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
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

<br/>

<span data-ttu-id="fb849-127">L'exemple suivant montre comment utiliser la méthode Seek pour rechercher un enregistrement dans une table liée.</span><span class="sxs-lookup"><span data-stu-id="fb849-127">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="fb849-128">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="fb849-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
