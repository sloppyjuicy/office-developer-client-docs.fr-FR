---
title: Field.ForeignName, propriété (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cbf586d3c07ccfd01a170efd4efaaacc45385c36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626685"
---
# <a name="fieldforeignname-property-dao"></a>Field.ForeignName, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le nom de l'objet **[Field](field-object-dao.md)** d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* ForeignName

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Si l'objet **[Relation](relation-object-dao.md)** n'est pas ajouté à l'objet **[Database](database-object-dao.md)**, mais que l'objet **Field** est ajouté à l'objet **Relation**, la propriété **ForeignName** est en lecture/écriture. Une fois que l'objet **Relation** est ajouté à la base de données, la propriété **ForeignName** est en lecture seule.

Seul un objet **Field** appartenant à la collection **Fields** d'un objet **Relation** peut prendre en charge la propriété **ForeignName**.

Les paramètres de propriété **[Name](connection-name-property-dao.md)** et **ForeignName** d'un objet **Field** spécifient les noms des champs correspondants dans les tables primaires et étrangères d'une relation. Les paramètres de propriété **[Table](relation-table-property-dao.md)** et **[ForeignTable](relation-foreigntable-property-dao.md)** d'un objet **Relation** déterminent les tables primaires et étrangères d'une relation.

Par exemple, prenons une liste de numéros de pièce valides (dans un champ appelé PartNo) stockée dans une table ValidParts. Vous pourriez établir une relation avec une table OrderItem de sorte que si un numéro de pièce était entré dans la table OrderItem, il devrait déjà exister dans la table ValidParts. Si le numéro de pièce n'existait pas dans la table ValidParts et si vous n'aviez pas défini la propriété **[Attributes](field-attributes-property-dao.md)** de l'objet **Relation** sur **dbRelationDontEnforce**, une erreur capturable surviendrait.

Dans ce cas, la table ValidParts est la table étrangère, la propriété **ForeignTable** de l'objet **Relation** est donc définie sur ValidParts et la propriété **Table** de l'objet **Relation** sur OrderItem. Les propriétés **Name** et **ForeignName** de l'objet **Field** de la collection **Fields** de l'objet **Relation** sont alors définies sur PartNo.

## <a name="example"></a>Exemple

Cet exemple montre comment les propriétés **Table**, **ForeignTable** et **ForeignName** définissent les termes d’une **Relation** entre deux tables.

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
