---
title: SÉLECTIONNEZ. INTO, instruction (Microsoft Access SQL)
TOCTitle: SELECT.INTO Statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4122421642b9746b5832984bf784faf65c603fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469655"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SÉLECTIONNEZ. INTO, instruction (Microsoft Access SQL)


**S’applique à**: Access 2013 | Office 2013

Crée une requête Création de table.

## <a name="syntax"></a>Syntaxe

SELECT *champ1*\[, *champ2*\[,... \] \] INTO *nouvelletable* \[IN *basededonnéesexterne* \] à partir de la *source*

L'instruction SELECT…INTO est composée des arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>champ1</em>, <em>champ2</em></p></td>
<td><p>Nom des champs à copier dans la nouvelle table.</p></td>
</tr>
<tr class="even">
<td><p><em>nouvelletable</em></p></td>
<td><p>Nom de la table à créer. Ce nom doit respecter les conventions d'affectation de nom standard. Si<em>nouvelletable</em> est identique au nom d'une table existante, une erreur interceptable se produit..</p></td>
</tr>
<tr class="odd">
<td><p><em>basededonnéesexterne</em></p></td>
<td><p>Chemin d'accès à une base de données externe. Pour une description du chemin d'accès, voir la clause <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">IN</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Nom de la table existante dans laquelle les enregistrements sont sélectionnés. Il peut s'agir d'une ou de plusieurs tables, ou d'une requête</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Vous pouvez utiliser les requêtes Création de table pour archiver les enregistrements, faire des copies de sauvegarde des tables, ou pour faire des copies à exporter dans une autre base de données ou à utiliser pour produire des états concernant des données sur une période déterminée. Par exemple, vous pouvez produire un état Ventes Mensuelles par Région en exécutant la même requête Création de table chaque mois.


> [!NOTE]
> <UL>
> <LI>
> <P>Vous pouvez définir une clé primaire pour la nouvelle table. Lorsque vous créez la table, ses champs héritent du type de données et de la taille de champ de chaque champ présent dans les tables sous-jacentes de la requête, mais aucune autre propriété de champ ou de table n'est transférée.</P>
> <LI>
> <P>Pour ajouter des données à une table existante, utilisez l'instruction <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A> au lieu de créer une requête Ajout.</P>
> <LI>
> <P>Pour savoir quels enregistrements seront sélectionnés avant d'exécuter la requête Création de table, lancez d'abord une instruction <A href="select-statement-microsoft-access-sql.md">SELECT</A> avec les mêmes critères de sélection puis examinez les résultats obtenus.</P></LI></UL>



## <a name="example"></a>Exemple

Dans cet exemple, tous les enregistrements de la table Employees sont sélectionnés, puis copiés dans une nouvelle table appelée Emp Backup.

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
