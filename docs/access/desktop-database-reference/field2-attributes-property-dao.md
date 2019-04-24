---
title: Field2. Attributes, propriété (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292887"
---
# <a name="field2attributes-property-dao"></a>Field2. Attributes, propriété (DAO)


**S’applique à** : Access 2013, Office 2013


Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet **Field2**. Type de données **Long** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Ceux

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

La valeur spécifie les caractéristiques du champ représenté par l'objet **Field2** et peut être une combinaison de ces constantes.

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
<td><p>Le champ est trié dans l’ordre décroissant (Z à A ou 100 à 0) ; cette option s’applique uniquement à un objet <strong>Field2</strong> d’une collection <strong>Fields</strong> d’un objet <strong>Index</strong>. Si vous omettez cette constante, le champ est trié dans l’ordre croissant (A à Z ou 0 à 100). Il s’agit de la valeur par défaut pour les champs <strong>Index</strong> et <strong>TableDef</strong> (espaces de travail Microsoft Access uniquement)..</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>La taille du champ est fixe (par défaut pour les champs numériques).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>Le champ contient un lien hypertexte (champs Mémo uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>Le champ stocke des informations de réplication pour les réplicas ; vous ne pouvez pas supprimer ce type de champ (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>La valeur du champ peut être modifiée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>La taille du champ est variable (champs Texte uniquement).</p></td>
</tr>
</tbody>
</table>


Pour un objet pas encore ajouté à une collection, cette propriété est en lecture/écriture. Pour un objet **Field2** ajouté, la disponibilité de la propriété **Attributes** dépend de l'objet contenant la collection **Fields**.

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
<td><p>objet <strong>Index</strong></p></td>
<td><p>En lecture/écriture jusqu'à ce que l'objet <strong>TableDef</strong> auquel l'objet <strong>Index</strong> est ajouté soit ajouté à un objet <strong>Database</strong>. La propriété est alors en lecture seule.</p></td>
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
<td><p>Non reconnu</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>TableDef</strong></p></td>
<td><p>En lecture-écriture.</p></td>
</tr>
</tbody>
</table>


Lorsque vous définissez plusieurs attributs, vous pouvez les combiner en additionnant les constantes appropriées. Toute valeur non valide est ignorée sans provoquer d'erreur.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **Attributes** pour les objets **Field2**, **Relation** et **TableDef** de la base de données Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
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

