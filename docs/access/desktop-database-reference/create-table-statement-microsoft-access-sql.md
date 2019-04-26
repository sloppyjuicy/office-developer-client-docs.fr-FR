---
title: Instruction CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295358"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Instruction CREATE TABLE (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée une table.

> [!NOTE]
> Le moteur de base de données Access ne prend pas en charge l’utilisation de l’instruction CREATE TABLE ou de toute instruction DDL avec des bases de données d’un moteur de base de données autre que Microsoft Access. Utilisez plutôt les méthodes **Create** de DAO.

## <a name="syntax"></a>Syntaxe

CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])

L’instruction CREATE TABLE comprend les parties suivantes :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Nom de la table à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Nom du ou des champs à créer dans la nouvelle table. Vous devez créer au moins un champ.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Type de données de <em>field</em> dans la nouvelle table.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Taille du champ en nombre de caractères (champs texte et binaires seulement).</p></td>
</tr>
<tr class="odd">
<td><p><em>index1</em>, <em>index2</em></p></td>
<td><p>Clause CONSTRAINT définissant un index de champ unique. Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>Clause CONSTRAINT définissant un index multi-champ. Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’instruction CREATE TABLE permet de définir une nouvelle table, ses champs et ses contraintes de champ. Si NOT NULL est spécifié pour un champ, les nouveaux enregistrements doivent contenir des données valides dans ce champ.

Une clause CONSTRAINT établit diverses restrictions sur un champ et peut être utilisée pour établir la clé primaire. Vous pouvez également utiliser l'instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour créer une clé primaire ou des index supplémentaires sur les tables existantes.

Vous pouvez utiliser l’instruction NON NULL sur un champ unique ou à l’intérieur d’une clause CONSTRAINT nommée qui s’applique à une instruction CONSTRAINT nommée portant sur un ou plusieurs champs. Toutefois, vous ne pouvez appliquer la restriction NON NULL qu’une seule fois à un champ. Une tentative d’appliquer cette restriction plusieurs fois génère une erreur d’exécution.

Lors de la création d'une table temporaire, celle-ci n'est visible que dans la session dans laquelle elle a été créée. Elle est supprimée automatiquement à la fin de la session. Les tables temporaires sont accessible par plusieurs utilisateurs.

L’attribut WITH COMPRESSION peut être utilisé uniquement avec les types de données CARACTÈRE et MÉMO (également appelé TEXTE) et leurs synonymes.

L’attribut WITH COMPRESSION a été ajouté pour les colonnes de type CARACTÈRE en raison de la modification du format de représentation de caractère Unicode. Les caractères Unicode nécessitent uniformément deux octets par caractère. Pour les bases de données Microsoft Jet qui contiennent principalement des données caractères, cela pourrait signifier que le fichier de base de données doublerait de taille lors de la conversion au format du moteur de base de données Microsoft Access. Cependant, la représentation Unicode de nombreux jeux de caractères, anciennement appelés jeux de caractères codés sur un octet (SBCS), peut facilement être compressée à un seul octet. Si vous définissez une colonne de type CARACTÈRE avec cet attribut, les données sont automatiquement compressées pour le stockage, et décompressées lors de leur extraction de la colonne.

Des colonnes de type MÉMO peuvent également être définies pour stocker des données dans un format compressé. Il existe cependant une limitation. Seules les instances de colonnes de type MÉMO qui, une fois compressées, ne dépassent pas 4 096 octets, sont compressées. Les autres instances des colonnes de type MÉMO ne sont pas compressées. Cela signifie que, dans un tableau donné, pour une colonne de type MÉMO donnée, certaines données peuvent être compressées et d’autres pas.

## <a name="example"></a>Exemple

Cet exemple crée une nouvelle table appelée ThisTable qui comporte deux champs de texte.

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Cet exemple crée une nouvelle table appelée MyTable avec deux champs de texte, un champ Date/Heure et un index unique composé de ces trois champs.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Cet exemple crée une nouvelle table avec deux champs de texte et un champ **Entier**. Le champ SSN correspond à la clé primaire.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```
