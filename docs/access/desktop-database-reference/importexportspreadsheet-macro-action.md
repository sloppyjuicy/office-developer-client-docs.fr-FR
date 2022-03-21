---
title: ImportExportSpreadsheet, action de macro
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: cfda0a704422a61cbf9a4ef9c71010566a8f052d
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630629"
---
# <a name="importexportspreadsheet-macro-action"></a>ImportExportSpreadsheet, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **ImporterExporterFeuilleDeCalcul** permet d'importer ou d'exporter des données entre la base de données Access (.mdb ou .accdb) ou le projet Access (.adp) actif et un fichier de feuille de calcul. Vous pouvez également lier les données figurant dans une feuille de calcul Microsoft Excel dans la base de données Access active. Avec une feuille de calcul attachée, vous pouvez afficher et modifier les données de la feuille dans Access, tout en garantissant l'accès aux données à partir de la feuille de calcul Excel. Vous pouvez aussi attacher les données d'un fichier de feuille de calcul Lotus 1-2-3, mais elles seront en lecture seule dans Access.

> [!NOTE]
> Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **TransferSpreadsheet** comporte les arguments suivants.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Type de transfert</strong></p></td>
<td><p>Type de transfert à effectuer. Sélectionnez <strong>Importation</strong>, <strong>Exportation</strong>, ou <strong>Attache</strong> dans la zone <strong>Type de transfert</strong> de la section <strong>Arguments de l'action</strong> du Générateur de macro. La valeur par défaut est <strong>Importation</strong>.  </p><p><strong>REMARQUE</strong> : le type de transfert <STRONG>Link</STRONG> n’est pas pris en charge pour les projets Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Type de feuille de calcul</strong></p></td>
<td><p>Type de feuille de calcul à partir de laquelle effectuer l'importation, vers laquelle effectuer l'exportation ou à laquelle attacher les données. Vous pouvez sélectionner un des types de feuilles de calcul dans la zone concernée. La valeur par défaut est <strong>Classeur Excel</strong>.  </p><p><strong>REMARQUE</strong> : Vous pouvez importer et lier (en lecture seule) des fichiers Lotus .WK4, mais vous ne pouvez pas exporter des données Access vers ce format de feuille de calcul. Access ne prend également plus en charge l'importation, l'exportation ou la liaison de données à partir de feuilles de calcul Lotus .WKS ou Excel version 2.0 avec cette action. Si vous souhaitez importer ou lier des données de feuilles de calcul au format Excel version 2.0 ou Lotus .WKS, convertissez les données de la feuille de calcul dans une version ultérieure d'Excel ou de Lotus 1-2-3 avant d'importer ou de lier les données dans Access.</p>
</td>
</tr>
<tr class="odd">
<td><p><strong>Nom de la table</strong></p></td>
<td><p>Nom de la table Access dans laquelle importer des données de feuille de calcul, vers laquelle exporter des données de feuille de calcul ou avec laquelle attacher des données de feuille de calcul. Vous pouvez également taper le nom de la requête Sélection Access à partir de laquelle vous souhaitez exporter les données. Il s'agit d'un argument obligatoire. Si vous sélectionnez <strong>Import</strong> dans l'argument <strong>Type de transfert</strong>, Access ajoute les données de feuille de calcul à cette table si la table existe déjà. Dans le cas contraire, Access crée une table contenant les données de feuille de calcul. Dans Access, vous ne pouvez pas utiliser une instruction SQL pour spécifier les données à exporter si vous utilisez l'action <strong>ImportExportSpreadsheet</strong>. Au lieu d'utiliser une instruction SQL, vous devez d'abord créer une requête, puis spécifier le nom de la requête dans l'argument <strong>Nom de la table</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de fichier</strong></p></td>
<td><p>Nom du fichier de feuille de calcul à partir duquel importer, vers lequel exporter ou auquel attacher des données. Inclut le chemin d'accès complet. Il s'agit d'un argument obligatoire. Access crée une feuille de calcul lorsque vous exportez des données provenant d'Access. Si le nom de fichier est identique au nom d'une feuille de calcul existante, Access remplace la feuille de calcul existante, sauf si vous exportez des données vers un classeur Excel version 5.0 ou ultérieure. Dans ce cas, Access copie les données exportées dans la feuille de calcul suivante disponible dans le classeur. Si vous importez ou attachez des données à partir d'une feuille de calcul Excel version 5.0 ou ultérieure, vous pouvez spécifier une feuille de calcul particulière en utilisant l'argument <strong>Range</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Contient les noms de champs</strong></p></td>
<td><p>Spécifie si la première ligne de la feuille de calcul contient les noms de champs. Si vous sélectionnez <strong>Oui</strong>, Access utilise les noms de cette ligne en tant que noms de champs dans la table Access lors de l'importation ou de la liaison des données de la feuille de calcul. Si vous sélectionnez <strong>Non</strong>, Access considère la première ligne comme une ligne de données normale. La valeur par défaut est <strong>Non</strong>. Lorsque vous exportez une table Access ou une requête Sélection vers une feuille de calcul, les noms des champs sont insérés à la première ligne de la feuille de calcul, que vous ayez sélectionné ou non cet argument.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Range</strong></p></td>
<td><p>Plage de cellules à importer ou attacher. Laissez cet argument vierge pour importer ou attacher la feuille de calcul entière. Vous pouvez taper le nom d'une plage dans la feuille de calcul, ou spécifier la plage de cellules à importer ou attacher, par exemple, A1:E25 (notez que la syntaxe A1..E25 ne fonctionne pas dans Access 97 ou une version ultérieure). Si l'importation ou la liaison s'effectue vers une feuille de calcul Excel version 5.0 ou ultérieure, vous pouvez faire précéder la plage du nom de la feuille de calcul, suivi d'un point d'exclamation, par exemple : Budget!A1:C7.</p><p><strong>REMARQUE</strong> : Lorsque vous exportez vers une feuille de calcul, vous devez laisser cet argument vide. Si vous entrez une plage, l'exportation échouera.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez exporter les données figurant dans des requêtes Sélection Access dans des feuilles de calcul. Access exporte le jeu de résultats de la requête comme s'il s'agissait d'une table.

Les données de la feuille de calcul que vous ajoutez à une table Access existante doivent être compatibles avec la structure de la table.

- Le type de données de chaque champ de la feuille de calcul doit être identique à celui du champ correspondant dans la table.

- Les champs doivent être positionnés dans le même ordre, sauf si l'argument **Contient les noms de champs** est défini sur **Oui**, auquel cas les noms de champs de la feuille de calcul doivent correspondre aux noms de champs de la table.

Exécuter cette action équivaut à cliquer sur l'onglet **Données externes**, puis sur **Excel** dans le groupe **Importation** ou **Exportation**, ou à cliquer sur **Plus** dans le groupe **Importation** ou **Exportation**, puis sur **Fichier Lotus 1-2-3**. Vous pouvez utiliser ces commandes pour sélectionner une source de données telle qu'Access ou un type de base de données, de feuille de calcul ou de fichier texte. Si vous sélectionnez une feuille de calcul, une série de boîtes de dialogue s'affichent ou un Assistant Access s'exécute pour vous permettre de sélectionner le nom de la feuille de calcul et d'autres options. Les arguments de l'action **ImporterExporterFeuilleDeCalcul** reflètent les options de ces boîtes de dialogue ou de cet Assistant.

> [!NOTE]
> Si vous interrogez ou filtrez une feuille de calcul liée, la requête ou le filtre respecte la casse.

Si la liaison s'effectue vers une feuille de calcul Excel ouverte en mode d'édition, Access n'effectuera la liaison que lorsque la feuille de calcul quittera ce mode (aucun délai).

Pour exécuter l'action **ImporterExporterFeuilleDeCalcul** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferSpreadsheet** de l'objet **DoCmd**.

