---
title: Propriété Index.Unique (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5c94200245b4736ad244cb37beec617a98d6c367
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704622"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="ab0bf-102">Propriété Index.Unique (DAO)</span><span class="sxs-lookup"><span data-stu-id="ab0bf-102">Index.Unique property (DAO)</span></span>

<span data-ttu-id="ab0bf-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab0bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab0bf-104">Définit ou renvoie une valeur qui indique si un objet **[Index](index-object-dao.md)** représente un index (une clé) unique d'une table (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ab0bf-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab0bf-105">Syntax</span></span>

<span data-ttu-id="ab0bf-106">*expression* . Unique</span><span class="sxs-lookup"><span data-stu-id="ab0bf-106">*expression* .Unique</span></span>

<span data-ttu-id="ab0bf-107">*expression* Variable qui représente un objet **Index** .</span><span class="sxs-lookup"><span data-stu-id="ab0bf-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0bf-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab0bf-108">Remarks</span></span>

<span data-ttu-id="ab0bf-109">Cette propriété est en lecture/écriture jusqu'à ce que l'objet soit ajouté à une collection ; elle passe alors en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="ab0bf-p101">Un index unique est constitué d'un ou de plusieurs champs qui organisent de manière logique tous les enregistrements d'une table dans un ordre unique et prédéfini. Si l'index est constitué d'un seul champ, les valeurs de ce dernier doivent être uniques pour la table entière. Si l'index est constitué de plus d'un champ, chacun de ces champs peut contenir des valeurs en double, mais chaque combinaison de valeurs de tous les champs indexés doit être unique.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-p101">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order. If the index consists of one field, values in that field must be unique for the entire table. If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="ab0bf-p102">Si les propriétés **Unique** et **[Primary](index-primary-property-dao.md)** d'un objet **Index** ont toutes les deux la valeur **True**, l'index est unique et primaire : il identifie de manière unique tous les enregistrements de la table dans un ordre logique et prédéfini. Si la propriété **Primary** a la valeur **False**, l'index est de type secondaire. Les index secondaires (clés et non clés) organisent les enregistrements de manière logique dans un ordre prédéfini sans servir d'identificateur pour les enregistrements de la table.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-p102">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order. If the **Primary** property is set to **False**, the index is a secondary index. Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>

> [!NOTE]
> - <span data-ttu-id="ab0bf-116">Vous n'êtes pas obligé de créer des index pour les tables mais sachez que, dans les grandes tables non indexées, l'accès à un enregistrement spécifique risque de prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span>
> - <span data-ttu-id="ab0bf-117">Les enregistrements extraits de tables non indexées sont renvoyés sans ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="ab0bf-118">La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** dans l'objet **Index** détermine l'ordre des enregistrements et donc les techniques d'accès à utiliser pour cet objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-118">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that **Index** object.</span></span>
> - <span data-ttu-id="ab0bf-119">Un index unique facilite la recherche des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-119">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="ab0bf-120">Index n’affectent pas l’ordre physique d’une table de base ; index affecte uniquement la manière dont les enregistrements sont accessibles par l’objet **[Recordset](recordset-object-dao.md)** de type table lorsqu’un index particulier est choisi ou lorsque le moteur de base de données Microsoft Access crée des objets **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ab0bf-120">Indexes don't affect the physical order of a base table; indexes affect only how the records are accessed by the table-type **[Recordset](recordset-object-dao.md)** object when a particular index is chosen or when the Microsoft Access database engine creates **Recordset** objects.</span></span>

## <a name="example"></a><span data-ttu-id="ab0bf-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="ab0bf-121">Example</span></span>

<span data-ttu-id="ab0bf-p103">Cet exemple attribue la valeur **True** à la propriété **Unique** d'un nouvel objet **Index** et ajoute l'index à la collection **Indexes** de la table Employees. Il énumère ensuite la collection **Indexes** de l'objet **TableDef** et la collection **Properties** de chaque **Index**. Le nouvel objet **Index** n'acceptera qu'un seul enregistrement avec une combinaison donnée de Country (pays), LastName (nom) et FirstName (prénom) dans l'objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="ab0bf-p103">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
