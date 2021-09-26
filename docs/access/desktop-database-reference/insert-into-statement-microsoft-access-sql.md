---
title: Instruction INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 0a4c94e90e2c9efd29d0d07eae852ab2a2c009f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568900"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>Instruction INSERT INTO (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Ajoute un ou plusieurs enregistrements à un tableau. Cette opération est une requête Ajout.

## <a name="syntax"></a>Syntaxe

### <a name="multiple-record-append-query"></a>Requête Ajout avec plusieurs enregistrements :

INSERT INTO *cible* \[(*champ1*\[, *champ2*\[, …\]\])\] \[IN *basededonnéesexterne*\] SELECT \[*source*.\]*champ1*\[, *champ2*\[, …\] FROM *expressiontable*

### <a name="single-record-append-query"></a>Requête Ajout avec un seul enregistrement :

INSERT INTO *cible* \[(*champ1*\[, *champ2*\[, …\]\])\] VALUES (*valeur1*\[, *valeur2*\[, …\])

L'instruction INSERT INTO comprend les éléments suivants :

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
<td><p><em>target</em></p></td>
<td><p>Nom de la table ou de la requête à laquelle ajouter les enregistrements.</p></td>
</tr>
<tr class="even">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Noms des champs auxquels ajouter les données, si après un argument <em>target</em>, ou noms des champs à partir desquels obtenir les données, si après un argument <em>source</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>basededonnéesexterne</em></p></td>
<td><p>Chemin d’accès à une base de données externe. Pour une description du chemin d’accès, voir la clause <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Nom de la table ou de la requête à partir de laquelle copier les enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><em>expressiontable</em></p></td>
<td><p>Nom des tables à partir desquelles les enregistrements sont insérés. Cet argument peut être un nom de table simple ou un composé issu d’une opération <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> ou <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a>, ou d’une requête enregistrée.</p></td>
</tr>
<tr class="even">
<td><p><em>valeur1</em>, <em>valeur2</em></p></td>
<td><p>Valeurs à insérer dans les champs spécifiques du nouvel enregistrement. Chaque valeur est insérée dans le champ qui correspond à la position de la valeur dans la liste : <em>valeur1</em> est insérée dans <em>champ1</em> du nouvel enregistrement, <em>valeur2</em> dans <em>champ2</em>, et ainsi de suite. Vous devez séparer les valeurs par une virgule et placer les champs de texte entre guillemets (' ').</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’instruction INSERT INTO pour ajouter un enregistrement unique à une table à l’aide de la syntaxe de requête Ajout d’enregistrement unique indiquée ci-dessus. Dans ce cas, votre code spécifie le nom et la valeur de chaque champ de l’enregistrement. Vous devez spécifier chacun des champs de l’enregistrement auxquels une valeur doit être attribuée, et la valeur de chaque champ. Si vous ne spécifiez pas tous les champs, la valeur par défaut ou une valeur **Null** est insérée dans les colonnes vides. Les enregistrements sont ajoutés à la fin de la table.

Vous pouvez également utiliser INSERT INTO pour ajouter un jeu d’enregistrements à partir d’une autre table ou requête à l’aide de la clause SELECT …FROM, comme décrit plus haut dans la syntaxe de requête Ajout avec plusieurs enregistrements. Dans ce cas, la clause SELECT spécifie les champs à ajouter à la table *cible* spécifiée.

La table *source* ou *cible* peut spécifier une table ou une requête. Si une requête est spécifiée, le moteur de base de données Microsoft Access ajoute des enregistrements à toutes les tables spécifiées par la requête.

INSERT INTO est facultative mais lorsqu’elle est incluse, elle précède l’instruction [SELECT](select-statement-microsoft-access-sql.md).

Si votre table de destination contient une clé primaire, assurez-vous que vous ajoutez des valeurs uniques et non **Null** dans les champs de clé primaire. Si ce n’est pas le cas, le moteur de base de données Microsoft Access n’ajoutera pas les enregistrements.

Si vous ajoutez des enregistrements à une table avec un champ NuméroAuto et que vous voulez renuméroter les enregistrements ajoutés, n’incluez pas le champ NuméroAuto dans votre requête. Incluez le champ NuméroAuto dans la requête si vous voulez conserver les valeurs d’origine du champ.

Utilisez la clause IN pour ajouter des enregistrements à une table dans une autre base de données.

Pour créer une table, utilisez l’instruction [SELECT... INTO](select-into-statement-microsoft-access-sql.md) au lieu de créer une requête Création de table.

Pour savoir quels enregistrements seront ajoutés avant d’exécuter la requête Ajout, exécutez d’abord une requête sélectionnée qui utilise les mêmes critères de sélection, et observez les résultats.

Une requête Ajout copie des enregistrements à partir d’une ou plusieurs tables vers une autre. Les tables contenant les enregistrements que vous ajoutez ne sont pas concernées par la requête Ajout.

Au lieu d’ajouter des enregistrements existants à partir d’une autre table, vous pouvez spécifier la valeur de chaque champ dans un nouvel enregistrement unique à l’aide de la clause VALUES. Si vous omettez la liste de champs, la clause VALUES doit inclure une valeur pour chaque champ de la table. Sinon, l’opération INSERT échoue. Utilisez une instruction INSERT INTO supplémentaire avec une clause VALUES pour chaque enregistrement supplémentaire que vous souhaitez créer.

**Lien fourni par** la communauté [UtterAccess](https://www.utteraccess.com). UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.

- [Générer des numéros séquentiels pour les instructions INSERT/UPDATE](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [Formateur SQL vers VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>Exemple

Cet exemple sélectionne tous les enregistrements dans une table New Customers hypothétique et les ajoute à la table Customers. Lorsque les colonnes individuelles ne sont pas désignées, les noms de colonne de la table SELECT doivent correspondre exactement à ceux de la table INSERT INTO.

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

Cet exemple crée un nouvel enregistrement dans la table Employees.

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

