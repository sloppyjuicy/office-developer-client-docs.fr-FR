---
title: ImporterExporterFeuilleDeCalcul, action de macro
TOCTitle: ImportExportSpreadsheet Macro Action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 78819ba2a82bf2fc9ab5c39300d06c1acdda80bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875804"
---
# <a name="importexportspreadsheet-macro-action"></a><span data-ttu-id="34353-102">ImporterExporterFeuilleDeCalcul, action de macro</span><span class="sxs-lookup"><span data-stu-id="34353-102">ImportExportSpreadsheet Macro Action</span></span>


<span data-ttu-id="34353-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34353-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34353-p101">L'action **ImporterExporterFeuilleDeCalcul** permet d'importer ou d'exporter des données entre la base de données Access (.mdb ou .accdb) ou le projet Access (.adp) actif et un fichier de feuille de calcul. Vous pouvez également lier les données figurant dans une feuille de calcul Microsoft Excel dans la base de données Access active. Avec une feuille de calcul attachée, vous pouvez afficher et modifier les données de la feuille dans Access, tout en garantissant l'accès aux données à partir de la feuille de calcul Excel. Vous pouvez aussi attacher les données d'un fichier de feuille de calcul Lotus 1-2-3, mais elles seront en lecture seule dans Access.</span><span class="sxs-lookup"><span data-stu-id="34353-p101">You can use the **ImportExportSpreadsheet** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and a spreadsheet file. You can also link the data in a Microsoft Excel spreadsheet to the current Microsoft Access database. With a linked spreadsheet, you can view and edit the spreadsheet data with Access while still allowing complete access to the data from your Excel spreadsheet program. You can also link to data in a Lotus 1-2-3 spreadsheet file, but this data is read-only in Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="34353-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="34353-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="34353-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="34353-110">Setting</span></span>

<span data-ttu-id="34353-111">L'action **TransférerFeuilleCalcul** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="34353-111">The **TransferSpreadsheet** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34353-112">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="34353-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="34353-113">Description</span><span class="sxs-lookup"><span data-stu-id="34353-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34353-114"><strong>Type de transfert</strong></span><span class="sxs-lookup"><span data-stu-id="34353-114"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="34353-p103">Type de transfert à effectuer. Sélectionnez <strong>Importation</strong>, <strong>Exportation</strong>, ou <strong>Attache</strong> dans la zone <strong>Type de transfert</strong> de la section <strong>Arguments de l'action</strong> du Générateur de macro. La valeur par défaut est <strong>Importation</strong>.  </span><span class="sxs-lookup"><span data-stu-id="34353-p103">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="34353-118">Le type de transfert <STRONG>Attache</STRONG> n’est pas pris en charge dans les projets Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="34353-118">The <STRONG>Link</STRONG> transfer type is not supported for Access projects (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34353-119"><strong>Type de feuille de calcul</strong></span><span class="sxs-lookup"><span data-stu-id="34353-119"><strong>Spreadsheet Type</strong></span></span></p></td>
<td><p><span data-ttu-id="34353-p104">Type de feuille de calcul à partir de laquelle effectuer l'importation, vers laquelle effectuer l'exportation ou à laquelle attacher les données. Vous pouvez sélectionner un des types de feuilles de calcul dans la zone concernée. La valeur par défaut est <strong>Classeur Excel</strong>.  </span><span class="sxs-lookup"><span data-stu-id="34353-p104">The type of spreadsheet to import from, export to, or link to. You can select one of a number of spreadsheet types in the box. The default is <strong>Excel Workbook</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="34353-p105">Vous pouvez importer et attacher des données (en lecture seule) vers des fichiers Lotus .WK4, mais vous ne pouvez pas exporter de données Access dans ce format de feuille de calcul. Via cette action, Access ne prend plus en charge l’importation, l’exportation ou la liaison des données à partir de feuilles de données Lotus .WKS ou Excel version 2.0. Pour attacher ou importer des données dans des données de feuilles de calcul au format Excel version 2.0 ou Lotus .WKS, vous devez convertir les données des feuilles de calcul dans une version ultérieure d’Excel ou de Lotus 1-2-3 avant d’importer ou d’attacher les données dans Access.</span><span class="sxs-lookup"><span data-stu-id="34353-p105">You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format. Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action. If you want to import from or link to spreadsheet data in Excel version 2.0 or Lotus .WKS format, convert the spreadsheet data to a later version of Excel or Lotus 1-2-3 before importing or linking the data into Access.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34353-126"><strong>Nom de la table</strong></span><span class="sxs-lookup"><span data-stu-id="34353-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="34353-p106">Nom de la table Access dans laquelle importer des données de feuille de calcul, vers laquelle exporter des données de feuille de calcul ou avec laquelle attacher des données de feuille de calcul. Vous pouvez également taper le nom de la requête Sélection Access à partir de laquelle vous souhaitez exporter les données. Il s'agit d'un argument obligatoire. Si vous sélectionnez <strong>Import</strong> dans l'argument <strong>Type de transfert</strong>, Access ajoute les données de feuille de calcul à cette table si la table existe déjà. Dans le cas contraire, Access crée une table contenant les données de feuille de calcul. Dans Access, vous ne pouvez pas utiliser une instruction SQL pour spécifier les données à exporter si vous utilisez l'action <strong>ImportExportSpreadsheet</strong>. Au lieu d'utiliser une instruction SQL, vous devez d'abord créer une requête, puis spécifier le nom de la requête dans l'argument <strong>Nom de la table</strong>.  </span><span class="sxs-lookup"><span data-stu-id="34353-p106">The name of the Access table to import spreadsheet data to, export spreadsheet data from, or link spreadsheet data to. You can also type the name of the Access select query you want to export data from. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument, Access appends the spreadsheet data to this table if the table already exists. Otherwise, Access creates a new table containing the spreadsheet data. In Access, you can't use an SQL statement to specify data to export when you are using the <strong>ImportExportSpreadsheet</strong> action. Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34353-134"><strong>Nom du fichier</strong></span><span class="sxs-lookup"><span data-stu-id="34353-134"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="34353-p107">Nom du fichier de feuille de calcul à partir duquel importer, vers lequel exporter ou auquel attacher des données. Inclut le chemin d'accès complet. Il s'agit d'un argument obligatoire. Access crée une feuille de calcul lorsque vous exportez des données provenant d'Access. Si le nom de fichier est identique au nom d'une feuille de calcul existante, Access remplace la feuille de calcul existante, sauf si vous exportez des données vers un classeur Excel version 5.0 ou ultérieure. Dans ce cas, Access copie les données exportées dans la feuille de calcul suivante disponible dans le classeur. Si vous importez ou attachez des données à partir d'une feuille de calcul Excel version 5.0 ou ultérieure, vous pouvez spécifier une feuille de calcul particulière en utilisant l'argument <strong>Range</strong>.  </span><span class="sxs-lookup"><span data-stu-id="34353-p107">The name of the spreadsheet file to import from, export to, or link to. Include the full path. This is a required argument. Access creates a new spreadsheet when you export data from Access. If the file name is the same as the name of an existing spreadsheet, Access replaces the existing spreadsheet, unless you're exporting to an Excel version 5.0 or later workbook. In that case, Access copies the exported data to the next available new worksheet in the workbook. If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can specify a particular worksheet by using the <strong>Range</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34353-142"><strong>Contient les noms de champs</strong></span><span class="sxs-lookup"><span data-stu-id="34353-142"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="34353-p108">Spécifie si la première ligne de la feuille de calcul contient les noms de champs. Si vous sélectionnez <strong>Oui</strong>, Access utilise les noms de cette ligne en tant que noms de champs dans la table Access lors de l'importation ou de la liaison des données de la feuille de calcul. Si vous sélectionnez <strong>Non</strong>, Access considère la première ligne comme une ligne de données normale. La valeur par défaut est <strong>Non</strong>. Lorsque vous exportez une table Access ou une requête Sélection vers une feuille de calcul, les noms des champs sont insérés à la première ligne de la feuille de calcul, que vous ayez sélectionné ou non cet argument.  </span><span class="sxs-lookup"><span data-stu-id="34353-p108">Specifies whether the first row of the spreadsheet contains the names of the fields. If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the spreadsheet data. If you select <strong>No</strong>, Access treats the first row as a normal row of data. The default is <strong>No</strong>. When you export an Access table or select query to a spreadsheet, the field names are inserted into the first row of the spreadsheet no matter what you select in this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34353-148"><strong>Plage</strong></span><span class="sxs-lookup"><span data-stu-id="34353-148"><strong>Range</strong></span></span></p></td>
<td><p><span data-ttu-id="34353-p109">Plage de cellules à importer ou attacher. Laissez cet argument vierge pour importer ou attacher la feuille de calcul entière. Vous pouvez taper le nom d'une plage dans la feuille de calcul, ou spécifier la plage de cellules à importer ou attacher, par exemple, A1:E25 (notez que la syntaxe A1..E25 ne fonctionne pas dans Access 97 ou une version ultérieure). Si l'importation ou la liaison s'effectue vers une feuille de calcul Excel version 5.0 ou ultérieure, vous pouvez faire précéder la plage du nom de la feuille de calcul, suivi d'un point d'exclamation, par exemple : Budget!A1:C7.</span><span class="sxs-lookup"><span data-stu-id="34353-p109">The range of cells to import or link. Leave this argument blank to import or link the entire spreadsheet. You can type the name of a range in the spreadsheet or specify the range of cells to import or link, such as A1:E25 (note that the A1..E25 syntax does not work in Access 97 or later). If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can prefix the range with the name of the worksheet and an exclamation point; for example, Budget!A1:C7.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="34353-p110">Lorsque vous effectuez une exportation vers une feuille de calcul, vous devez laisser cet argument vierge. Si vous entrez une plage, l’exportation échoue.</span><span class="sxs-lookup"><span data-stu-id="34353-p110">When you export to a spreadsheet, you must leave this argument blank. If you enter a range, the export will fail.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="34353-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="34353-155">Remarks</span></span>

<span data-ttu-id="34353-p111">Vous pouvez exporter les données figurant dans des requêtes Sélection Access dans des feuilles de calcul. Access exporte le jeu de résultats de la requête comme s'il s'agissait d'une table.</span><span class="sxs-lookup"><span data-stu-id="34353-p111">You can export the data in Access select queries to spreadsheets. Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="34353-158">Les données de la feuille de calcul que vous ajoutez à une table Access existante doivent être compatibles avec la structure de la table.</span><span class="sxs-lookup"><span data-stu-id="34353-158">Spreadsheet data that you append to an existing Access table must be compatible with the table's structure.</span></span>

  - <span data-ttu-id="34353-159">Le type de données de chaque champ de la feuille de calcul doit être identique à celui du champ correspondant dans la table.</span><span class="sxs-lookup"><span data-stu-id="34353-159">Each field in the spreadsheet must be of the same data type as the corresponding field in the table.</span></span>

  - <span data-ttu-id="34353-160">Les champs doivent être positionnés dans le même ordre, sauf si l'argument **Contient les noms de champs** est défini sur **Oui**, auquel cas les noms de champs de la feuille de calcul doivent correspondre aux noms de champs de la table.</span><span class="sxs-lookup"><span data-stu-id="34353-160">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the spreadsheet must match the field names in the table).</span></span>

<span data-ttu-id="34353-p112">Exécuter cette action équivaut à cliquer sur l'onglet **Données externes**, puis sur **Excel** dans le groupe **Importation** ou **Exportation**, ou à cliquer sur **Plus** dans le groupe **Importation** ou **Exportation**, puis sur **Fichier Lotus 1-2-3**. Vous pouvez utiliser ces commandes pour sélectionner une source de données telle qu'Access ou un type de base de données, de feuille de calcul ou de fichier texte. Si vous sélectionnez une feuille de calcul, une série de boîtes de dialogue s'affichent ou un Assistant Access s'exécute pour vous permettre de sélectionner le nom de la feuille de calcul et d'autres options. Les arguments de l'action **ImporterExporterFeuilleDeCalcul** reflètent les options de ces boîtes de dialogue ou de cet Assistant.</span><span class="sxs-lookup"><span data-stu-id="34353-p112">This action is similar to clicking the **External Data** tab and clicking **Excel** in the **Import** or **Export** group, or clicking **More** in the **Import** or **Export** group and clicking **Lotus 1-2-3 File**. You can use these commands to select a source of data, such as Access or a type of database, spreadsheet, or text file. If you select a spreadsheet, a series of dialog boxes appear, or an Access wizard runs, in which you select the name of the spreadsheet and other options. The arguments of the **ImportExportSpreadsheet** action reflect the options in these dialog boxes or in the wizards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="34353-165">[!REMARQUE] Si vous interrogez ou filtrez une feuille de calcul liée, la requête ou le filtre respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="34353-165">If you query or filter a linked spreadsheet, the query or filter is case-sensitive.</span></span></P>



<span data-ttu-id="34353-166">Si la liaison s'effectue vers une feuille de calcul Excel ouverte en mode d'édition, Access n'effectuera la liaison que lorsque la feuille de calcul quittera ce mode (aucun délai).</span><span class="sxs-lookup"><span data-stu-id="34353-166">If you link to an Excel spreadsheet that is open in Edit mode, Access will wait until the Excel spreadsheet is out of Edit mode before completing the link; there's no time-out.</span></span>

<span data-ttu-id="34353-167">Pour exécuter l'action **ImporterExporterFeuilleDeCalcul** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferSpreadsheet** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="34353-167">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>

