---
title: Field2.ForeignName Property (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eff81bf8d2e7f7f040611ffc1aafdedff1e35ddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874047"
---
# <a name="field2foreignname-property-dao"></a>Field2.ForeignName Property (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le nom de l'objet **Field2** d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . ForeignName

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Si l'objet **[Relation](relation-object-dao.md)** n'est pas ajouté à l'objet **[Database](database-object-dao.md)**, mais que l'objet **Field2** est ajouté à l'objet **Relation**, la propriété **ForeignName** est en lecture/écriture. Une fois que l'objet **Relation** est ajouté à la base de données, la propriété **ForeignName** est en lecture seule.

Seul un objet **Field2** appartenant à la collection **Fields** d'un objet **Relation** peut prendre en charge la propriété **ForeignName**.

Les paramètres de propriété **[Name](connection-name-property-dao.md)** et **ForeignName** d'un objet **Field2** spécifient les noms des champs correspondants dans les tables primaires et étrangères d'une relation. Les paramètres de propriété **[Table](relation-table-property-dao.md)** et **[ForeignTable](relation-foreigntable-property-dao.md)** d'un objet **Relation** déterminent les tables primaires et étrangères d'une relation.

Par exemple, prenons une liste de numéros de pièce valides (dans un champ appelé PartNo) stockée dans une table ValidParts. Vous pourriez établir une relation avec une table OrderItem de sorte que si un numéro de pièce était entré dans la table OrderItem, il devrait déjà exister dans la table ValidParts. Si le numéro de pièce n'existait pas dans la table ValidParts et si vous n'aviez pas défini la propriété **[Attributes](field-attributes-property-dao.md)** de l'objet **Relation** sur **dbRelationDontEnforce**, une erreur capturable surviendrait.

Dans ce cas, la table ValidParts est la table étrangère, la propriété **ForeignTable** de l'objet **Relation** est donc définie sur ValidParts et la propriété **Table** de l'objet **Relation** sur OrderItem. Les propriétés **Name** et **ForeignName** de l'objet **Field2** de la collection **Fields** de l'objet **Relation** sont alors définies sur PartNo.

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
