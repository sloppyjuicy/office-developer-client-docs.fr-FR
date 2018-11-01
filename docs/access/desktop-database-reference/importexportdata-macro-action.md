---
title: ImporterExporterDonnées, action de macro
TOCTitle: ImportExportData Macro Action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 62a496867852afb89d5b556f6be793f3f8c3739e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887781"
---
# <a name="importexportdata-macro-action"></a><span data-ttu-id="b064f-102">ImporterExporterDonnées, action de macro</span><span class="sxs-lookup"><span data-stu-id="b064f-102">ImportExportData Macro Action</span></span>

<span data-ttu-id="b064f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b064f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b064f-p101">L'action **ImporterExporterDonnées** permet d'importer ou d'exporter des données entre la base de données Access (.mdb ou .accdb) active, ou le projet Access (.adp) actif et une autre base de données. Pour les bases de données Microsoft Access, vous pouvez également attacher une table à la base de données Access active, à partir d'une autre base de données. Avec une table attachée, vous pouvez accéder aux données de la table sans déplacer celle-ci de l'autre base de données.</span><span class="sxs-lookup"><span data-stu-id="b064f-p101">You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database. For Microsoft Access databases, you can also link a table to the current Access database from another database. With a linked table, you have access to the table's data while the table itself remains in the other database.</span></span>

> [!NOTE]
> <span data-ttu-id="b064f-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="b064f-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="settings"></a><span data-ttu-id="b064f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b064f-109">Settings</span></span>

<span data-ttu-id="b064f-110">L'action **ImporterExporterDonnées** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b064f-110">The **ImportExportData** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b064f-111">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="b064f-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b064f-112">Description</span><span class="sxs-lookup"><span data-stu-id="b064f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b064f-113"><strong>Type de transfert</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-113"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p103">Type de transfert à effectuer. Sélectionnez <strong>Importation</strong>, <strong>Exportation</strong>, ou <strong>Attache</strong> dans la zone <strong>Type de transfert</strong> de la section <strong>Arguments de l'action</strong> du Générateur de macro. La valeur par défaut est <strong>Importation</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p103">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="b064f-117">Le type de transfert **Attache** n’est pas pris en charge dans les projets Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="b064f-117">The **Link** transfer type is not supported for Access projects (.adp).</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b064f-118"><strong>Type de base de données</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-118"><strong>Database Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p104">Type de base de données à partir de laquelle ou vers laquelle vous souhaitez importer, exporter ou attacher des éléments. Vous pouvez sélectionner <strong>Microsoft Access</strong>, ou l'un des nombreux autres types de base de données dans la zone <strong>Type de base de données</strong>. La valeur par défaut est <strong>Microsoft Access</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p104">The type of database to import from, export to, or link to. You can select <strong>Microsoft Access</strong> or one of a number of other database types in the <strong>Database Type</strong> box. The default is <strong>Microsoft Access</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b064f-122"><strong>Nom de la base de données</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-122"><strong>Database Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p105">Nom de la base de données à partir de laquelle importer, vers laquelle exporter ou à laquelle attacher des données. Inclut le chemin d'accès complet. Il s'agit d'un argument obligatoire. Pour les types de bases de données utilisant des fichiers distincts pour chaque table, telles que FoxPro, Paradox et dBASE, entrez le nom du répertoire contenant le fichier. Entrez le nom de fichier dans l'argument <strong>Source</strong> (pour l'importation ou l'attachement de données) ou l'argument <strong>Destination</strong> (pour l'exportation). Pour les bases de données ODBC, entrez la chaîne de connexion ODBC (Open Database Connectivity) complète.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p105">The name of the database to import from, export to, or link to. Include the full path. This is a required argument. For types of databases that use separate files for each table, such as FoxPro, Paradox, and dBASE, enter the directory containing the file. Enter the file name in the <strong>Source</strong> argument (to import or link) or the <strong>Destination</strong> argument (to export). For ODBC databases, type the full Open Database Connectivity (ODBC) connection string.</span></span></p>
<p><span data-ttu-id="b064f-129">Pour visualiser un exemple de chaîne de connexion, attachez une table externe à Access :</span><span class="sxs-lookup"><span data-stu-id="b064f-129">To see an example of a connection string, link an external table to Access:</span></span></p>
<ol>
<li><p><span data-ttu-id="b064f-130">Dans la boîte de dialogue <strong>Données externes</strong>, entrez le chemin d'accès à votre base de données source dans le champ <strong>Nom de fichier</strong>.</span><span class="sxs-lookup"><span data-stu-id="b064f-130">In the <strong>Get External Data</strong> dialog box, enter the path of your source database in the <strong>File name</strong> box.</span></span></p></li>
<li><p><span data-ttu-id="b064f-131">Cliquez sur <strong>Lier à la source de données en créant une table attachée</strong>, puis cliquez sur <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="b064f-131">Click <strong>Link to the data source by creating a linked table</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b064f-132">Sélectionnez une table dans la boîte de dialogue <strong>Attacher les tables</strong>, puis cliquez sur <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="b064f-132">Select a table in the <strong>Link Tables</strong> dialog box, and click <strong>OK</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="b064f-p106">Ouvrez la table attachée en mode Création et affichez les propriétés de la table en cliquant sur <strong>Feuille de propriétés</strong> sous l'onglet <strong>Créer</strong> du groupe <strong>Outils</strong>. Le texte affiché dans le paramètre de propriété <strong>Description</strong> est la chaîne de connexion de cette table.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p106">Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>. The text in the <strong>Description</strong> property setting is the connection string for this table.</span></span></p>
<p><span data-ttu-id="b064f-135">Pour plus d’informations sur les chaînes de connexion ODBC, consultez le fichier d’aide ou la documentation du pilote ODBC de ce type de base de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="b064f-135">For more information about ODBC connection strings, see the Help file or other documentation for the ODBC driver of this type of ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b064f-136"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-136"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p107">Type de l'objet à exporter ou à importer. Si vous sélectionnez <strong>Microsoft Access</strong> comme argument <strong>Type de base de données</strong>, vous pouvez sélectionner <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d'accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d'objet</strong>. La valeur par défaut est <strong>Table</strong>. Si vous sélectionnez un autre type de base de données, ou si vous sélectionnez <strong>Lien</strong> dans la zone <strong>Type de transfert</strong>, cet argument sera ignoré. Si vous exportez une requête sélectionnée vers une base de données Access, sélectionnez <strong>Table</strong> dans cet argument pour exporter le jeu de résultats de la requête et sélectionnez <strong>Requête</strong> pour exporter la requête elle-même. Si vous exportez une requête sélectionnée vers un autre type de base de données, cet argument est ignoré et le jeu de résultats de la requête est exporté.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p107">The type of object to import or export. If you select <strong>Microsoft Access</strong> for the <strong>Database Type</strong> argument, you can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box. The default is <strong>Table</strong>. If you select any other type of database, or if you select <strong>Link</strong> in the <strong>Transfer Type</strong> box, this argument is ignored. If you are exporting a select query to an Access database, select <strong>Table</strong> in this argument to export the result set of the query, and select <strong>Query</strong> to export the query itself. If you are exporting a select query to another type of database, this argument is ignored and the result set of the query is exported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b064f-143"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-143"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p108">Nom de la table, de la requête Sélection ou de l'objet Access à importer, exporter, ou attacher. Pour certains types de bases de données, telles que FoxPro, Paradox ou dBASE, il s'agit d'un nom de fichier. Entrez l'extension du nom de fichier (par exemple, .dbf) dans le nom de fichier. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b064f-p108">The name of the table, select query, or Access object that you want to import, export, or link. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b064f-148"><strong>Destination</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-148"><strong>Destination</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p109">Nom de la table importée, exportée ou liée, de la requête sélectionnée ou d'un objet Access dans la base de données de destination. Pour certains types de bases de données, telles que FoxPro, Paradox ou dBASE, il s'agit d'un nom de fichier. Inclut l'extension du nom de fichier (par exemple .dbf) dans le nom de fichier. Il s'agit d'un argument obligatoire. Si vous sélectionnez <strong>Importer</strong> dans l'argument <strong>Type de transfert</strong> et <strong>Table</strong> dans l'argument <strong>Type d'objet</strong>, Access crée une nouvelle table contenant les données de la table importée. Si vous importez une table ou un autre objet, Access ajoute un numéro au nom en cas de conflit avec un nom existant. Par exemple, si vous importez la table Employés, mais que la table Employés existe déjà, Access renomme Employés1 la table importée ou tout autre objet importé. Si vous exportez vers une base de données Access ou une autre base de données, Access remplace automatiquement toute table ou tout objet existant qui porte le même nom.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p109">The name of the imported, exported, or linked table, select query, or Access object in the destination database. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument and <strong>Table</strong> in the <strong>Object Type</strong> argument, Access creates a new table containing the data in the imported table. If you import a table or other object, Access adds a number to the name if it conflicts with an existing name. For example, if you import Employees and Employees already exists, Access renames the imported table or other object Employees1. If you export to an Access database or another database, Access automatically replaces any existing table or other object that has the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b064f-157"><strong>Structure seulement</strong></span><span class="sxs-lookup"><span data-stu-id="b064f-157"><strong>Structure Only</strong></span></span></p></td>
<td><p><span data-ttu-id="b064f-p110">Spécifie s'il faut importer ou exporter uniquement la structure d'une table de base de données, sans ses données. Sélectionnez <strong>Oui</strong> ou <strong>Non</strong>. La valeur par défaut est <strong>Non</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b064f-p110">Specifies whether to import or export only the structure of a database table without any of its data. Select <strong>Yes</strong> or <strong>No</strong>. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b064f-161">Remarques</span><span class="sxs-lookup"><span data-stu-id="b064f-161">Remarks</span></span>

<span data-ttu-id="b064f-p111">Vous pouvez importer et exporter des tables entre Access et d'autres types de base de données. Vous pouvez également exporter des requêtes Sélection Access dans d'autres types de base de données. Access exporte le jeu de résultats de la requête dans le formulaire d'une table. Vous pouvez importer et exporter des objets de base de données Access, s'il s'agit de deux bases de données Access.</span><span class="sxs-lookup"><span data-stu-id="b064f-p111">You can import and export tables between Access and other types of databases. You can also export Access select queries to other types of databases. Access exports the result set of the query in the form of a table. You can import and export any Access database object if both databases are Access databases.</span></span>

<span data-ttu-id="b064f-p112">Si vous importez une table d'une autre base de données Access (.mdb ou .accdb) qui est attachée dans cette base, elle reste attachée même après son importation, c'est-à-dire que le lien est importé et pas la table.</span><span class="sxs-lookup"><span data-stu-id="b064f-p112">If you import a table from another Access database (.mdb or .accdb) that's a linked table in that database, it will still be linked after you import it. That is, the link is imported, not the table itself.</span></span>

<span data-ttu-id="b064f-p113">Si la base de données cible requiert un mot de passe, une boîte de dialogue s'affiche lors de l'exécution de la macro. Tapez le mot de passe dans cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b064f-p113">If the database you're accessing requires a password, a dialog box appears when you run the macro. Type the password in this dialog box.</span></span>

<span data-ttu-id="b064f-p114">L'action **ImporterExporterDonnées** est similaire aux commandes de l'onglet **Données externes**, sous **Importer** ou **Exporter**. Vous pouvez utiliser ces commandes pour sélectionner une source de données, par exemple une base de données Access ou un autre type de base de données, une feuille de calcul ou un fichier texte. Si vous sélectionnez une base de données, une ou plusieurs boîtes de dialogue s'afficheront pour vous permettre de sélectionner le type d'objet à importer ou exporter (pour les bases de données Access), le nom de l'objet et d'autres options, selon la base de données à partir de laquelle vous importez ou vers laquelle vous exportez ou attachez des éléments. Les arguments de l'action **ImporterExporterDonnées** reflètent les options dans ces boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b064f-p114">The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**. You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file. If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to. The arguments for the **ImportExportData** action reflect the options in these dialog boxes.</span></span>

<span data-ttu-id="b064f-174">Pour renseigner des informations d'index pour une table dBASE attachée, attachez d'abord la table :</span><span class="sxs-lookup"><span data-stu-id="b064f-174">If you want to supply index information for a linked dBASE table, first link the table:</span></span>

1.  <span data-ttu-id="b064f-175">Cliquez sur **Fichier dBASE**.</span><span class="sxs-lookup"><span data-stu-id="b064f-175">Click **dBASE File**.</span></span>

2.  <span data-ttu-id="b064f-176">Dans la boîte de dialogue **Données externes**, entrez le chemin d'accès au fichier dBASE dans le champ **Nom de fichier**.</span><span class="sxs-lookup"><span data-stu-id="b064f-176">In the **Get External Data** dialog box, enter the path for the dBASE file in the **File name** box.</span></span>

3.  <span data-ttu-id="b064f-177">Cliquez sur **Lier à la source de données en créant une table attachée**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b064f-177">Click **Link to the data source by creating a linked table**, then click **OK**.</span></span>

4.  <span data-ttu-id="b064f-p115">Spécifiez les index dans les boîtes de dialogue pour cette commande. Access stocke les informations d'index dans un fichier spécial d'informations (.inf), situé dans le dossier Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="b064f-p115">Specify the indexes in the dialog boxes for this command. Access stores the index information in a special information (.inf) file, located in the Microsoft Office folder.</span></span>

5.  <span data-ttu-id="b064f-180">Vous pouvez ensuite supprimer le lien vers la table attachée.</span><span class="sxs-lookup"><span data-stu-id="b064f-180">You can then delete the link to the linked table.</span></span>

<span data-ttu-id="b064f-181">La prochaine fois que vous utiliserez l'action **ImporterExporterDonnées** pour lier cette table dBASE, Access utilisera automatiquement les informations d'index que vous avez spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b064f-181">The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.</span></span>

> [!NOTE]
> <span data-ttu-id="b064f-182">[!REMARQUE] Si vous interrogez ou filtrez une table attachée, la requête ou le filtre respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="b064f-182">If you query or filter a linked table, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="b064f-183">Pour exécuter l'action **ImporterExporterDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferDatabase** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="b064f-183">To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.</span></span>

