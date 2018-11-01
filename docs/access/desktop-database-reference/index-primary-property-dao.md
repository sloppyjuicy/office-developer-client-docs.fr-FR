---
title: Index.Primary Property (DAO)
TOCTitle: Primary Property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
ms.openlocfilehash: efaf00dc54068c6ce7c2991613b9485bcbdf41c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891239"
---
# <a name="indexprimary-property-dao"></a><span data-ttu-id="d0adf-102">Index.Primary Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d0adf-102">Index.Primary Property (DAO)</span></span>


<span data-ttu-id="d0adf-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0adf-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d0adf-104">Définit ou renvoie une valeur qui indique si un objet **[Index](index-object-dao.md)** représente un index de clé primaire pour une table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="d0adf-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a primary key index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0adf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0adf-105">Syntax</span></span>

<span data-ttu-id="d0adf-106">*expression* . Principal</span><span class="sxs-lookup"><span data-stu-id="d0adf-106">*expression* .Primary</span></span>

<span data-ttu-id="d0adf-107">*expression* Variable qui représente un objet **Index** .</span><span class="sxs-lookup"><span data-stu-id="d0adf-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0adf-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0adf-108">Remarks</span></span>

<span data-ttu-id="d0adf-p101">Le paramètre de propriété **Primary** est en lecture/écriture pour un nouvel objet **Index** par encore ajouté à une collection et en lecture seule pour un objet **Index** existant dans une collection **[Indexes](indexes-collection-dao.md)**. Si l'objet **Index** est ajouté à l'objet **[TableDef](tabledef-object-dao.md)** mais que l'objet **TableDef** n'est pas ajouté à la collection **[TableDefs](tabledefs-collection-dao.md)**, la propriété **Index** est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d0adf-p101">The **Primary** property setting is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection. If the **Index** object is appended to the **[TableDef](tabledef-object-dao.md)** object but the **TableDef** object isn't appended to the **[TableDefs](tabledefs-collection-dao.md)** collection, the **Index** property is read/write.</span></span>

<span data-ttu-id="d0adf-p102">Un index de clé primaire consiste en un ou plusieurs champs qui identifient de manière unique tous les enregistrements d'une table dans un ordre prédéfini. Étant donné que le champ d'index doit être unique, la propriété **[Unique](index-unique-property-dao.md)** de l'objet **Index** est définie sur **True**. Si l'index de clé primaire est constitué de plusieurs champs, chaque champ peut contenir des valeurs dupliquées, mais chaque combinaison de valeurs de tous les champs indexés doit être unique. Un index de clé primaire est constitué d'une clé pour la table et renferme généralement les mêmes champs que la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="d0adf-p102">A primary key index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the index field must be unique, the **[Unique](index-unique-property-dao.md)** property of the **Index** object is set to **True**. If the primary key index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique. A primary key index consists of a key for the table and usually contains the same fields as the primary key.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d0adf-p103">[!REMARQUE] La création d'index n'est pas obligatoire pour les tables, mais l'accès à un enregistrement spécifique dans des grandes tables non indexées peut prendre beaucoup de temps. La propriété <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> de chaque objet <STRONG><A href="field-object-dao.md">Field</A></STRONG> de l'objet <STRONG>Index</STRONG> détermine l'ordre des enregistrements et, par conséquent, les techniques d'accès à utiliser pour cet index. Lorsque vous créez une nouvelle table dans votre base de données, il est recommandé de créer un index sur un ou plusieurs champs qui identifie chaque enregistrement de manière unique, puis de définir la propriété <STRONG>Primary</STRONG> de l'objet <STRONG>Index</STRONG> sur <STRONG>True</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d0adf-p103">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time. The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that index. When you create a new table in your database, it's a good idea to create an index on one or more fields that uniquely identify each record, and then set the <STRONG>Primary</STRONG> property of the <STRONG>Index</STRONG> object to <STRONG>True</STRONG>.</span></span></P>



<span data-ttu-id="d0adf-118">Lorsque vous définissez une clé primaire pour une table, la clé primaire est automatiquement définie comme index de clé primaire de la table.</span><span class="sxs-lookup"><span data-stu-id="d0adf-118">When you set a primary key for a table, the primary key is automatically defined as the primary key index for the table.</span></span>

## <a name="example"></a><span data-ttu-id="d0adf-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="d0adf-119">Example</span></span>

<span data-ttu-id="d0adf-p104">Cet exemple utilise la propriété **Primary** pour désigner un nouvel objet **Index** dans une **TableDef** comme **Index** primaire pour cette table. Notez que le fait de définir la propriété **Primary** sur **True** définit automatiquement les propriétés **Unique** et **Required** sur **True**.</span><span class="sxs-lookup"><span data-stu-id="d0adf-p104">This example uses the **Primary** property to designate a new **Index** in a new **TableDef** as the primary **Index** for that table. Note that setting the **Primary** property to **True** automatically sets **Unique** and **Required** properties to **True** as well.</span></span>

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
