---
title: Field.Attributes, propriété (DAO)
TOCTitle: Attributes Property
description: Propriété Attributes
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/14/2021
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 77cae4e2d4c3a09d75afa3c9f2228f72bccfd5d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626756"
---
# <a name="fieldattributes-property-dao"></a>Field.Attributes, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet **[Field](field-object-dao.md)**. Valeur de type **Long** en lecture et en écriture.

## <a name="syntax"></a>Syntaxe

*expression* .Attributes

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

La propriété **Attributes** d’un objet **Field** spécifie les caractéristiques du champ représenté par l’objet **Field**. La propriété **Attributes** est stockée sous la seule valeur Long Integer et elle est la somme des constantes Long suivantes :


|**Constante**|**Valeur**|**Description**|
|:----------|:----------|:----------|
|**dbAutoIncrField**|**16**|La valeur de champ des nouveaux enregistrements est automatiquement incrémentée d’un entier long unique non modifiable (dans un espace de travail Microsoft Access, pris en charge uniquement par les tables de bases de données de moteur de base de données Microsoft Access).|
|**dbDescending**|**1**|Le champ est trié dans l’ordre décroissant (Z à A ou 100 à 0). Cette option ne concerne qu’un objet <strong>Field</strong> dans une collection <strong>Fields</strong> d’un objet <strong>Index</strong>. Si vous omettez cette constante, le champ est trié dans l’ordre croissant (A à Z ou 0 à 100). Il s’agit de la valeur par défaut pour les champs <strong>Index</strong> et <strong>TableDef</strong> (espaces de travail Microsoft Access uniquement).|
|**dbFixedField**|**1**|La taille de champ est fixe (par défaut : champs numériques).|
|**dbHyperlinkField**|**32768**|Le champ contient des informations de lien hypertexte (champs Memo uniquement).|
|**dbSystemField**|**8192**|Le champ stocke des informations de réplication pour réplicas ; Vous ne pouvez pas supprimer ce type de champ (espace de travail Microsoft Access uniquement).|
|**dbUpdatableField**|**32**|La valeur de champ peut être modifiée.|
|**dbVariableField**|**2**|La taille du champ est variable (champs Text uniquement).\

Dans le cas d'un objet qui n'est pas encore ajouté à une collection, cette propriété est en lecture/écriture. En ce qui concerne un objet **Field** ajouté, la disponibilité de la propriété **Attributes** dépend de l'objet qui contient la collection **Fields**.

|**Si l'objet Field appartient à un**|**La propriété Attributes est alors**|
|:----------|:----------|
|objet **Index**|En lecture et en écriture jusqu'à ce que l’objet **TableDef** auquel l’objet **Index** est ajouté soit ajouté à un objet **Database** ; la propriété est alors en lecture seule.|
|objet **QueryDef**|Lecture seule|
|objet **Recordset**|Lecture seule|
|objet **Relation**|Non pris en charge|
|objet **TableDef**|Lecture/écriture|

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

