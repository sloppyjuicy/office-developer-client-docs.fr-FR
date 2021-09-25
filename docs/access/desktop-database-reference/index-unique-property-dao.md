---
title: Index.Unique, propriété (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 45428f15c0bca259703e0f95fb7ad8693d841044
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615339"
---
# <a name="indexunique-property-dao"></a>Index.Unique, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique si un objet **[Index](index-object-dao.md)** représente un index (une clé) unique d'une table (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* Unique

*expression* Variable qui représente un objet **Index.**

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture jusqu'à ce que l'objet soit ajouté à une collection ; elle passe alors en lecture seule.

Un index unique est constitué d'un ou de plusieurs champs qui organisent de manière logique tous les enregistrements d'une table dans un ordre unique et prédéfini. Si l'index est constitué d'un seul champ, les valeurs de ce dernier doivent être uniques pour la table entière. Si l'index est constitué de plus d'un champ, chacun de ces champs peut contenir des valeurs en double, mais chaque combinaison de valeurs de tous les champs indexés doit être unique.

Si les propriétés **Unique** et **[Primary](index-primary-property-dao.md)** d'un objet **Index** ont toutes les deux la valeur **True**, l'index est unique et primaire : il identifie de manière unique tous les enregistrements de la table dans un ordre logique et prédéfini. Si la propriété **Primary** a la valeur **False**, l'index est de type secondaire. Les index secondaires (clés et non clés) organisent les enregistrements de manière logique dans un ordre prédéfini sans servir d'identificateur pour les enregistrements de la table.

> [!NOTE]
> - Vous n'êtes pas obligé de créer des index pour les tables mais sachez que, dans les grandes tables non indexées, l'accès à un enregistrement spécifique risque de prendre beaucoup de temps.
> - Les enregistrements extraits de tables non indexées sont renvoyés sans ordre particulier.
> - La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **[Field](field-object-dao.md)** dans l'objet **Index** détermine l'ordre des enregistrements et donc les techniques d'accès à utiliser pour cet objet **Index**.
> - Un index unique facilite la recherche des enregistrements.
> - Les index n’affectent pas l’ordre physique d’une table de base ; Les index affectent uniquement la façon dont les enregistrements sont accessibles par l’objet **[Recordset](recordset-object-dao.md)** de type table lorsqu’un index particulier est choisi ou lorsque le moteur de base de données Microsoft Access crée des objets **Recordset.**

## <a name="example"></a>Exemple

Cet exemple attribue la valeur **True** à la propriété **Unique** d'un nouvel objet **Index** et ajoute l'index à la collection **Indexes** de la table Employees. Il énumère ensuite la collection **Indexes** de l'objet **TableDef** et la collection **Properties** de chaque **Index**. Le nouvel objet **Index** n'acceptera qu'un seul enregistrement avec une combinaison donnée de Country (pays), LastName (nom) et FirstName (prénom) dans l'objet **TableDef**.

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
