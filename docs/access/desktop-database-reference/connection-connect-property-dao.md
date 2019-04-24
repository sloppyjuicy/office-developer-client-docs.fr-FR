---
title: Connection. Connect, propriété (DAO)
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
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="25d77-102">Connection. Connect, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="25d77-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="25d77-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25d77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25d77-104">Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte.</span><span class="sxs-lookup"><span data-stu-id="25d77-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="25d77-105">Type de données **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="25d77-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d77-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25d77-106">Syntax</span></span>

<span data-ttu-id="25d77-107">*expression* . Connexions</span><span class="sxs-lookup"><span data-stu-id="25d77-107">*expression* .Connect</span></span>

<span data-ttu-id="25d77-108">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="25d77-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="25d77-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="25d77-109">Remarks</span></span>

<span data-ttu-id="25d77-p102">Le paramètre de la propriété **Connect** est un type **String** composé d'un spécificateur de type de base de données et de zéro ou plusieurs paramètres séparés par des points-virgules. La propriété **Connect** passe des informations complémentaires à ODBC et à certains pilotes ISAM selon les circonstances.</span><span class="sxs-lookup"><span data-stu-id="25d77-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="25d77-112">Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.</span><span class="sxs-lookup"><span data-stu-id="25d77-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="25d77-113">Dans le cas d'un objet **TableDef** représentant une table liée, la valeur de la propriété **Connect** est constituée d'un ou de deux éléments (un spécificateur de type de base de données et un chemin d'accès à la base de données), se terminant chacun par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="25d77-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="25d77-114">Le chemin présenté dans le tableau suivant représente le chemin complet du répertoire contenant les fichiers de base de données ; il doit être précédé par l'identificateur DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="25d77-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="25d77-115">Dans certains cas (comme avec Microsoft Excel et les bases de données avec moteur de base de données Microsoft Access), vous devez inclure un nom de fichier spécifique à l'argument du chemin de la base de données.</span><span class="sxs-lookup"><span data-stu-id="25d77-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="25d77-116">Le tableau suivant indique les types de bases de données possibles, ainsi que leurs spécificateurs et chemins correspondants, pour la valeur de la propriété **Connect**.</span><span class="sxs-lookup"><span data-stu-id="25d77-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25d77-117">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="25d77-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="25d77-118">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="25d77-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="25d77-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="25d77-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25d77-120">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="25d77-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="25d77-121">[base de données];</span><span class="sxs-lookup"><span data-stu-id="25d77-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="25d77-122">lecteur: \ chemin\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="25d77-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="25d77-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="25d77-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="25d77-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="25d77-125">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="25d77-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="25d77-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="25d77-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="25d77-128">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="25d77-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="25d77-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="25d77-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="25d77-131">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="25d77-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="25d77-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="25d77-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="25d77-134">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="25d77-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="25d77-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="25d77-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="25d77-137">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="25d77-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="25d77-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="25d77-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="25d77-140">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="25d77-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="25d77-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="25d77-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="25d77-143">lecteur: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="25d77-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="25d77-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="25d77-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="25d77-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="25d77-146">lecteur: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="25d77-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-147">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="25d77-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="25d77-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="25d77-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="25d77-149">lecteur: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="25d77-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="25d77-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="25d77-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="25d77-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="25d77-152">lecteur: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="25d77-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-153">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="25d77-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="25d77-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="25d77-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="25d77-155">lecteur: \ path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="25d77-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="25d77-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="25d77-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="25d77-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="25d77-158">lecteur: \ path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="25d77-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="25d77-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="25d77-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="25d77-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="25d77-161">lecteur: \ path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="25d77-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-162">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="25d77-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="25d77-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="25d77-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="25d77-164">lecteur: \ chemin\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="25d77-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-165">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="25d77-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="25d77-166">Export HTML;</span><span class="sxs-lookup"><span data-stu-id="25d77-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="25d77-167">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-168">Texte</span><span class="sxs-lookup"><span data-stu-id="25d77-168">Text</span></span></p></td>
<td><p><span data-ttu-id="25d77-169">Textes</span><span class="sxs-lookup"><span data-stu-id="25d77-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="25d77-170">lecteur: \ chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="25d77-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d77-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="25d77-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="25d77-172">ODBC BASE de données = base de données; UID = utilisateur; PWD = mot de passe; DSN = DataSourceName; [LOGINTIMEOUT = secondes;]</span><span class="sxs-lookup"><span data-stu-id="25d77-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="25d77-173">Aucun</span><span class="sxs-lookup"><span data-stu-id="25d77-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d77-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="25d77-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="25d77-175">Exchange 4,0; MAPILEVEL = folderPath; [TABLETYPE = {0 | 1}]; [PROFILe = profil;] [PWD = mot de passe;] [Base de données = base de données;]</span><span class="sxs-lookup"><span data-stu-id="25d77-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="25d77-176">lecteur: \ chemin\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="25d77-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25d77-177">Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="25d77-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="25d77-178">Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.</span><span class="sxs-lookup"><span data-stu-id="25d77-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="25d77-179">Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »).</span><span class="sxs-lookup"><span data-stu-id="25d77-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="25d77-180">Le chemin d'accès n'inclut pas le nom du dossier qui sera ouvert en tant que table; le nom de ce dossier doit plutôt être spécifié en tant qu'argument nom de la méthode **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="25d77-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="25d77-181">La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="25d77-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="25d77-182">La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="25d77-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="25d77-183">Pour les tables de base d'une base de données Microsoft Access, la valeur de la propriété **Connect** est une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="25d77-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="25d77-184">Vous pouvez définir la propriété **Connect** d'un objet **Database** en fournissant un argument source à la méthode **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="25d77-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="25d77-185">Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.</span><span class="sxs-lookup"><span data-stu-id="25d77-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="25d77-186">Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC.</span><span class="sxs-lookup"><span data-stu-id="25d77-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="25d77-187">L’argument type_base_données de la chaîne de connexion correspond à "ODBC;" et la chaîne contient ensuite des informations spécifiques du pilote ODBC servant à accéder aux données distantes.</span><span class="sxs-lookup"><span data-stu-id="25d77-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="25d77-188">Pour plus d'informations, consultez la documentation relative au pilote.</span><span class="sxs-lookup"><span data-stu-id="25d77-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="25d77-189">Vous devez définir la propriété **Connect** avant de définir la propriété **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="25d77-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="25d77-190">Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.</span><span class="sxs-lookup"><span data-stu-id="25d77-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


