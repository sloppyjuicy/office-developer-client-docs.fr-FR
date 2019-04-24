---
title: Index. primary, propriété (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: da0d28a5599dadc9432b38ab6155e53e884e4838
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291753"
---
# <a name="indexprimary-property-dao"></a>Index. primary, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique si un objet **[Index](index-object-dao.md)** représente un index de clé primaire pour une table (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Primary

*expression* Variable qui représente un objet **index** .

## <a name="remarks"></a>Remarques

Le paramètre de propriété **Primary** est en lecture/écriture pour un nouvel objet **Index** par encore ajouté à une collection et en lecture seule pour un objet **Index** existant dans une collection **[Indexes](indexes-collection-dao.md)**. Si l'objet **Index** est ajouté à l'objet **[TableDef](tabledef-object-dao.md)** mais que l'objet **TableDef** n'est pas ajouté à la collection **[TableDefs](tabledefs-collection-dao.md)**, la propriété **Index** est en lecture/écriture.

Un index de clé primaire consiste en un ou plusieurs champs qui identifient de manière unique tous les enregistrements d'une table dans un ordre prédéfini. Étant donné que le champ d'index doit être unique, la propriété **[Unique](index-unique-property-dao.md)** de l'objet **Index** est définie sur **True**. Si l'index de clé primaire est constitué de plusieurs champs, chaque champ peut contenir des valeurs dupliquées, mais chaque combinaison de valeurs de tous les champs indexés doit être unique. Un index de clé primaire est constitué d'une clé pour la table et renferme généralement les mêmes champs que la clé primaire.

> [!NOTE]
> [!REMARQUE] La création d'index n'est pas obligatoire pour les tables, mais l'accès à un enregistrement spécifique dans des grandes tables non indexées peut prendre beaucoup de temps. La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** de l'objet **Index** détermine l'ordre des enregistrements et, par conséquent, les techniques d'accès à utiliser pour cet index. Lorsque vous créez une nouvelle table dans votre base de données, il est recommandé de créer un index sur un ou plusieurs champs qui identifie chaque enregistrement de manière unique, puis de définir la propriété **Primary** de l'objet **Index** sur **True**.

Lorsque vous définissez une clé primaire pour une table, la clé primaire est automatiquement définie comme index de clé primaire de la table.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Primary** pour désigner un nouvel objet **Index** dans une **TableDef** comme **Index** primaire pour cette table. Notez que le fait de définir la propriété **Primary** sur **True** définit automatiquement les propriétés **Unique** et **Required** sur **True**.

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
