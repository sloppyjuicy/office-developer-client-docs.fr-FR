---
title: Utilisation de Microsoft Access en tant que serveur DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access prend en charge l'échange dynamique de données (DDE) à la fois comme application de destination (client) et comme application source (serveur).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 2b22ed9b6c85f8cfe3d6374c0b882048741d6b96
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464896"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Utilisation de Microsoft Access en tant que serveur DDE

**S’applique à** : Access 2013, Office 2013 

Microsoft Access prend en charge l'échange dynamique de données (DDE) à la fois comme application de destination (client) et comme application source (serveur). Par exemple, une application telle que Microsoft Word, représentant le client, peut utiliser l'échange dynamique de données pour demander des données à une base de données Microsoft Access, représentant le serveur.

> [!TIP]
> [!CONSEIL] Si vous souhaitez manipuler des objets Microsoft Access à partir d'une autre application, il est peut-être préférable de recourir à l'automation.

Une conversation DDE entre un client et un serveur est établie sur un sujet spécifique. Ce sujet est soit un fichier de données qui utilise le format reconnu par l'application serveur, soit le sujet System qui fournit les informations relatives à l'application serveur elle-même. Une fois qu’une conversation a commencé sur un sujet particulier, seul un élément de données associé à cette rubrique peut être transféré.

Par exemple, supposez que Microsoft Word pour Windows est en cours d'exécution et que vous souhaitez insérer des données d'une base de données Microsoft Access particulière dans un document. Vous entamez une conversation DDE avec Microsoft Access en ouvrant un canal DDE à l'aide de la fonction **DDEInitiate** et en spécifiant le nom du fichier de base de données comme sujet. Vous pouvez alors transférer des données de cette base de données vers Microsoft Word à travers ce canal.

En tant que serveur DDE, Microsoft Access reconnaît les sujets suivants :

- Le sujet System

- Le nom d'une base de données (sujet *base-de-données*)

- Le nom d'une table (sujet *nom-table*)

- Le nom d'une requête (sujet *nom-requête*)

- Une instruction Microsoft Access SQL (sujet *chaîne-sql*)

Après avoir établi une conversation DDE, vous pouvez utiliser l’instruction **DDEExecute** pour envoyer une commande du client à l’application serveur. Lorsqu'il est utilisé comme serveur DDE, Microsoft Access reconnaît, comme commande valide, n'importe lequel des éléments suivants :

- Le nom d'une macro dans la base de données en cours.

- N'importe quelle action que vous pouvez exécuter en Visual Basic au moyen d'une des méthodes de l'objet **DoCmd**.

- Les actions OuvrirBase et FermerBase, qui ne sont utilisées que pour l'échange dynamique de données (pour savoir comment utiliser ces actions, voyez l'exemple plus loin sous cette rubrique).

> [!NOTE]
> [!REMARQUE] Lorsque vous spécifiez une action de macro comme instruction **DDEExecute**, l'action et les arguments éventuels suivent la syntaxe de **DoCmd** et doivent être entourés de crochets ([ ]). Toutefois, les applications qui prennent en charge DDE ne reconnaissent pas les constantes intrinsèques dans les opérations DDE. De même, les arguments de type chaîne de caractères doivent être entourés de guillemets doubles (" ") si la chaîne renferme une virgule. Dans tous les autres cas, les guillemets doubles sont superflus.

L'application client peut utiliser la fonction **DDERequest** pour demander des données textuelles à l'application serveur sur un canal DDE ouvert. Elle peut également utiliser l'instruction **DDEPoke** pour envoyer des données à l'application serveur. Une fois le transfert de données terminé, le client peut utiliser l’instruction **DDETerminate** pour fermer le canal DDE ou l’instruction **DDETerminateAll** pour fermer tous les canaux ouverts.

> [!NOTE]
> [!REMARQUE] Lorsque la réception de données par votre application client à travers un canal DDE est terminée, il est préférable de fermer ce canal afin de ne pas épuiser la mémoire et les ressources du système.

L'exemple suivant montre comment créer avec Visual Basic une procédure Microsoft Word qui utilise Microsoft Access comme serveur DDE (pour que cet exemple fonctionne, Microsoft Access doit être actif) :

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```


Les sections suivantes vous informent sur les sujets DDE valides pris en charge par Microsoft Access.

## <a name="the-system-topic"></a>Le sujet System

La rubrique System est une rubrique standard pour toutes les applications Microsoft Windows basées sur un logiciel. It supplies information about the other topics supported by the application. Pour accéder à ces informations, votre code doit d’abord appeler la fonction **DDEInitiate** avec *l’argument sujet* , puis exécuter l’instruction **DDERequest** avec l’une des instructions suivantes fournies pour l’argument *élément* .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Retourne</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Une liste d'éléments pris en charge par le sujet System dans Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Formats</p></td>
<td><p>Une liste des formats que Microsoft Access peut copier dans le Presse-papiers.</p></td>
</tr>
<tr class="odd">
<td><p>État</p></td>
<td><p>&quot;Occupé&quot; ou &quot;prêt&quot;.</p></td>
</tr>
<tr class="even">
<td><p>Rubriques</p></td>
<td><p>Une liste de toutes les bases de données ouvertes.</p></td>
</tr>
</tbody>
</table>


L'exemple suivant montre comment utiliser les fonctions **DDEInitiate** et **DDERequest** avec le sujet System :

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a>Rubrique sur la base de données

Le sujet *base-de-données* contient le nom de fichier d'une base de données existante. Vous pouvez taper uniquement le nom de base (Northwind) ou son chemin d’accès et son extension .mdb (C:\\AccessSamplesNorthwind.mdb\\\\). Une fois que vous avez engagé une conversation DDE avec la base de données, vous pouvez demander une liste des objets contenus dans celle-ci.

> [!NOTE]
> Vous ne pouvez pas recourir à l'échange dynamique de données (DDE) pour interroger le fichier d'information du groupe de travail.

Le sujet *base-de-données* prend en charge les éléments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Retourne</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TableList</p></td>
<td><p>Une liste de tableaux</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Une liste de requêtes</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Une liste de formulaires</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Une liste de rapports</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Une liste de macros</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Une liste de modules</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Une liste d'affichages.</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Une liste de procédures enregistrées.</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Une liste de schémas de base de données.</p></td>
</tr>
</tbody>
</table>


L'exemple suivant montre comment ouvrir le formulaire Employés de la base de données Les comptoirs à l'aide d'une procédure Visual Basic :

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a>Rubrique TABLE

Ces sujets utilisent la syntaxe suivante :

_databasename_ ; **TABLE** _tablename_

_databasename_ ; **QUERY** _queryname_

_databasename_ ; **SQL** [ _sqlstring_ ]


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
<td><p><em>databasename</em></p></td>
<td><p>Le nom de la base de données contenant la table ou la requête à laquelle s'applique l'instruction SQL, suivi d'un point-virgule (;). Le nom de la base de données peut se présenter sous la forme la plus simple (Comptoir) ou sous la forme du nom complet avec chemin d'accès et extension .mdb (C:\Access\Samples\Comptoir.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
<td><p>Le nom d'une table existante.</p></td>
</tr>
<tr class="odd">
<td><p><em>queryname</em></p></td>
<td><p>Le nom d'une requête existante.</p></td>
</tr>
<tr class="even">
<td><p><em>sqlstring</em></p></td>
<td><p>Une instruction SQL valide pouvant compter jusqu'à 256 caractères et se terminant par un point-virgule. Pour échanger plus de 256 caractères, omettez cet argument et créez une instruction SQL au moyen de plusieurs instructions <strong>DDEPoke</strong> successives. Par exemple, le code Visual Basic suivant crée une instruction SQL au moyen de <strong>DDEPoke</strong>, puis demande le résultat de la requête.</p></td>
</tr>
</tbody>
</table>


Le tableau ci-dessous énumère les éléments valides pour les sujets TABLE *nom-table*, QUERY *nom-requête* et SQL *chaîne-sql*.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Item</p></th>
<th><p>Retourne</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tous</p></td>
<td><p>Toutes les données contenues dans la table, y compris les noms de champs.</p></td>
</tr>
<tr class="even">
<td><p>Données</p></td>
<td><p>Toutes les lignes de données, sans les noms de champs.</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>Une liste d'une seule ligne reprenant les noms de champs.</p></td>
</tr>
<tr class="even">
<td><p>FieldNames; T</p></td>
<td><p>Une liste de deux lignes reprenant les noms de champs (première ligne) et leurs types de données (seconde ligne).</p>
<p>Voici les valeurs renvoyées :</p>
<p>Valeur</p>
<p><ul>
<li>0</li>
<li>1</li>
<li>2</li>
<li>3</li>
<li>4</li>
<li>5</li>
<li>6 </li>
<li>7 </li>
<li>8 </li>
<li>9 </li>
<li>10</li>
<li>11</li>
<li>12 </li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Les données contenues dans la ligne suivante de la table ou de la requête. Lorsque vous ouvrez un canal, NextRow retourne les données dans la première ligne. Si la ligne en cours est le dernier enregistrement et si vous exécutez NextRow, l'appel échoue.</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>Les données contenues dans la ligne précédente de la table ou de la requête. Si PrevRow est le premier appel sur un nouveau canal, les données contenues dans la dernière ligne de la table ou de la requête sont retournées. Si le premier enregistrement est la ligne en cours, l'appel PrevRow échoue..</p></td>
</tr>
<tr class="even">
<td><p>FirstRow</p></td>
<td><p>Les données contenues dans la première ligne de la table ou de la requête.</p></td>
</tr>
<tr class="odd">
<td><p>LastRow</p></td>
<td><p>Les données contenues dans la dernière ligne de la table ou de la requête.</p></td>
</tr>
<tr class="even">
<td><p>FieldCount</p></td>
<td><p>Le nombre de champs dans la table ou la requête.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>Une instruction SQL représentant la table ou la requête. Pour les tableaux, cet élément renvoie une SQL sous la &quot;forme SELECT `*` FROM <em>table</em>;&quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText ; <em>n</em></p></td>
<td><p>Une instruction SQL, en segments de <em>n</em> caractères, représentant la table ou la requête, où <em>n</em> est un nombre entier dont la valeur ne peut dépasser 256. Par exemple, supposons qu’une requête est représentée par l’instruction SQL &quot;suivante : L’élément SQLText ;7&quot; renvoie les blocs délimités par des tabulations suivants &quot;: L’élément SQLText ;7&quot; renvoie les blocs délimités par des tabulations suivants :</p></td>
</tr>
</tbody>
</table>


L'exemple suivant montre comment utiliser l'échange dynamique de données (DDE) dans une procédure Visual Basic pour demander des données d'une table de la base de données exemple Comptoirs et insérer ces données dans un fichier texte :

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
