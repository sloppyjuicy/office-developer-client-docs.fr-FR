---
title: ImportExportData, action de macro
TOCTitle: ImportExportData macro action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 847f23c429b06fee51b42aa211d672b051accb7c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920395"
---
# <a name="importexportdata-macro-action"></a>ImportExportData, action de macro

**S’applique à**: Access 2013, Office 2013

L'action **ImporterExporterDonnées** permet d'importer ou d'exporter des données entre la base de données Access (.mdb ou .accdb) active, ou le projet Access (.adp) actif et une autre base de données. Pour les bases de données Microsoft Access, vous pouvez également attacher une table à la base de données Access active, à partir d'une autre base de données. Avec une table attachée, vous pouvez accéder aux données de la table sans déplacer celle-ci de l'autre base de données.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.

## <a name="settings"></a>Paramètres

L'action **ImporterExporterDonnées** utilise les arguments suivants :

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
<td><p>Type de transfert à effectuer. Sélectionnez <strong>Importation</strong>, <strong>Exportation</strong>, ou <strong>Attache</strong> dans la zone <strong>Type de transfert</strong> de la section <strong>Arguments de l'action</strong> du Générateur de macro. La valeur par défaut est <strong>Importation</strong>.  </p>

> [!NOTE]
> Le type de transfert **Attache** n’est pas pris en charge dans les projets Access (.adp).


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Type de base de données</strong></p></td>
<td><p>Type de base de données à partir de laquelle ou vers laquelle vous souhaitez importer, exporter ou attacher des éléments. Vous pouvez sélectionner <strong>Microsoft Access</strong>, ou l'un des nombreux autres types de base de données dans la zone <strong>Type de base de données</strong>. La valeur par défaut est <strong>Microsoft Access</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nom de la base de données</strong></p></td>
<td><p>Nom de la base de données à partir de laquelle importer, vers laquelle exporter ou à laquelle attacher des données. Inclut le chemin d'accès complet. Il s'agit d'un argument obligatoire. Pour les types de bases de données utilisant des fichiers distincts pour chaque table, telles que FoxPro, Paradox et dBASE, entrez le nom du répertoire contenant le fichier. Entrez le nom de fichier dans l'argument <strong>Source</strong> (pour l'importation ou l'attachement de données) ou l'argument <strong>Destination</strong> (pour l'exportation). Pour les bases de données ODBC, entrez la chaîne de connexion ODBC (Open Database Connectivity) complète.  </p>
<p>Pour visualiser un exemple de chaîne de connexion, attachez une table externe à Access :</p>
<ol>
<li><p>Dans la boîte de dialogue <strong>Données externes</strong>, entrez le chemin d'accès à votre base de données source dans le champ <strong>Nom de fichier</strong>.</p></li>
<li><p>Cliquez sur <strong>Lier à la source de données en créant une table attachée</strong>, puis cliquez sur <strong>OK</strong>.</p></li>
<li><p>Sélectionnez une table dans la boîte de dialogue <strong>Attacher les tables</strong>, puis cliquez sur <strong>OK</strong>.</p></li>
</ol>
<p>Ouvrez la table attachée en mode Création et affichez les propriétés de la table en cliquant sur <strong>Feuille de propriétés</strong> sous l'onglet <strong>Créer</strong> du groupe <strong>Outils</strong>. Le texte affiché dans le paramètre de propriété <strong>Description</strong> est la chaîne de connexion de cette table.  </p>
<p>Pour plus d’informations sur les chaînes de connexion ODBC, consultez le fichier d’aide ou la documentation du pilote ODBC de ce type de base de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Type d'objet</strong></p></td>
<td><p>Type de l'objet à exporter ou à importer. Si vous sélectionnez <strong>Microsoft Access</strong> comme argument <strong>Type de base de données</strong>, vous pouvez sélectionner <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d'accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d'objet</strong>. La valeur par défaut est <strong>Table</strong>. Si vous sélectionnez un autre type de base de données, ou si vous sélectionnez <strong>Lien</strong> dans la zone <strong>Type de transfert</strong>, cet argument sera ignoré. Si vous exportez une requête sélectionnée vers une base de données Access, sélectionnez <strong>Table</strong> dans cet argument pour exporter le jeu de résultats de la requête et sélectionnez <strong>Requête</strong> pour exporter la requête elle-même. Si vous exportez une requête sélectionnée vers un autre type de base de données, cet argument est ignoré et le jeu de résultats de la requête est exporté.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Nom de la table, de la requête Sélection ou de l'objet Access à importer, exporter, ou attacher. Pour certains types de bases de données, telles que FoxPro, Paradox ou dBASE, il s'agit d'un nom de fichier. Entrez l'extension du nom de fichier (par exemple, .dbf) dans le nom de fichier. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Destination</strong></p></td>
<td><p>Nom de la table importée, exportée ou liée, de la requête sélectionnée ou d'un objet Access dans la base de données de destination. Pour certains types de bases de données, telles que FoxPro, Paradox ou dBASE, il s'agit d'un nom de fichier. Inclut l'extension du nom de fichier (par exemple .dbf) dans le nom de fichier. Il s'agit d'un argument obligatoire. Si vous sélectionnez <strong>Importer</strong> dans l'argument <strong>Type de transfert</strong> et <strong>Table</strong> dans l'argument <strong>Type d'objet</strong>, Access crée une nouvelle table contenant les données de la table importée. Si vous importez une table ou un autre objet, Access ajoute un numéro au nom en cas de conflit avec un nom existant. Par exemple, si vous importez la table Employés, mais que la table Employés existe déjà, Access renomme Employés1 la table importée ou tout autre objet importé. Si vous exportez vers une base de données Access ou une autre base de données, Access remplace automatiquement toute table ou tout objet existant qui porte le même nom.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Structure seulement</strong></p></td>
<td><p>Spécifie s'il faut importer ou exporter uniquement la structure d'une table de base de données, sans ses données. Sélectionnez <strong>Oui</strong> ou <strong>Non</strong>. La valeur par défaut est <strong>Non</strong>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez importer et exporter des tables entre Access et d'autres types de base de données. Vous pouvez également exporter des requêtes Sélection Access dans d'autres types de base de données. Access exporte le jeu de résultats de la requête dans le formulaire d'une table. Vous pouvez importer et exporter des objets de base de données Access, s'il s'agit de deux bases de données Access.

Si vous importez une table d'une autre base de données Access (.mdb ou .accdb) qui est attachée dans cette base, elle reste attachée même après son importation, c'est-à-dire que le lien est importé et pas la table.

Si la base de données cible requiert un mot de passe, une boîte de dialogue s'affiche lors de l'exécution de la macro. Tapez le mot de passe dans cette boîte de dialogue.

L'action **ImporterExporterDonnées** est similaire aux commandes de l'onglet **Données externes**, sous **Importer** ou **Exporter**. Vous pouvez utiliser ces commandes pour sélectionner une source de données, par exemple une base de données Access ou un autre type de base de données, une feuille de calcul ou un fichier texte. Si vous sélectionnez une base de données, une ou plusieurs boîtes de dialogue s'afficheront pour vous permettre de sélectionner le type d'objet à importer ou exporter (pour les bases de données Access), le nom de l'objet et d'autres options, selon la base de données à partir de laquelle vous importez ou vers laquelle vous exportez ou attachez des éléments. Les arguments de l'action **ImporterExporterDonnées** reflètent les options dans ces boîtes de dialogue.

Pour renseigner des informations d'index pour une table dBASE attachée, attachez d'abord la table :

1.  Cliquez sur **Fichier dBASE**.

2.  Dans la boîte de dialogue **Données externes**, entrez le chemin d'accès au fichier dBASE dans le champ **Nom de fichier**.

3.  Cliquez sur **Lier à la source de données en créant une table attachée**, puis cliquez sur **OK**.

4.  Spécifiez les index dans les boîtes de dialogue pour cette commande. Access stocke les informations d'index dans un fichier spécial d'informations (.inf), situé dans le dossier Microsoft Office.

5.  Vous pouvez ensuite supprimer le lien vers la table attachée.

La prochaine fois que vous utiliserez l'action **ImporterExporterDonnées** pour lier cette table dBASE, Access utilisera automatiquement les informations d'index que vous avez spécifiées.

> [!NOTE]
> [!REMARQUE] Si vous interrogez ou filtrez une table attachée, la requête ou le filtre respecte la casse.

Pour exécuter l'action **ImporterExporterDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferDatabase** de l'objet **DoCmd**.

