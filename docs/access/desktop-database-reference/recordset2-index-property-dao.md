---
title: Recordset2.Index, propriété (DAO)
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
# <a name="recordset2index-property-dao"></a><span data-ttu-id="d6264-102">Recordset2.Index, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="d6264-102">Recordset2.Index property (DAO)</span></span>

<span data-ttu-id="d6264-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6264-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6264-104">Définit ou renvoie une valeur qui indique le nom de l’objet **[Index](index-object-dao.md)** actuel dans un type de tableau **[Recordset](recordset-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="d6264-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6264-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6264-105">Syntax</span></span>

<span data-ttu-id="d6264-106">*expression* .Index</span><span class="sxs-lookup"><span data-stu-id="d6264-106">*expression* .Index</span></span>

<span data-ttu-id="d6264-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="d6264-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6264-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6264-108">Remarks</span></span>

<span data-ttu-id="d6264-p101">Les enregistrements de tables de base ne sont pas stockés dans un ordre particulier. Définir le **Index** propriété modifie l’ordre des enregistrements renvoyés à partir de la base de données ; il n’affecte pas l’ordre dans lequel les enregistrements sont stockés.</span><span class="sxs-lookup"><span data-stu-id="d6264-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="d6264-p102">La valeur **Index** objet doit déjà être défini. Si vous définissez la **Index** propriété pour un **Index** objet n’existe pas ou si le **Index** propriété n’est pas définie lorsque vous utilisez le **[ Avance rapide](recordset2-seek-method-dao.md)** méthode, une erreur récupérable se produit.</span><span class="sxs-lookup"><span data-stu-id="d6264-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset2-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="d6264-113">Examiner la **index** collection d’un **TableDef** objet pour déterminer les éléments **Index** objets sont disponibles pour le type de table **jeu d’enregistrements** les objets créés à partir de qui **TableDef** objet.</span><span class="sxs-lookup"><span data-stu-id="d6264-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="d6264-114">Vous pouvez créer un nouvel index de la table en créant une nouvelle **Index** objet définissant ses propriétés, en ajoutant le **index** ensemble de sous-jacents **TableDef** objet et rouvrir le **jeu d’enregistrements** objet.</span><span class="sxs-lookup"><span data-stu-id="d6264-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="d6264-115">Enregistrements renvoyés à partir d’un type de table **jeu d’enregistrements** objet peut être ordonné de façon uniquement par les index définis pour sous-jacents **TableDef** objet.</span><span class="sxs-lookup"><span data-stu-id="d6264-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="d6264-116">Pour trier les enregistrements d’une autre façon, vous pouvez ouvrir un objet **Recordset** de type feuille de réponse dynamique, instantané ou avant uniquement à l’aide d’une instruction SQL avec une clause ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="d6264-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="d6264-p104">Vous ne devez créer d’index pour les tableaux. Avec des tableaux de grande taille, non indexés, accéder à un enregistrement spécifique ou en créant un **jeu d’enregistrements** objet peut prendre un certain temps. Créer des index trop grand nombre en revanche, ralentit la mise à jour, ajouter et supprimer des opérations, car tous les index sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d6264-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="d6264-120">Enregistrements lus à partir de tables sans index sont renvoyés dans aucune séquence particulière.</span><span class="sxs-lookup"><span data-stu-id="d6264-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="d6264-121">Le **[attributs](field-attributes-property-dao.md)** propriété de chaque **[champ](field-object-dao.md)** objet dans le **Index** objet détermine la ordre des enregistrements et par conséquent détermine les techniques d’accès à utiliser pour cet index.</span><span class="sxs-lookup"><span data-stu-id="d6264-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="d6264-122">Un index unique vous permet d’optimiser la recherche des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d6264-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="d6264-123">Les index n'ont aucune incidence sur l'ordre physique d'une table de base. Ils affectent uniquement la procédure d'accès aux enregistrements utilisée par l'objet **Recordset** de type table lors de la sélection d'un index particulier ou de l'ouverture de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d6264-123">Indexes don't affect the physical order of a base tableindexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>

## <a name="example"></a><span data-ttu-id="d6264-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="d6264-124">Example</span></span>

<span data-ttu-id="d6264-125">Cet exemple utilise la propriété **Index** pour définir des ordres d’enregistrements différents pour un objet **Recordset** de type table.</span><span class="sxs-lookup"><span data-stu-id="d6264-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

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

<span data-ttu-id="d6264-126">Cet exemple illustre la méthode **Seek** en autorisant l’utilisateur à rechercher un produit avec un numéro d’identification.</span><span class="sxs-lookup"><span data-stu-id="d6264-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

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
