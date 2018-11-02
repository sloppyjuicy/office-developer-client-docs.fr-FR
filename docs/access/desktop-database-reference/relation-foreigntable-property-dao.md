---
title: Propriété Relation.ForeignTable (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dcd454bc1c570e119cc8948acb8077a54649db84
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921711"
---
# <a name="relationforeigntable-property-dao"></a>Propriété Relation.ForeignTable (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie le nom de la table étrangère d'une relation (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . ForeignTable

*expression* Variable qui représente un objet **Relation** .

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture pour un nouvel objet **[Relation](relation-object-dao.md)** pas encore ajouté à une collection et en lecture seule pour un objet **Relation** existant de la collection **[Relations](relations-collection-dao.md)**.

Le paramètre de propriété **ForeignTable** d'un objet **Relation** est le paramètre de propriété **[Name](connection-name-property-dao.md)** de l'objet **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** qui représente la table étrangère ou la requête ; le paramètre de propriété **[Table](relation-table-property-dao.md)** est le paramètre de propriété **Name** de l'objet **TableDef** ou **QueryDef** qui représente la table primaire ou la requête.

Par exemple, prenons une liste de numéros de pièce valides (dans un champ appelé PartNo) stockée dans une table ValidParts. Vous pourriez établir une relation avec une table OrderItem de sorte que si un numéro de pièce était entré dans la table OrderItem, il devrait déjà exister dans la table ValidParts. Si le numéro de pièce n'existait pas dans la table ValidParts et si vous n'aviez pas défini la propriété **[Attributes](field-attributes-property-dao.md)** de l'objet **Relation** sur **dbRelationDontEnforce**, une erreur capturable surviendrait.

Dans ce cas, la table ValidParts est la table primaire, la propriété **Table** de l'objet **Relation** est donc définie sur ValidParts et la propriété **ForeignTable** de l'objet **Relation** sur OrderItem. Les propriétés **Name** et **ForeignName** de l'objet **Field** de la collection **Fields** de l'objet **Relation** sont alors définies sur PartNo.

## <a name="example"></a>Exemple

Cet exemple montre comment les propriétés **Table**, **ForeignTable** et **ForeignName** définissent les termes d'une **Relation** entre deux tables.

```vb 
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
