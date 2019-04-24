---
title: ImportExportText, action de macro
TOCTitle: ImportExportText macro action
ms:assetid: 366fa095-6f09-7c22-e734-bfa585cfe79e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192475(v=office.15)
ms:contentKeyID: 48544171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168097
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a26b370e14dba68b0cbe686f4b23ae0db3fc1fea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291865"
---
# <a name="importexporttext-macro-action"></a>ImportExportText, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **ImporterExporterTexte** permet d'importer ou d'exporter du texte entre la base de données Microsoft Access (.mdb ou .accdb) ou le projet Access (.adp) actif et un fichier texte. Vous pouvez également lier les données d'un fichier texte à la base de données Access en cours. Avec un fichier texte lié, vous pouvez consulter les données de texte avec Access, tout en autorisant un accès complet aux données de votre programme de traitement de texte. Vous pouvez également importer de, exporter vers et créer un lien vers une table ou une liste dans un fichier\*html (. html).

> [!NOTE]
> [!REMARQUE] Si la liaison de données s'effectue dans un fichier texte ou dans un fichier HTML, les données seront en lecture seule dans Access. Cette action ne sera pas autorisée si la base de données n’est pas approuvée. 

## <a name="setting"></a>Paramètre

L’action **ImporterExporterTexte** utilise les arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>Type de transfert à effectuer. Vous pouvez importer des données de, exporter des données dans, ou lier des données à des fichiers textes délimités ou à des fichiers textes de longueur fixe ou des fichiers HTML. Vous pouvez également exporter des données dans un fichier de publipostage Microsoft Word, que vous pourrez ensuite utiliser avec la fonction de publipostage de Microsoft Word pour créer des documents fusionnés tels que des lettres types et des étiquettes de publipostage. Sélectionnez <strong>Importation texte (délimité)</strong>, <strong>Importation texte (longueur fixe)</strong>, <strong>Importation HTML</strong>, <strong>Exportation texte (délimité)</strong>, <strong>Exportation texte (longueur fixe)</strong>, <strong>Exportation HTML</strong>, <strong>Fusion avec Word pour Windows</strong>, <strong>Liaison texte (délimité)</strong>, <strong>Liaison texte (longueur fixe)</strong> ou <strong>Liaison HTML</strong> dans la zone <strong>Type de transfert</strong> dans la section <strong>Arguments de l'action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Importation texte (délimité)</strong>.  </p><p><strong>Remarque</strong>: seuls les types de transfert <STRONG>importation</STRONG>texte (délimité), importation texte <STRONG></STRONG>( <STRONG>longueur fixe</STRONG>), <STRONG>exportation</STRONG>texte (longueur fixe), exportation texte (longueur fixe) ou <STRONG>exportation Word pour Windows fusionnent</STRONG> sont pris en charge dans un projet Access (. ADP).</p></td>
</tr>
<tr class="even">
<td><p><strong>Format</strong></p></td>
<td><p>Format du groupe d'options définissant le mode d'importation ou de liaison d'un fichier texte. Dans le cas d'un fichier texte de longueur fixe, vous devez spécifier un argument ou utiliser un fichier schema.ini, qui doit être stocké dans le même dossier que le fichier texte importé, attaché ou exporté.  </p>
<p>Pour créer une spécification d'importation ou de liaison d'un fichier texte, procédez comme suit :</p>
<ol>
<li><p>Dans la boîte de dialogue <strong>Données externes</strong>, entrez le chemin d'accès au fichier texte source dans le champ <strong>Nom de fichier</strong>.</p></li>
<li><p>Sélectionnez l'option de stockage des données (importation, ajout ou liaison), puis cliquez sur <strong>OK</strong>.</p></li>
<li><p>Dans la boîte de dialogue <strong>Assistant Importation de texte</strong>, cliquez sur <strong>Options avancées</strong>.</p></li>
<li><p>Spécifiez les options souhaitées pour cette spécification, puis cliquez sur <strong>Enregistrer sous</strong>.</p></li>
<li><p>Entrez le nom souhaité pour la spécification, puis cliquez sur <strong>OK</strong>.</p></li>
<li><p>Vous pouvez gérer les spécifications existantes en cliquant sur <strong>Paramètres</strong> dans la boîte de dialogue de spécification.</p></li>
<li><p>Cliquez sur <strong>OK</strong> pour fermer la boîte de dialogue de spécification.</p></li>
</ol>
<p></p>
<p>Vous pouvez ensuite entrer le nom de la spécification dans cet argument, dès que vous voulez importer ou exporter le même type de fichier texte. Vous pouvez importer, exporter ou lier des fichiers texte délimités sans entrer de nom de spécification pour cet argument. Dans ce cas, Access utilise les valeurs par défaut définies dans la boîte de dialogue de l'assistant. Access utilise un format prédéfini pour les fichiers de publipostage, ce qui vous évite de devoir entrer un nom de spécification pour cet argument lors de l'exportation de ce type de fichiers. Vous pouvez utiliser les spécifications d'importation et d'exportation avec les fichiers HTML, mais la spécification relative à la mise en forme du type de données sera la seule appliquée.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nom de la table</strong></p></td>
<td><p>Nom de la table Access dans laquelle importer des données texte, à partir de laquelle exporter des données texte ou à laquelle lier des données texte. Vous pouvez également entrer le nom de la requête Access à partir de laquelle vous souhaitez exporter les données. Il s'agit d'un argument obligatoire. Si vous cliquez sur <strong>Importation texte (délimité)</strong>, <strong>Importation texte (longueur fixe)</strong> ou <strong>Importation HTML</strong> dans la zone <strong>Type de transfert</strong>, Access ajoute les données texte à cette table si la table existe déjà. Si elle n'existe pas encore, Access crée une table contenant les données texte. Vous ne pouvez pas utiliser d'instruction SQL pour spécifier les données à exporter si vous utilisez l'action <strong>ImportExportText</strong>. Au lieu d'utiliser une instruction SQL, vous devez d'abord créer une requête, puis spécifier le nom de la requête dans l'argument <strong>Nom de la table</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nom du fichier</strong></p></td>
<td><p>Nom du fichier texte à partir duquel importer les données, vers lequel exporter les données ou auquel lier les données. Incluez le chemin d'accès complet. Il s'agit d'un argument obligatoire. Access crée un fichier texte lorsque vous exportez des données à partir d'Access. Si le nom de fichier est le même que le nom d'un fichier texte existant, Access remplace le fichier texte existant. Si vous souhaitez importer ou lier une table ou une liste en particulier dans un fichier HTML, vous pouvez utiliser l'argument <strong>Nom de la table HTML</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Contient les noms de champs</strong></p></td>
<td><p>Spécifie si la première ligne du fichier texte contient les noms des champs. Si vous sélectionnez <strong>Oui</strong>, Access utilise les noms figurant sur cette ligne comme noms de champs dans la table Access lorsque vous importez ou liez les données texte. Si vous sélectionnez <strong>Non</strong>, Access traite la première ligne comme une ligne de données normale. La valeur par défaut est <strong>Non</strong>.<br/><br/>Access ignore cet argument pour les fichiers de publipostage Word pour Windows, car la première ligne doit contenir les noms de champs. Lorsque vous exportez une table Access ou une requête sélectionnée vers un fichier texte délimité ou de longueur fixe, Access insère les noms de champs de votre table ou requête sélectionnée dans la première ligne du fichier texte si vous avez sélectionné <strong>Oui</strong> pour cet argument.<br/><br/>Si vous importez ou liez un fichier texte de longueur fixe et sélectionnez <strong>Oui</strong> dans cette zone, la première ligne contenant les noms de champs doit utiliser le séparateur de champ défini dans la spécification d'importation/exportation pour séparer les noms de champs. Si vous exportez des données vers un fichier texte de longueur fixe et sélectionnez <strong>Oui</strong> pour cet argument, Access insère les noms de champs dans la première ligne du fichier texte avec ce séparateur.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de la table HTML</strong></p></td>
<td><p>The name of the table or list in the HTML file that you want to import or link. This argument is ignored unless the <strong>Transfer Type</strong> argument is set to Import HTML or Link HTML. If you leave this argument blank, the first table or list in the HTML file is imported or linked. <br/><br/>Le nom de la table ou de la liste dans le fichier HTML est déterminé par le &lt;texte&gt; spécifié par la balise Caption &lt;,&gt; s'il existe une balise Caption. S’il n’y a aucune balise &lt;CAPTION&gt;, le nom est déterminé selon le texte spécifié par la balise &lt;TITLE&gt;. If more than one table or list has the same name, Access distinguishes them by adding a number to the end of each name; for example, Employees1 and Employees2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Page de codes</strong></p></td>
<td><p>Nom du jeu de caractères utilisé dans la page de codes.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez exporter des données figurant dans des requêtes Sélection Access vers des fichiers texte. Access exporte le jeu de résultats de la requête comme s'il s'agissait d'une table.

Les données de texte que vous ajoutez à une table Access existante doivent être compatibles avec la structure de la table.

- Le type de données de chaque champ du texte doit être identique à celui du champ correspondant dans la table.

- Les champs doivent être positionnés dans le même ordre, sauf si l'argument **Contient les noms de champs** est défini sur **Oui**, auquel cas les noms de champs du texte doivent correspondre aux noms de champs de la table.

L'exécution de cette action équivaut à cliquer sur **Fichier texte** dans le groupe **Importation** ou **Exportation** de l'onglet **Données externes**. Les arguments de l'action **ImporterExporterTexte** reflètent les options de l'Assistant exécuté par la commande **Fichier texte**.

> [!TIP]
> [!CONSEIL] La spécification d'importation ou d'exportation stocke les informations nécessaires à Access pour importer, exporter ou attacher un fichier texte. Vous pouvez utiliser les spécifications stockées pour importer, exporter ou attacher des données textuelles depuis ou vers des fichiers texte similaires. Par exemple, si vous recevez les chiffres de vente hebdomadaires de votre société dans un fichier texte provenant d'un ordinateur central, vous pouvez créer et enregistrer une spécification pour ce type de données, puis utiliser cette spécification lors de l'ajout de ces données dans votre base de données Access.

> [!NOTE]
> [!REMARQUE] Si vous interrogez ou filtrez un fichier texte lié, la requête ou le filtre respecte la casse.

Pour exécuter l'action **ImporterExporterTexte** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferText** de l'objet **DoCmd**.

