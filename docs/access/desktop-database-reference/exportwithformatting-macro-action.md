---
title: ExporterAvecMiseEnForme, action de macro
TOCTitle: ExportWithFormatting Macro Action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89c29d18e21a28448e03fee763b4087bf623d5a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469166"
---
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="d9c4a-102">ExporterAvecMiseEnForme, action de macro</span><span class="sxs-lookup"><span data-stu-id="d9c4a-102">ExportWithFormatting Macro Action</span></span>


<span data-ttu-id="d9c4a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9c4a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9c4a-104">Faites appel à l'action **ExporterAvecMiseEnForme** pour sortir les données dans l'objet de base de données Microsoft Access spécifié (une feuille de données, un formulaire, un état, un module, une page d'accès aux données) dans des formats de sortie différents.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="d9c4a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9c4a-105">Settings</span></span>

<span data-ttu-id="d9c4a-106">L'action **ExporterAvecMiseEnForme** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9c4a-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9c4a-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d9c4a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d9c4a-108">Description</span><span class="sxs-lookup"><span data-stu-id="d9c4a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9c4a-109"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-p101">Type d'objet contenant les données à copier. Cliquez sur <strong>Table</strong> (pour une feuille de données de table), <strong>Requête</strong> (pour une feuille de données de requête), <strong>Formulaire</strong> (pour un formulaire ou une feuille de données de formulaire), <strong>État</strong>, <strong>Module</strong>, <strong>Vue serveur</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d'objet</strong> de la section <strong>Arguments de l'action</strong> du volet du Générateur de macro. Vous ne pouvez pas copier une macro. Pour copier l'objet actif, sélectionnez son type à l'aide de cet argument et laissez l'argument <strong>Nom de l'objet</strong> vide. Cet argument est obligatoire. La valeur par défaut est <strong>Table</strong>.  </span><span class="sxs-lookup"><span data-stu-id="d9c4a-p101">The type of object containing the data to output. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't output a macro. If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank. This is a required argument. The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9c4a-116"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-p102">Nom de l'objet contenant les données à créer. La zone <strong>Nom de l'objet</strong> regroupe tous les objets de la base de données ayant le type sélectionné par l'argument <strong>Type d'objet</strong>. Si vous exécutez une macro contenant l'action <strong>ExportWithFormatting</strong> dans une base de données bibliothèque, Access recherche d'abord l'objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.  </span><span class="sxs-lookup"><span data-stu-id="d9c4a-p102">The name of the object containing the data to output. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9c4a-120"><strong>Format de sortie</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-121">Type de format à utiliser pour la copie des données.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-121">The type of format you want to use to output the data.</span></span> <span data-ttu-id="d9c4a-122">Vous pouvez sélectionner le <strong>classeur Excel 97 - Excel 2003 (*.xls)</strong>, <strong>Classeur Excel binaire (*.xlsb)</strong>, <strong>Le classeur Excel (*.xlsx)</strong>, <strong>HTML (*.htm ; \* .html)</strong>, <strong>Classeur Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Format PDF (*.pdf)</strong>, <strong> Rich Text Format.RTF</strong>, des <strong>fichiers texte (*.txt)</strong>ou <strong>Format XPS (*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-122">You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>.</span></span> <span data-ttu-id="d9c4a-123">Si vous laissez cet argument vide, Access vous demande de spécifier le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-123">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9c4a-124"><strong>Fichier de copie</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-p104">Fichier vers lequel vous voulez copier les données, y compris le chemin d'accès complet. Vous pouvez, si vous le souhaitez, inclure l'extension de nom de fichier standard du format de sortie choisi via l'argument <strong>Format de sortie</strong>. Si vous laissez l'argument <strong>Fichier de sortie</strong> vide, Access vous demande un nom de fichier de copie.  </span><span class="sxs-lookup"><span data-stu-id="d9c4a-p104">The file to which you want to output the data, including the full path. You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required. If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9c4a-128"><strong>Lancement automatique</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-129">Spécifie si le logiciel approprié doit se lancer immédiatement après l'exécution de l'action <strong>ExporterAvecMiseEnForme</strong>, avec le fichier spécifié par l'argument <strong>Fichier de copie</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9c4a-130"><strong>Fichier de modèle</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-p105">Chemin d'accès et nom de fichier du fichier à utiliser comme modèle pour les fichiers HTML. Le fichier de modèle est un fichier texte qui comporte des balises HTML et des jetons propres à Access.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-p105">The path and file name of a file you want to use as a template for HTML files. The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9c4a-133"><strong>Encodage</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-p106">Type de format de chiffrement des caractères voulu pour le texte ou les données HTML à copier. Vous avez le choix entre <strong>MS-DOS</strong>, <strong>Unicode</strong> et <strong>Unicode (UTF-8)</strong>. Le paramètre de l'argument <strong>MS-DOS</strong> n'est disponible que pour les fichiers texte. Si vous laissez cet argument vide, Access copie les données avec l'encodage Windows par défaut pour les fichiers texte et avec l'encodage système par défaut pour les fichiers HTML.  </span><span class="sxs-lookup"><span data-stu-id="d9c4a-p106">The type of character encoding format you want used to output the text or HTML data. You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>. The <strong>MS-DOS</strong> argument setting is available only for text files. If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9c4a-138"><strong>Qualité de copie</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4a-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4a-139">Sélectionnez <strong>Imprimer</strong> pour optimiser la copie pour l'impression ou <strong>Écran</strong> pour optimiser la copie pour l'affichage sur un écran.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d9c4a-140">Notes</span><span class="sxs-lookup"><span data-stu-id="d9c4a-140">Remarks</span></span>

<span data-ttu-id="d9c4a-p107">Les données Access sont copiées dans le format sélectionné et peuvent être lues par tout programme qui utilise ce format. Par exemple, vous pouvez copier un état Access avec sa mise en forme vers un document RTF et ouvrir ensuite ce document dans Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-p107">The Access data is output in the selected format and can be read by any program that uses the same format. For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="d9c4a-p108">Si vous copiez l'objet de base de données au format HTML, Access crée un fichier HTML contenant les données de l'objet. Vous pouvez utiliser l'argument **Fichier de modèle** pour spécifier un fichier à utiliser comme modèle pour le fichier .html.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-p108">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object. You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="d9c4a-145">Les règles suivantes s'appliquent lorsque vous utilisez l'action **ExporterAvecMiseEnForme** pour copier un objet de base de données dans l'un des formats de copie :</span><span class="sxs-lookup"><span data-stu-id="d9c4a-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="d9c4a-p109">Vous pouvez copier des données dans une table, une requête et des feuilles de données de formulaire. Dans le fichier de copie, tous les champs de la feuille de données apparaissent comme dans Access, à l'exception des champs contenant des objets OLE. Les colonnes des champs des objets OLE sont incluses dans le fichier de copie, mais sont vides.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-p109">You can output data in table, query, and form datasheets. In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects. The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="d9c4a-149">Pour un contrôle qui est lié à un champ Oui/non (bouton bascule, case d’option ou case à cocher), le fichier de sortie affiche la valeur – 1 (Oui) ou 0 (non).</span><span class="sxs-lookup"><span data-stu-id="d9c4a-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="d9c4a-150">Dans le cas d'une zone de texte liée à un champ de lien hypertexte, le fichier de copie affiche le lien hypertexte pour tous les formats de sortie excepté le format texte MS-DOS (dans ce cas, le lien hypertexte s'affiche en tant que texte normal).</span><span class="sxs-lookup"><span data-stu-id="d9c4a-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="d9c4a-151">Si vous copiez les données dans un formulaire en mode Formulaire, le fichier de copie contient la vue de feuille de données de ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="d9c4a-p110">Lorsque vous copiez une feuille de données, un formulaire ou une page d'accès aux données au format HTML, un fichier .html est créé et lorsque vous copiez un état au format HTML, un fichier .html est créé pour chaque page de l'état.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-p110">When you output a datasheet, form, or data access page in HTML format, one .html file is created. When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="d9c4a-154">Le résultat de l'exécution de l'action **ExporterAvecMiseEnForme** équivaut à cliquer sur une des options du groupe **Export** de l'onglet **Données externes**. Les arguments de l'action correspondent aux paramètres de la boîte de dialogue **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="d9c4a-155">Pour exécuter l'action **ExporterAvecMiseEnForme** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OutputTo** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-155">To run the **ExportWithFormatting** action in a Visual Basic for Applications (VBA) module, use the **OutputTo** method of the **DoCmd** object.</span></span>

