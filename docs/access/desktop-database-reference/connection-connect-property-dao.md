---
title: Connexion. Connecter property (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295925"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="a0214-102">Connexion. Connecter property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0214-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="a0214-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0214-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0214-p101">Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte. Valeur de type **String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a0214-p101">Sets or returns a value that provides information about the source of an open connection. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0214-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0214-106">Syntax</span></span>

<span data-ttu-id="a0214-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="a0214-107">*expression* .Connect</span></span>

<span data-ttu-id="a0214-108">*expression* Variable qui représente un objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="a0214-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0214-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0214-109">Remarks</span></span>

<span data-ttu-id="a0214-p102">Le **Connect** paramètre de la propriété est un **chaîne** composé d’un spécificateur de type base de données et de zéro ou plusieurs paramètres séparés par des points-virgules. Le **Connect** propriété transmet des informations supplémentaires à ODBC et certains pilotes ISAM selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a0214-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="a0214-112">Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.</span><span class="sxs-lookup"><span data-stu-id="a0214-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="a0214-113">Pour un **TableDef** objet qui représente une table liée, le **Connect** paramètre de la propriété se compose d’une ou deux parties (un spécificateur de type base de données et un chemin d’accès à la base de données), chacune se termine par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="a0214-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="a0214-p103">Le chemin présenté dans le tableau suivant représente le chemin complet du répertoire contenant les fichiers de base de données ; il doit être précédé par l'identificateur DATABASE=. Dans certains cas (comme avec Microsoft Excel et les bases de données avec moteur de base de données Microsoft Access), vous devez inclure un nom de fichier spécifique à l'argument du chemin de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a0214-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="a0214-116">Le tableau suivant indique les types de base de données possible et leur spécificateurs de base de données correspondantes et les chemins d’accès relatifs le **Connect** paramètre de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a0214-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0214-117">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="a0214-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="a0214-118">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="a0214-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="a0214-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0214-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0214-120">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="a0214-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="a0214-121">[database];</span><span class="sxs-lookup"><span data-stu-id="a0214-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="a0214-122">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="a0214-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-123">dBase III</span><span class="sxs-lookup"><span data-stu-id="a0214-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="a0214-124">dBase III</span><span class="sxs-lookup"><span data-stu-id="a0214-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="a0214-125">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-126">dBase IV</span><span class="sxs-lookup"><span data-stu-id="a0214-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="a0214-127">dBase IV</span><span class="sxs-lookup"><span data-stu-id="a0214-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="a0214-128">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-129">dBase 5</span><span class="sxs-lookup"><span data-stu-id="a0214-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="a0214-130">dBase 5.0</span><span class="sxs-lookup"><span data-stu-id="a0214-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="a0214-131">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="a0214-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="a0214-133">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="a0214-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="a0214-134">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="a0214-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="a0214-136">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="a0214-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="a0214-137">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="a0214-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="a0214-139">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="a0214-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="a0214-140">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-141">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="a0214-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="a0214-142">Excel 3.0 ;</span><span class="sxs-lookup"><span data-stu-id="a0214-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="a0214-143">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="a0214-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-144">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="a0214-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="a0214-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="a0214-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="a0214-146">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="a0214-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-147">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="a0214-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="a0214-148">Excel 5.0 ;</span><span class="sxs-lookup"><span data-stu-id="a0214-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="a0214-149">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="a0214-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="a0214-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="a0214-151">Excel</span><span class="sxs-lookup"><span data-stu-id="a0214-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="a0214-152">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="a0214-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-153">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="a0214-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="a0214-154">Lotus WK1 ;</span><span class="sxs-lookup"><span data-stu-id="a0214-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="a0214-155">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="a0214-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-156">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="a0214-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="a0214-157">Lotus WK3 ;</span><span class="sxs-lookup"><span data-stu-id="a0214-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="a0214-158">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="a0214-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-159">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="a0214-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="a0214-160">Lotus WK4 ;</span><span class="sxs-lookup"><span data-stu-id="a0214-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="a0214-161">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="a0214-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-162">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="a0214-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="a0214-163">Importation HTML ;</span><span class="sxs-lookup"><span data-stu-id="a0214-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="a0214-164">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="a0214-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-165">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="a0214-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="a0214-166">Exportation HTML ;</span><span class="sxs-lookup"><span data-stu-id="a0214-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="a0214-167">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-168">Texte</span><span class="sxs-lookup"><span data-stu-id="a0214-168">Text</span></span></p></td>
<td><p><span data-ttu-id="a0214-169">Text;</span><span class="sxs-lookup"><span data-stu-id="a0214-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="a0214-170">drive:\path</span><span class="sxs-lookup"><span data-stu-id="a0214-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0214-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="a0214-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="a0214-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="a0214-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="a0214-173">Aucun</span><span class="sxs-lookup"><span data-stu-id="a0214-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0214-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="a0214-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="a0214-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="a0214-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="a0214-176">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="a0214-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0214-177">Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="a0214-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="a0214-178">Si un mot de passe est requis sans être fourni dans le **Connect** propriété définissant, une boîte de dialogue Connexion s’affiche la première fois une table est accessible par le pilote ODBC puis de nouveau si la connexion est fermée et rouvert.</span><span class="sxs-lookup"><span data-stu-id="a0214-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="a0214-179">Pour les données dans Microsoft Exchange, vous devez définir la clé MAPILEVEL obligatoire pour un chemin d’accès du dossier entièrement résolu (par exemple, « boîte aux lettres – Pat SmithIAlpha/aujourd'hui »).</span><span class="sxs-lookup"><span data-stu-id="a0214-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="a0214-180">Le chemin n’inclut pas le nom du dossier qui sera ouvert en tant que table. Au lieu de cela, le nom du dossier doit être spécifié comme argument Name de la méthode **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="a0214-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="a0214-181">La clé TABLETYPE doit être définie sur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a0214-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="a0214-182">Les valeurs par défaut clés profil au profil actuellement utilisent.</span><span class="sxs-lookup"><span data-stu-id="a0214-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="a0214-183">Pour les tables de base dans une base de données Microsoft Access, la **Connect** paramètre de la propriété est une chaîne nulle (« »).</span><span class="sxs-lookup"><span data-stu-id="a0214-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="a0214-184">Vous pouvez définir la propriété **Connecter** d’un objet **Database** en fournissant un argument source à la **méthode OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="a0214-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="a0214-185">Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a0214-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="a0214-186">Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC.</span><span class="sxs-lookup"><span data-stu-id="a0214-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="a0214-187">L’argument type_base_données de la chaîne de connexion correspond à "ODBC;" et la chaîne contient ensuite des informations spécifiques du pilote ODBC servant à accéder aux données distantes.</span><span class="sxs-lookup"><span data-stu-id="a0214-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="a0214-188">Pour plus d'informations, consultez la documentation relative au pilote.</span><span class="sxs-lookup"><span data-stu-id="a0214-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="a0214-189">Vous devez définir la **Connect** propriété avant de définir la **ReturnsRecords** propriété.</span><span class="sxs-lookup"><span data-stu-id="a0214-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="a0214-190">Vous devez disposer des autorisations d’accès à l’ordinateur qui contient le serveur de base de données que vous essayez d’accéder.</span><span class="sxs-lookup"><span data-stu-id="a0214-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


