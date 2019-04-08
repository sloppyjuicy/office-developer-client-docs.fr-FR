---
title: Initialisation du pilote Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: e59070b67358b3700ca677149a849768c144c1a3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "31518130"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="b1f30-102">Initialisation du pilote Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="b1f30-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="b1f30-103">**S'applique à**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office pour l'accès professionnel 2013 | Excel 2010 | Access 2010</span><span class="sxs-lookup"><span data-stu-id="b1f30-103">**Applies to**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for business Access 2013 | Excel 2010 | Access 2010</span></span>

<span data-ttu-id="b1f30-104">Lorsque vous installez le pilote Excel, le programme d'installation écrit un ensemble de valeurs par défaut dans le Registre Windows dans les sous-clés Engines et ISAM formats.</span><span class="sxs-lookup"><span data-stu-id="b1f30-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="b1f30-105">Vous ne devez pas modifier ces paramètres directement; Utilisez le programme d'installation de votre application pour ajouter, supprimer ou modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="b1f30-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="b1f30-106">Les sections suivantes décrivent les paramètres d'initialisation et de format ISAM pour le pilote de base de données Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b1f30-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="b1f30-107">Paramètres d'initialisation Excel</span><span class="sxs-lookup"><span data-stu-id="b1f30-107">Excel initialization settings</span></span>

<span data-ttu-id="b1f30-108">Le dossier **Excel des\\moteurs\\de connectivité Access** inclut des paramètres d'initialisation pour le pilote Aceexcl. dll, utilisés pour l'accès externe aux feuilles de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b1f30-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="b1f30-109">L'exemple ci-après montre des paramètres par défaut pour les entrées de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="b1f30-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="b1f30-110">Le moteur de base de données Microsoft Access utilise les entrées de dossier Excel suivantes.</span><span class="sxs-lookup"><span data-stu-id="b1f30-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1f30-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b1f30-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="b1f30-112">Description</span><span class="sxs-lookup"><span data-stu-id="b1f30-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-113">Win32</span><span class="sxs-lookup"><span data-stu-id="b1f30-113">win32</span></span></p></td>
<td><p><span data-ttu-id="b1f30-p103">Emplacement de msexcl40.dll. Le Chemin d'accès complet est déterminé au moment de l'installation. Les valeurs sont de type REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="b1f30-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f30-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="b1f30-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="b1f30-118">Nombre de lignes à vérifier pour le type de données.</span><span class="sxs-lookup"><span data-stu-id="b1f30-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="b1f30-119">Celui-ci est déterminé en fonction du nombre maximal de types de données trouvés.</span><span class="sxs-lookup"><span data-stu-id="b1f30-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="b1f30-120">En cas d'égalité, le type de données est déterminé dans l'ordre suivant : Numérique, Monétaire, Date, Texte, Booléen.</span><span class="sxs-lookup"><span data-stu-id="b1f30-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="b1f30-121">Si les données rencontrées ne correspondent pas au type de données déterminé pour la colonne, une valeur  <strong>Null </strong> est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="b1f30-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="b1f30-122">Lors de l'importation, si une colonne a mélangé des type de données, la colonne entière sera mise en forme en fonction du paramètre ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="b1f30-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="b1f30-123">Le nombre de lignes par défaut à vérifier est de 8.</span><span class="sxs-lookup"><span data-stu-id="b1f30-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="b1f30-124">Les valeurs sont de type REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="b1f30-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="b1f30-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="b1f30-p105">Peut être défini avec la valeur MajorityType ou Text. Avec MajorityType, les colonnes de types de données mélangés sont mises en forme en fonction du type de données prédominant à l'importation. Avec Text, elles seront mises en forme selon le type de données texte à l'importation. La valeur par défaut est Text. Les values sont de type REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="b1f30-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f30-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="b1f30-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="b1f30-p106">Nombre de lignes vides devant être ajouté à la fin d'une feuille de calcul version 3.5 ou 4.0, avant l'ajout de nouvelles données. Par exemple, si AppendBlankRows possède la valeur 4, Microsoft Jet ajoutera 4 lignes vides à la fin de la feuille de calcul avant d'ajouter les lignes qui contiennent des données. Les valeurs entières pour ce paramètre peuvent être comprises entre 0 entre 16 ; la valeur par défaut est 01 (une ligne supplémentaire). Les valeurs sont de type REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="b1f30-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="b1f30-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="b1f30-p107">Valeur binaire qui indique si la première ligne du tableau contient des noms de colonne. La valeur 01 indique que les noms de colonne sont pris de la première ligne, pendant l'importation. La valeur 00 indique l'absence de nom de colonne dans la première ligne ; les noms de colonne sont alors F1, F2, F3 etc. La valeur par défaut est 01. Les valeurs sont de type REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="b1f30-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="b1f30-142">Le dossier **\\Excel 8,0\\engines de moteur de connectivité** contient les entrées suivantes, qui s'appliquent à Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="b1f30-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1f30-143">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="b1f30-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="b1f30-144">Type</span><span class="sxs-lookup"><span data-stu-id="b1f30-144">Type</span></span></p></th>
<th><p><span data-ttu-id="b1f30-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1f30-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-146">Moteur</span><span class="sxs-lookup"><span data-stu-id="b1f30-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="b1f30-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1f30-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b1f30-148">Excel</span><span class="sxs-lookup"><span data-stu-id="b1f30-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f30-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="b1f30-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="b1f30-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1f30-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b1f30-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="b1f30-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="b1f30-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="b1f30-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1f30-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b1f30-154">0102</span><span class="sxs-lookup"><span data-stu-id="b1f30-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f30-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="b1f30-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="b1f30-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1f30-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b1f30-157">2,00</span><span class="sxs-lookup"><span data-stu-id="b1f30-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="b1f30-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="b1f30-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1f30-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="b1f30-160">0,1</span><span class="sxs-lookup"><span data-stu-id="b1f30-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f30-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="b1f30-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="b1f30-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1f30-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b1f30-163">2,00</span><span class="sxs-lookup"><span data-stu-id="b1f30-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="b1f30-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="b1f30-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1f30-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b1f30-166">0102</span><span class="sxs-lookup"><span data-stu-id="b1f30-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1f30-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="b1f30-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="b1f30-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1f30-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b1f30-p108">Permet d'exporter les données de la base de données active vers le fichier Microsoft Excel 97. Ce processus entraîne l'écrasement des données si l'exportation a lieu vers un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="b1f30-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1f30-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="b1f30-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="b1f30-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b1f30-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b1f30-173">0102</span><span class="sxs-lookup"><span data-stu-id="b1f30-173">01</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="b1f30-174">Utilisation du paramètre TypeGuessRows pour le pilote Excel</span><span class="sxs-lookup"><span data-stu-id="b1f30-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="b1f30-175">Lorsque vous utilisez le pilote Microsoft Excel, vous pouvez utiliser la valeur de Registre **TypeGuessRows** pour configurer le nombre de lignes à vérifier pour le type de données.</span><span class="sxs-lookup"><span data-stu-id="b1f30-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="b1f30-176">La valeur **TypeGuessRows** se trouve sous la sous-clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="b1f30-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# [<a name="office-2016"></a><span data-ttu-id="b1f30-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="b1f30-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="b1f30-178">Pour une installation MSI d'Office</span><span class="sxs-lookup"><span data-stu-id="b1f30-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="b1f30-179">Pour Office 32 bits sur 32 bits Windows ou 64 bits sur Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b1f30-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  **<span data-ttu-id="b1f30-180">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-180">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel</span></span>**

- <span data-ttu-id="b1f30-181">Pour Office 32 bits sur les Windows 64 bits:</span><span class="sxs-lookup"><span data-stu-id="b1f30-181">For 32-bit Office on 64-bit Windows:</span></span>

  **<span data-ttu-id="b1f30-182">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-182">HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel</span></span>**
    
<span data-ttu-id="b1f30-183">Pour une installation «démarrer en un clic» d'Office</span><span class="sxs-lookup"><span data-stu-id="b1f30-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="b1f30-184">Pour Office 32 bits sur 32 bits Windows ou 64 bits sur Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b1f30-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  **<span data-ttu-id="b1f30-185">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-185">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel</span></span>**

- <span data-ttu-id="b1f30-186">Pour Office 32 bits sur les Windows 64 bits:</span><span class="sxs-lookup"><span data-stu-id="b1f30-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  **<span data-ttu-id="b1f30-187">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-187">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel</span></span>**

<span data-ttu-id="b1f30-188">Le nombre par défaut de lignes à vérifier est **8** (huit).</span><span class="sxs-lookup"><span data-stu-id="b1f30-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="b1f30-189">Lorsque vous définissez la valeur **TypeGuessRows** sur **0** (zéro), le pilote Excel vérifie les premières lignes de 16 384 pour le type de données.</span><span class="sxs-lookup"><span data-stu-id="b1f30-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="b1f30-190">Si vous souhaitez vérifier plus de 16 384 lignes, définissez **TypeGuessRows** sur une valeur qui est basée sur la plage de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b1f30-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="b1f30-191">Pour vérifier toutes les lignes, définissez **TypeGuessRows** sur 1 048 576 (nombre maximal de lignes autorisées dans Excel).</span><span class="sxs-lookup"><span data-stu-id="b1f30-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="b1f30-192">Le type de données est déterminé par le nombre maximal de types de données qui sont trouvés.</span><span class="sxs-lookup"><span data-stu-id="b1f30-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="b1f30-193">En cas de lien, le type de données est déterminé dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="b1f30-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="b1f30-194">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1f30-194">Number</span></span>
- <span data-ttu-id="b1f30-195">Devise</span><span class="sxs-lookup"><span data-stu-id="b1f30-195">Currency</span></span>
- <span data-ttu-id="b1f30-196">Date</span><span class="sxs-lookup"><span data-stu-id="b1f30-196">Date</span></span>
- <span data-ttu-id="b1f30-197">Text</span><span class="sxs-lookup"><span data-stu-id="b1f30-197">Text</span></span>
- <span data-ttu-id="b1f30-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="b1f30-198">Boolean</span></span>

<span data-ttu-id="b1f30-199">Si des données ne correspondent pas au type de données devinées pour la colonne, ces données sont renvoyées sous la forme d'une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="b1f30-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="b1f30-200">Lors d'une importation, si une colonne possède des types de données mixtes, la colonne entière est convertie en un type de données défini par le paramètre **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="b1f30-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# [<a name="office-2013"></a><span data-ttu-id="b1f30-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1f30-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="b1f30-202">Pour Office 32 bits sur 32 bits Windows ou 64 bits sur Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b1f30-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

**<span data-ttu-id="b1f30-203">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-203">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel</span></span>**

<span data-ttu-id="b1f30-204">Pour Office 32 bits sur les Windows 64 bits:</span><span class="sxs-lookup"><span data-stu-id="b1f30-204">For 32-bit Office on 64-bit Windows:</span></span>

**<span data-ttu-id="b1f30-205">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-205">HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel</span></span>**

<span data-ttu-id="b1f30-206">Le nombre par défaut de lignes à vérifier est **8** (huit).</span><span class="sxs-lookup"><span data-stu-id="b1f30-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="b1f30-207">Lorsque vous définissez la valeur **TypeGuessRows** sur **0** (zéro), le pilote Excel vérifie les premières lignes de 16 384 pour le type de données.</span><span class="sxs-lookup"><span data-stu-id="b1f30-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="b1f30-208">Si vous souhaitez vérifier plus de 16 384 lignes, définissez **TypeGuessRows** sur une valeur qui est basée sur la plage de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b1f30-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="b1f30-209">Pour vérifier toutes les lignes, définissez **TypeGuessRows** sur 1 048 576 (nombre maximal de lignes autorisées dans Excel).</span><span class="sxs-lookup"><span data-stu-id="b1f30-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="b1f30-210">Le type de données est déterminé par le nombre maximal de types de données qui sont trouvés.</span><span class="sxs-lookup"><span data-stu-id="b1f30-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="b1f30-211">En cas de lien, le type de données est déterminé dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="b1f30-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="b1f30-212">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1f30-212">Number</span></span>
- <span data-ttu-id="b1f30-213">Devise</span><span class="sxs-lookup"><span data-stu-id="b1f30-213">Currency</span></span>
- <span data-ttu-id="b1f30-214">Date</span><span class="sxs-lookup"><span data-stu-id="b1f30-214">Date</span></span>
- <span data-ttu-id="b1f30-215">Text</span><span class="sxs-lookup"><span data-stu-id="b1f30-215">Text</span></span>
- <span data-ttu-id="b1f30-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="b1f30-216">Boolean</span></span>

<span data-ttu-id="b1f30-217">Si des données ne correspondent pas au type de données devinées pour la colonne, ces données sont renvoyées sous la forme d'une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="b1f30-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="b1f30-218">Lors d'une importation, si une colonne possède des types de données mixtes, la colonne entière est convertie en un type de données défini par le paramètre **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="b1f30-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# [<a name="office-2010"></a><span data-ttu-id="b1f30-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="b1f30-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="b1f30-220">Pour Office 32 bits sur 32 bits Windows ou 64 bits sur Windows, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="b1f30-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

**<span data-ttu-id="b1f30-221">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-221">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel</span></span>**

<span data-ttu-id="b1f30-222">Pour Office 32 bits sur les Windows 64 bits:</span><span class="sxs-lookup"><span data-stu-id="b1f30-222">For 32-bit Office on 64-bit Windows:</span></span>

**<span data-ttu-id="b1f30-223">Engine\Engines\Excel de connectivité HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access</span><span class="sxs-lookup"><span data-stu-id="b1f30-223">HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel</span></span>**

<span data-ttu-id="b1f30-224">Le nombre par défaut de lignes à vérifier est **8** (huit).</span><span class="sxs-lookup"><span data-stu-id="b1f30-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="b1f30-225">Lorsque vous définissez la valeur **TypeGuessRows** sur **0** (zéro), le pilote Excel vérifie les premières lignes de 16 384 pour le type de données.</span><span class="sxs-lookup"><span data-stu-id="b1f30-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="b1f30-226">Si vous souhaitez vérifier plus de 16 384 lignes, définissez **TypeGuessRows** sur une valeur qui est basée sur la plage de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b1f30-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="b1f30-227">Pour vérifier toutes les lignes, définissez **TypeGuessRows** sur 1 048 576 (nombre maximal de lignes autorisées dans Excel).</span><span class="sxs-lookup"><span data-stu-id="b1f30-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="b1f30-228">Le type de données est déterminé par le nombre maximal de types de données qui sont trouvés.</span><span class="sxs-lookup"><span data-stu-id="b1f30-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="b1f30-229">En cas de lien, le type de données est déterminé dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="b1f30-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="b1f30-230">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1f30-230">Number</span></span>
- <span data-ttu-id="b1f30-231">Devise</span><span class="sxs-lookup"><span data-stu-id="b1f30-231">Currency</span></span>
- <span data-ttu-id="b1f30-232">Date</span><span class="sxs-lookup"><span data-stu-id="b1f30-232">Date</span></span>
- <span data-ttu-id="b1f30-233">Text</span><span class="sxs-lookup"><span data-stu-id="b1f30-233">Text</span></span>
- <span data-ttu-id="b1f30-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="b1f30-234">Boolean</span></span>

<span data-ttu-id="b1f30-235">Si des données ne correspondent pas au type de données devinées pour la colonne, ces données sont renvoyées sous la forme d'une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="b1f30-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="b1f30-236">Lors d'une importation, si une colonne possède des types de données mixtes, la colonne entière est convertie en un type de données défini par le paramètre **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="b1f30-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="b1f30-237">[!REMARQUE] Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="b1f30-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1f30-238">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1f30-238">See also</span></span>

- [<span data-ttu-id="b1f30-239">Utilisation du paramètre TypeGuessRows pour le pilote Excel</span><span class="sxs-lookup"><span data-stu-id="b1f30-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

