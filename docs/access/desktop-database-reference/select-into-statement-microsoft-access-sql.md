---
title: SELECT.INTO, instruction (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308721"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="374d9-102">SELECT.INTO, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="374d9-102">SELECT…INTO Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="374d9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="374d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="374d9-104">Crée une requête Création de table.</span><span class="sxs-lookup"><span data-stu-id="374d9-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="374d9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="374d9-105">Syntax</span></span>

<span data-ttu-id="374d9-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span><span class="sxs-lookup"><span data-stu-id="374d9-106">SELECT field1[, field2[, …]] INTO newtable [IN externaldatabase]
    FROM source</span></span>

<span data-ttu-id="374d9-107">L’instruction SELECT...INTO comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="374d9-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="374d9-108">Quitter</span><span class="sxs-lookup"><span data-stu-id="374d9-108">Part</span></span></p></th>
<th><p><span data-ttu-id="374d9-109">Description</span><span class="sxs-lookup"><span data-stu-id="374d9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="374d9-110"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="374d9-110"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="374d9-111">Noms des champs à copier dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="374d9-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="374d9-112"><em>newtable</em></span><span class="sxs-lookup"><span data-stu-id="374d9-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="374d9-p101">Nom de la table devant être créée. Il doit respecter des conventions de noms standard. Si <em>nouvelletable</em> correspond au nom d’une table existante, une erreur récupérable se produit.</span><span class="sxs-lookup"><span data-stu-id="374d9-p101">The name of the table to be created. It must conform to standard naming conventions. If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="374d9-116"><em>basededonnéesexterne</em></span><span class="sxs-lookup"><span data-stu-id="374d9-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="374d9-p102">Chemin d’accès à une base de données externe. Pour une description du chemin d’accès, voir la clause <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</span><span class="sxs-lookup"><span data-stu-id="374d9-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="374d9-119"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="374d9-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="374d9-120">Nom de la table dans laquelle des enregistrements sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="374d9-120">The name of the existing table from which records are selected.</span></span> <span data-ttu-id="374d9-121">Il peut s’agir d’une ou plusieurs tables, ou d’une requête.</span><span class="sxs-lookup"><span data-stu-id="374d9-121">This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="374d9-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="374d9-122">Remarks</span></span>

<span data-ttu-id="374d9-p104">Vous pouvez utiliser des requêtes Création de table pour archiver des enregistrements, créer des copies de sauvegarde de vos tables, ou créer des copies à exporter vers une autre base de données ou à utiliser comme base pour les états qui affichent des données pour une période spécifique. Par exemple, vous pouvez produire un rapport des ventes mensuelles par région en exécutant la même requête Création de table chaque mois.</span><span class="sxs-lookup"><span data-stu-id="374d9-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="374d9-p105">Vous pouvez définir une  pour la nouvelle table. Lorsque vous créez la table, les champs de celle-ci héritent du  et de la taille de champ de chaque champ dans les tables sous-jacentes de la requête. Aucune autre propriété de champ ou de table n’est transférée.</span><span class="sxs-lookup"><span data-stu-id="374d9-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="374d9-127">Pour ajouter des données à une table existante, utilisez plutôt l’instruction INSÉRER DANS pour créer une [.</span><span class="sxs-lookup"><span data-stu-id="374d9-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="374d9-128">Pour déterminer les enregistrements qui seront sélectionnés avant d’exécuter la requête Création de table, commencez par examiner les résultats d’une instruction SELECT qui utilise les mêmes critères de sélection.</span><span class="sxs-lookup"><span data-stu-id="374d9-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="374d9-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="374d9-129">Example</span></span>

<span data-ttu-id="374d9-130">Cet exemple sélectionne tous les enregistrements de la table Employees et les copie dans une nouvelle table nommée Emp Backup.</span><span class="sxs-lookup"><span data-stu-id="374d9-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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
