---
title: Initialisation du pilote de Source de données texte
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9b240dbf55d2907b24b47349ee56e492f7d5e08d
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026462"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="127b6-102">Initialisation du pilote de Source de données texte</span><span class="sxs-lookup"><span data-stu-id="127b6-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="127b6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="127b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="127b6-104">Le même pilote de base de données est utilisé pour les sources de données texte et sources de données HTML.</span><span class="sxs-lookup"><span data-stu-id="127b6-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="127b6-105">Lorsque vous installez le pilote de base de données de Source de données texte, le programme d’installation écrit un ensemble de valeurs par défaut dans les sous-clés et ISAM Formats du Registre Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="127b6-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="127b6-106">Vous ne devez pas modifier ces paramètres directement. Utilisez le programme d’installation pour votre application pour ajouter, supprimer ou modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="127b6-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="127b6-107">Les sections suivantes décrivent l’initialisation et les paramètres de Format ISAM pour le pilote de base de données de Source de données de texte.</span><span class="sxs-lookup"><span data-stu-id="127b6-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="127b6-108">Paramètres d’initialisation de source de données texte</span><span class="sxs-lookup"><span data-stu-id="127b6-108">Text data source initialization settings</span></span>

<span data-ttu-id="127b6-109">Le **Access Connectivity Engine\\Formats ISAM\\dossier texte** inclut les paramètres d’initialisation du pilote Acetxt.dll, utilisé pour l’accès externe aux fichiers de données de texte.</span><span class="sxs-lookup"><span data-stu-id="127b6-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="127b6-110">L'exemple ci-dessous montre des paramètres par défaut pour les entrées de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="127b6-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

<span data-ttu-id="127b6-111">Le moteur de base de données Microsoft Access utilise les entrées de dossier Text suivantes.</span><span class="sxs-lookup"><span data-stu-id="127b6-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="127b6-112">Entrée</span><span class="sxs-lookup"><span data-stu-id="127b6-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="127b6-113">Description</span><span class="sxs-lookup"><span data-stu-id="127b6-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="127b6-114">Win32</span><span class="sxs-lookup"><span data-stu-id="127b6-114">win32</span></span></p></td>
<td><p><span data-ttu-id="127b6-p103">Emplacement de Acetxt.dll. Le Chemin d'accès complet est déterminé au moment de l'installation. Les valeurs sont de type REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="127b6-p103">The location of Acetxt.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="127b6-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="127b6-p104">Nombre de lignes devant être analysées pour déterminer les types de colonne. En présence de la valeur 0, la recherche porte sur le fichier entier. La valeur par défaut est 25. Les valeurs sont de type REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="127b6-p104">The number of rows to be scanned when guessing the column types. If set to 0, the entire file will be searched. The default is 25. Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="127b6-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="127b6-p105">Valeur binaire indiquant si la première ligne de la table contient des noms de colonnes. La valeur 01 indique que les noms de colonne sont pris dans la première ligne, pendant l'importation.</span><span class="sxs-lookup"><span data-stu-id="127b6-p105">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-126">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="127b6-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="127b6-p106">Indicateur du mode de stockage des pages. Les valeurs suivantes peuvent être utilisées :</span><span class="sxs-lookup"><span data-stu-id="127b6-p106">An indicator of how text pages are stored. Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="127b6-p107">ANSI — page de code ANSI de la machine. Conversions AnsiToUnicode et UnicodeToAnsi réalisées.</span><span class="sxs-lookup"><span data-stu-id="127b6-p107">ANSI — The ANSI code page of the machine. AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="127b6-p108">OEM — page de code OEM de la machine. Conversions OEMToUnicode et UnicodeToOEM réalisées.</span><span class="sxs-lookup"><span data-stu-id="127b6-p108">OEM — The OEM code page of the machine. OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="127b6-133">Unicode   — conversions de page de code non réalisées.</span><span class="sxs-lookup"><span data-stu-id="127b6-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="127b6-134">&lt;nombre décimal&gt; — le numéro de page de code d’un jeu de caractères spécifique.</span><span class="sxs-lookup"><span data-stu-id="127b6-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="127b6-135">Conversions de Unicode et seront effectuées.</span><span class="sxs-lookup"><span data-stu-id="127b6-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="127b6-p110">La valeur par défaut est ANSI. Les valeurs sont de type REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="127b6-p110">The default is ANSI. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-138">Format</span><span class="sxs-lookup"><span data-stu-id="127b6-138">Format</span></span></p></td>
<td><p><span data-ttu-id="127b6-139">Peut être un des suivants : TabDelimited, CSVDelimited, délimité (&lt;caractère&gt;).</span><span class="sxs-lookup"><span data-stu-id="127b6-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="127b6-140">Le délimiteur à caractère unique dans le format délimité peut être n’importe quel caractère unique à l’exception des guillemets doubles (&quot;).</span><span class="sxs-lookup"><span data-stu-id="127b6-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="127b6-141">La valeur par défaut est CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="127b6-141">The default is CSVDelimited.</span></span> <span data-ttu-id="127b6-142">Les valeurs sont de type REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="127b6-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-143">Extensions</span><span class="sxs-lookup"><span data-stu-id="127b6-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="127b6-p112">Extension de tout fichier à parcourir lorsque vous recherchez des données textuelles. Les extensions par défaut sont txt, csv, tab, asc. Les valeurs sont de type REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="127b6-p112">The extension of any files to be browsed when looking for text-based data. The default is txt, csv, tab, asc. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="127b6-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="127b6-p113">Valeur binaire qui indique si le symbole monétaire correspondant est inclus lorsque les champs monétaires sont exportées. La valeur 01 indique que le symbole est inclus. La valeur 00 indique que seules les données numériques sont exportées. La valeur par défaut est 01. Les valeurs sont de type REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="127b6-p113">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported. A value of 01 indicates that the symbol is included. A value of 00 indicates that only the numeric data is exported. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="127b6-153">Formats ISAM de source de données texte</span><span class="sxs-lookup"><span data-stu-id="127b6-153">Text data source ISAM formats</span></span>

<span data-ttu-id="127b6-154">Le **Access Connectivity Engine\\Formats ISAM\\texte** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="127b6-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="127b6-155">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="127b6-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="127b6-156">Type</span><span class="sxs-lookup"><span data-stu-id="127b6-156">Type</span></span></p></th>
<th><p><span data-ttu-id="127b6-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="127b6-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="127b6-158">Engine</span><span class="sxs-lookup"><span data-stu-id="127b6-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="127b6-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-160">Texte</span><span class="sxs-lookup"><span data-stu-id="127b6-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="127b6-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="127b6-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-163">Fichier texte (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="127b6-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="127b6-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="127b6-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-166">Fichiers texte (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="127b6-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="127b6-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="127b6-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-169">01</span><span class="sxs-lookup"><span data-stu-id="127b6-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="127b6-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="127b6-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-172">01</span><span class="sxs-lookup"><span data-stu-id="127b6-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="127b6-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="127b6-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="127b6-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="127b6-175">2</span><span class="sxs-lookup"><span data-stu-id="127b6-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="127b6-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="127b6-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-178">00</span><span class="sxs-lookup"><span data-stu-id="127b6-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="127b6-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="127b6-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-181">00</span><span class="sxs-lookup"><span data-stu-id="127b6-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="127b6-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="127b6-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-p114">Permet d'importer des données du fichier externe dans la base de données active. La modification des données dans la base de données active n'entraîne pas celle des données du fichier externe.</span><span class="sxs-lookup"><span data-stu-id="127b6-p114">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="127b6-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="127b6-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-p115">Permet de créer, dans la base de données active, une table liée au fichier externe. La modification des données dans la base de données active entraîne celle des données dans le fichier externe.</span><span class="sxs-lookup"><span data-stu-id="127b6-p115">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="127b6-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="127b6-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-p116">Permet d'exporter les données de la base de données active vers le fichier texte. Ce processus entraîne l'écrasement des données si l'exportation a lieu vers un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="127b6-p116">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="127b6-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="127b6-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-196">01</span><span class="sxs-lookup"><span data-stu-id="127b6-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="127b6-197">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="127b6-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="127b6-198">Formats ISAM d’importation HTML</span><span class="sxs-lookup"><span data-stu-id="127b6-198">HTML import ISAM formats</span></span>

<span data-ttu-id="127b6-199">Le **Access Connectivity Engine\\Formats ISAM\\importation HTML** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="127b6-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="127b6-200">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="127b6-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="127b6-201">Type</span><span class="sxs-lookup"><span data-stu-id="127b6-201">Type</span></span></p></th>
<th><p><span data-ttu-id="127b6-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="127b6-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="127b6-203">Engine</span><span class="sxs-lookup"><span data-stu-id="127b6-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="127b6-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-205">Texte</span><span class="sxs-lookup"><span data-stu-id="127b6-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="127b6-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="127b6-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-208">Fichiers HTML (*.ht*)</span><span class="sxs-lookup"><span data-stu-id="127b6-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="127b6-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="127b6-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-211">01</span><span class="sxs-lookup"><span data-stu-id="127b6-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="127b6-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="127b6-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-214">00</span><span class="sxs-lookup"><span data-stu-id="127b6-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="127b6-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="127b6-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="127b6-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="127b6-217">2</span><span class="sxs-lookup"><span data-stu-id="127b6-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="127b6-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="127b6-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-220">00</span><span class="sxs-lookup"><span data-stu-id="127b6-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="127b6-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="127b6-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-223">00</span><span class="sxs-lookup"><span data-stu-id="127b6-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="127b6-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="127b6-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-p117">Permet d'importer des données du fichier externe dans la base de données active. La modification des données dans la base de données active n'entraîne pas celle des données du fichier externe.</span><span class="sxs-lookup"><span data-stu-id="127b6-p117">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="127b6-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="127b6-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-p118">Permet de créer, dans la base de données active, une table liée au fichier externe. La modification des données dans la base de données active entraîne celle des données dans le fichier externe.</span><span class="sxs-lookup"><span data-stu-id="127b6-p118">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="127b6-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="127b6-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-234">01</span><span class="sxs-lookup"><span data-stu-id="127b6-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="127b6-235">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="127b6-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="127b6-236">Formats ISAM d’exportation HTML</span><span class="sxs-lookup"><span data-stu-id="127b6-236">HTML export ISAM formats</span></span>

<span data-ttu-id="127b6-237">Le **Access Connectivity Engine\\Formats ISAM\\exportation HTML** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="127b6-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="127b6-238">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="127b6-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="127b6-239">Type</span><span class="sxs-lookup"><span data-stu-id="127b6-239">Type</span></span></p></th>
<th><p><span data-ttu-id="127b6-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="127b6-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="127b6-241">Engine</span><span class="sxs-lookup"><span data-stu-id="127b6-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="127b6-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-243">Texte</span><span class="sxs-lookup"><span data-stu-id="127b6-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="127b6-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="127b6-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-246">Fichiers HTML (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="127b6-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="127b6-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="127b6-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-249">00</span><span class="sxs-lookup"><span data-stu-id="127b6-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="127b6-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="127b6-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-252">01</span><span class="sxs-lookup"><span data-stu-id="127b6-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="127b6-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="127b6-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="127b6-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="127b6-255">2</span><span class="sxs-lookup"><span data-stu-id="127b6-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="127b6-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="127b6-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-258">00</span><span class="sxs-lookup"><span data-stu-id="127b6-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="127b6-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="127b6-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-261">00</span><span class="sxs-lookup"><span data-stu-id="127b6-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="127b6-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="127b6-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="127b6-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="127b6-p119">Permet d'exporter les données de la base de données active vers le fichier texte. Ce processus entraîne l'écrasement des données si l'exportation a lieu vers un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="127b6-p119">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="127b6-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="127b6-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="127b6-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="127b6-268">01</span><span class="sxs-lookup"><span data-stu-id="127b6-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="127b6-269">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="127b6-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="127b6-270">Personnalisation du fichier Schema.ini pour le texte et des données HTML</span><span class="sxs-lookup"><span data-stu-id="127b6-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="127b6-p120">Pour lire, importer ou exporter des données de texte et des données HTML, vous devez créer un fichier Schema.ini en plus d'inclure les informations ISAM de texte dans le fichier .ini. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en forme du fichier de texte, lecture du fichier lors de l'importation et format d'exportation par défaut des fichiers. Les exemple suivants montrent la disposition pour un fichier de largeur fixe, Filename.txt :</span><span class="sxs-lookup"><span data-stu-id="127b6-p120">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

<span data-ttu-id="127b6-274">De même, la mise en forme d'un fichier délimité est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="127b6-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

<span data-ttu-id="127b6-275">Si vous exportez des données dans un fichier de texte délimité, définissez également la mise en forme de ce fichier :</span><span class="sxs-lookup"><span data-stu-id="127b6-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

<span data-ttu-id="127b6-p121">L'exemple My Special Export fait référence à une option d'exportation spécifique ; vous pouvez combiner d'autres options d'exportation au moment de la connexion. Ce dernier exemple correspond à un nom de source de données (DSN) pouvant être passé au moment de la connexion (facultatif). Les trois sections de format peuvent être incluses dans le même fichier .ini..</span><span class="sxs-lookup"><span data-stu-id="127b6-p121">The My Special Export example refers to a specific export option; you can specify any variation of export options at connect time. This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time. All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="127b6-279">Le moteur de base de données Microsoft Access utilise les entrées du fichier Schema.ini suivantes.</span><span class="sxs-lookup"><span data-stu-id="127b6-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="127b6-280">Entrée</span><span class="sxs-lookup"><span data-stu-id="127b6-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="127b6-281">Description</span><span class="sxs-lookup"><span data-stu-id="127b6-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="127b6-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="127b6-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="127b6-283">Peut être défini à l'aide des valeurs <strong>True</strong> (le premier enregistrement contient les noms de colonne) ou <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="127b6-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-284">Format</span><span class="sxs-lookup"><span data-stu-id="127b6-284">Format</span></span></p></td>
<td><p><span data-ttu-id="127b6-285">Peut être définie sur une des valeurs suivantes : TabDelimited, CSVDelimited, délimité (&lt;caractère&gt;), ou FixedLength.</span><span class="sxs-lookup"><span data-stu-id="127b6-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="127b6-286">Le délimiteur spécifié pour le format de fichier délimité peut être n’importe quel caractère unique à l’exception des guillemets doubles (&quot;).</span><span class="sxs-lookup"><span data-stu-id="127b6-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-287">FormatFixe</span><span class="sxs-lookup"><span data-stu-id="127b6-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="127b6-288">Utilisé uniquement lorsque le format est FixedLength, peut être défini avec l'une des valeurs suivantes : RaggedEdge ou TrueFixedLength.
</span><span class="sxs-lookup"><span data-stu-id="127b6-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="127b6-289">RaggedEdge permet aux lignes d'être terminées par une marque de fin de paragraphe (caractère de retour chariot).</span><span class="sxs-lookup"><span data-stu-id="127b6-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="127b6-290">TrueFixedLength nécessite que chaque ligne comporte un nombre exact de caractères. Tous les caractères de retour chariot qui ne se situent pas à une limite de ligne sont considérées comme intégrés dans un champ.</span><span class="sxs-lookup"><span data-stu-id="127b6-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="127b6-291">Si ce paramètre n'est pas présent, la valeur par défaut est RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="127b6-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="127b6-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="127b6-p124">Indique le nombre de lignes à analyser lors de l'estimation des types de données des colonnes. La valeur 0 indique que la recherche est effectuée dans l'ensemble du fichier.</span><span class="sxs-lookup"><span data-stu-id="127b6-p124">Indicates the number of rows to be scanned when guessing the column data types. If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-295">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="127b6-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="127b6-296">Peut être défini en OEM, ANSI, UNICODE ou le nombre décimal d'une page de code valide, et indique le jeu de caractères du fichier source.</span><span class="sxs-lookup"><span data-stu-id="127b6-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="127b6-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="127b6-p125">Peut être défini en une chaîne de format indiquant les dates et les heures. Cette entrée doit être spécifiée si tous les champs date/heure de l'importation/exportation sont traités avec le même format. Tous les formats de moteur de base de données Microsoft Jet à l'exception d'AM et PM sont pris en charge. En l'absence d'une chaîne de format, les options de représentation de date et d'heure courtes du Panneau de configuration de Windows sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="127b6-p125">Can be set to a format string indicating dates and times. This entry should be specified if all date/time fields in the import/export are handled with the same format. All of the Microsoft Jet database engine formats except AM and PM are supported. In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="127b6-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="127b6-p126">Indique le symbole à utiliser pour les valeurs monétaires dans le fichier de texte ($ ou €, par exemple). Si cette entrée n'est pas présente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-p126">Indicates the currency symbol to be used for currency values in the text file. Examples include the dollar sign ($) and Dm. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="127b6-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="127b6-307">Peut être définie à une des valeurs suivantes : symbole monétaire en préfixe, sans séparation ($1) symbole monétaire en suffixe, sans séparation (1$) symbole monétaire en préfixe avec un caractère séparation ($ 1) symbole monétaire en suffixe avec une séparation d’un caractère (1 $) si cette entrée est absent, la valeur par défaut dans le panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="127b6-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="127b6-p127">Définit le nombre de chiffres utilisés pour la partie décimale d'un montant monétaire. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-p127">Specifies the number of digits used for the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="127b6-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="127b6-312">Peut être une des valeurs suivantes : ($1) : $1 – 1 $ $1 – (1$) – 1$ $ 1 – $ 1 – – 1 $ – 1 1 $ $– $ 1 – $ 1 – 1 – $ ($ 1) (1 $) le signe dollar est indiqué à des fins de cet exemple, mais elle doit être remplacée par la valeur CurrencySymbol appropriée dans le programme.</span><span class="sxs-lookup"><span data-stu-id="127b6-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="127b6-313">Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="127b6-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="127b6-p129">Désigne le symbole mono-caractère à utiliser pour séparer les milliers dans les valeurs monétaires du fichier de texte. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-p129">Indicates the single-character symbol to be used for separating currency values by thousands in the text file. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="127b6-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="127b6-p130">Peut être tout caractère utilisé pour séparer la partie entière et la partie décimale d'un montant monétaire. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-p130">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="127b6-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="127b6-p131">Peut être tout caractère utilisé pour séparer la partie entière et la partie décimale d'un nombre. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-p131">Can be set to any single character that is used to separate the integer from the fractional part of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="127b6-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="127b6-p132">Indique le nombre de chiffres utilisées dans la partie décimale d'un nombre. Si cette entrée est absente, la valeur par défaut du Panneau de configuration de Windows est utilisée.</span><span class="sxs-lookup"><span data-stu-id="127b6-p132">Indicates the number of decimal digits in the fractional portion of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="127b6-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="127b6-327">Indique si une valeur décimale inférieure à 1 et supérieure à –1 doit commencer par des zéros. Cette valeur peut être False (pas de zéros) ou True.</span><span class="sxs-lookup"><span data-stu-id="127b6-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="127b6-328">Col1, Col2, …</span><span class="sxs-lookup"><span data-stu-id="127b6-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="127b6-329">Répertorie les colonnes dans le fichier texte à lire.</span><span class="sxs-lookup"><span data-stu-id="127b6-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="127b6-330">Le format de cette entrée doit être : <em>Coln</em>=<em>NomColonne</em> type [Width <em> #</em>] <em>NomColonne</em>: les noms de colonne contenant des espaces doivent être placés entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="127b6-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="127b6-331"><em>type</em>: peut être Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="127b6-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="127b6-332">Binaire, OLE, texte ou Mémo.</span><span class="sxs-lookup"><span data-stu-id="127b6-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="127b6-333">En outre, les types de pilote texte ODBC suivants sont pris en charge : Char (comme texte) Float (comme Double) Integer (comme court) LongChar (comme Mémo) Date <em>format de date</em> dans le cas d’un type Mémo un marqueur de format supplémentaire [Attribute Hyperlink] peut être permet de spécifier les colonnes qui doivent être des URL actifs dans Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="127b6-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="127b6-334">Dans le cas d'un type Décimal, les marqueurs de format supplémentaires [Scale #] Precision #] doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="127b6-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="127b6-335">DélimiteurTexte</span><span class="sxs-lookup"><span data-stu-id="127b6-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="127b6-336">Peut être tout caractère utilisé pour délimiter les chaînes qui contiennent un des autres caractères spéciaux.
</span><span class="sxs-lookup"><span data-stu-id="127b6-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="127b6-337">Ex. :</span><span class="sxs-lookup"><span data-stu-id="127b6-337">E.g.</span></span> <span data-ttu-id="127b6-338">&quot;ABC&quot;,&quot;xyz, pqr&quot;,&quot;hij&quot; si cette entrée n’est pas présente le séparateur par défaut est un guillemet double.</span><span class="sxs-lookup"><span data-stu-id="127b6-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="127b6-339">Si cette entrée est la chaîne &quot;aucun&quot; puis aucun des caractères ne sont considérés comme des séparateurs.</span><span class="sxs-lookup"><span data-stu-id="127b6-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="127b6-340">[!REMARQUE] Lorsque vous modifiez des paramètres Schema.ini, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="127b6-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


