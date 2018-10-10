---
title: Instruction CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE Statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 749d593a0c9ed32290ee91aec20c79a141a83f56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470733"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Instruction CREATE TABLE (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

Crée une table.

> [!NOTE]
> [!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge l'utilisation de l'instruction CREATE TABLE, ni d'aucune instruction DDL, avec des bases de données autres que celles du moteur de base de données Microsoft Access. Utilisez les méthodes Create DAO à la place.

## <a name="syntax"></a>Syntaxe

CRÉER \[temporaire\] TABLE *table* (*type champ1* \[(*taille*)\] \[non NULL\] \[WITH COMPRESSION | AVEC COMP\] \[ *index1* \] \[, *champ2* *type* \[(*taille*)\] \[non NULL\] \[ *index2* \] \[,... \] \] \[, CONSTRAINT *index de plusieurs champs* \[,... \]\])

L’instruction CREATE TABLE comprend les éléments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Élément</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Nom de la table à créer.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Nom du ou des champs à créer dans la nouvelle table. Vous devez créer au moins un champ.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Le type de données du <em>champ</em> dans la nouvelle table.</p></td>
</tr>
<tr class="even">
<td><p><em>taille</em></p></td>
<td><p>Taille du champ en nombre de caractères (champs texte et binaires seulement).</p></td>
</tr>
<tr class="odd">
<td><p><em>index1</em>, <em>index2</em></p></td>
<td><p>Clause CONSTRAINT définissant un index de champ unique. Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>indexmultichamp</em></p></td>
<td><p>Clause CONSTRAINT définissant un index multichamp. Pour plus d'informations sur la création de cet index, voir <a href="constraint-clause-microsoft-access-sql.md">Clause CONSTRAINT</a>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez l'instruction CREATE TABLE pour définir une nouvelle table, ses champs et ses contraintes de champ. Si NOT NULL est spécifié pour un champ, les nouveaux enregistrements doivent contenir des données valides dans ce champ.

Une clause CONSTRAINT établit diverses restrictions sur un champ et peut être utilisée pour établir la clé primaire. Vous pouvez également utiliser l'instruction [CREATE INDEX](create-index-statement-microsoft-access-sql.md) pour créer une clé primaire ou des index supplémentaires sur les tables existantes.

Vous ne pouvez pas utiliser NOT NULL sur un champ unique ou dans une clause nommée CONSTRAINT qui s'applique à une clause CONSTRAINT nommée de champ unique ou multichamp. Cependant, vous ne pouvez appliquer la restriction NOT NULL qu'une seule fois à un champ. Toute tentative d'application de cette restriction plus d'une fois entraîne une erreur d'exécution.

Lors de la création d'une table temporaire, celle-ci n'est visible que dans la session dans laquelle elle a été créée. Elle est automatiquement supprimée lorsque la session est terminée. Les tables temporaires sont accessibles par plusieurs utilisateurs.

L'attribut WITH COMPRESSION peut être utilisé uniquement avec les types de données CARACTÈRES et MÉMO (également connus sous le nom de données TEXTE) et leurs synonymes.

L'attribut WITH COMPRESSION a été ajouté pour les colonnes CARACTÈRES en raison du changement de format de représentation des caractères Unicode. Les caractères Unicode nécessitent uniformément deux octets pour chaque caractère. Pour les bases de données Microsoft® Jet qui contiennent principalement des données caractères, cela pourrait signifier que le fichier de base de données doublerait de taille lors de la conversion au format du moteur de base de données Microsoft Access. Cependant, la représentation Unicode de nombreux jeux de caractères, anciennement appelés jeux de caractères codés sur un octet (SBCS) peut facilement être compressée à un seul octet. Si vous définissez une colonne de caractères avec cet attribut, les données seront automatiquement compressées au moment du stockage, et décompressées lors de leur récupération à partir de la colonne.

Les colonnes MÉMO peuvent également être définies pour stocker des données dans un format compressé. Toutefois, il existe une limite. Seules les instances des colonnes MÉMO qui, une fois compressées, représentent 4 096 octets ou moins, seront compressées. Toutes les autres instances des colonnes MÉMO resteront non compressées. Cela signifie que dans une table donnée, pour une colonne MÉMO donnée, certaines données peuvent être compressées et d'autres non.

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
