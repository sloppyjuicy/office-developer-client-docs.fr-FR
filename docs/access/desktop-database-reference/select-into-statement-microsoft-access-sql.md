---
title: SELECT.INTO, instruction (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 03/22/2022
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 04e4fecb068bdd5a9a46dd9d38edeaa961cdedf5
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63715927"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECT.INTO, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Crée une requête Création de table.

## <a name="syntax"></a>Syntaxe

SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*

L’instruction SELECT...INTO comprend les parties suivantes :

|**Élément**|**Description**|
|:-------|:--------------|
| _field1,field2_ | Noms des champs à copier dans la nouvelle table.</br>|
| _newtable_ | Nom de la table devant être créée. Il doit respecter des conventions de noms standard. Si <em>nouvelletable</em> correspond au nom d’une table existante, une erreur récupérable se produit.</p></td>
| _basededonnéesexterne_ | Chemin d’accès à une base de données externe. Pour une description du chemin d’accès, voir la clause [IN](/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql.md).</br>|
| _source_ | Nom de la table existante dans laquelle des enregistrements sont sélectionnés. Il peut s’agir d’une ou plusieurs tables, ou d’une requête.</br>|

## <a name="remarks"></a>Remarques

Vous pouvez utiliser des requêtes Création de table pour archiver des enregistrements, créer des copies de sauvegarde de vos tables, ou créer des copies à exporter vers une autre base de données ou à utiliser comme base pour les états qui affichent des données pour une période spécifique. Par exemple, vous pouvez produire un rapport des ventes mensuelles par région en exécutant la même requête Création de table chaque mois.

> [!NOTE]
>
> - Vous pouvez définir une  pour la nouvelle table. Lorsque vous créez la table, les champs de celle-ci héritent du  et de la taille de champ de chaque champ dans les tables sous-jacentes de la requête. Aucune autre propriété de champ ou de table n’est transférée.
> - Pour ajouter des données à une table existante, utilisez plutôt l’instruction INSÉRER DANS pour créer une [.
> - Pour déterminer les enregistrements qui seront sélectionnés avant d’exécuter la requête Création de table, commencez par examiner les résultats d’une instruction SELECT qui utilise les mêmes critères de sélection.

## <a name="example"></a>Exemple

Cet exemple sélectionne tous les enregistrements de la table Employees et les copie dans une nouvelle table nommée Emp Backup.

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
