---
title: Field.Attributes, propriété (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 010c7a2aea777a93d1ced2d33d8743320dd05ada
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293153"
---
# <a name="fieldattributes-property-dao"></a>Field.Attributes, propriété (DAO)


**S’applique à** : Access 2013, Office 2013


Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet **[Field](field-object-dao.md)**. **Long** (en lecture/écriture).

## <a name="syntax"></a>Syntaxe

*expression* .Attributes

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

La valeur spécifie les caractéristiques du champ représenté par l’objet **Field** et peut être une combinaison de ces constantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>La valeur de champ des nouveaux enregistrements est automatiquement incrémentée d’un entier long unique non modifiable (dans un espace de travail Microsoft Access, pris en charge uniquement par les tables de bases de données de moteur de base de données Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>Le champ est trié dans l’ordre décroissant (Z à A ou 100 à 0) ; cette option s’applique uniquement à un objet <strong>Field</strong> d’une collection <strong>Fields</strong> d’un objet <strong>Index</strong>. Si vous omettez cette constante, le champ est trié par ordre croissant (A à Z ou 0 à 100). Il s’agit de la valeur par défaut pour les champs <strong>Index</strong> et <strong>TableDef</strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>La taille de champ est fixe (par défaut : champs numériques).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>Le champ contient des informations de lien hypertexte (champs Memo uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>Le champ stocke des informations de réplication pour réplicas ; Vous ne pouvez pas supprimer ce type de champ (espace de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>La valeur de champ peut être modifiée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>La taille du champ est variable (champs texte uniquement).</p></td>
</tr>
</tbody>
</table>


Dans le cas d'un objet qui n'est pas encore ajouté à une collection, cette propriété est en lecture/écriture. En ce qui concerne un objet **Field** ajouté, la disponibilité de la propriété **Attributes** dépend de l'objet qui contient la collection **Fields**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si l'objet Field appartient à un</p></th>
<th><p>La propriété Attributes est</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objet <strong>Index</strong></p></td>
<td><p>En lecture/écriture jusqu'à ce que l’objet <strong>TableDef</strong> auquel l’objet <strong>Index</strong> est ajouté soit ajouté à un objet <strong>Database</strong> ; la propriété est alors en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>TableDef</strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
</tbody>
</table>


Lorsque vous définissez plusieurs attributs, vous pouvez les combiner en additionnant les constantes appropriées. Toute valeur non valide est ignorée sans provoquer d'erreur.

## <a name="example"></a>Exemple

Cet exemple affiche la propriété **Attributes** des objets **Field**, **Relation** et **TableDef** dans la base de données Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

