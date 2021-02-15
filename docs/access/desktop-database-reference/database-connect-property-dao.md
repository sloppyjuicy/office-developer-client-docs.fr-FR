---
title: Database.Connect, propriété (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb3566a4f402c1b8ae75a47880f2101bf35d77db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294987"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="8094f-102">Database.Connect, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="8094f-102">Database.Connect property (DAO)</span></span>


<span data-ttu-id="8094f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8094f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8094f-104">Définit ou renvoie une valeur qui fournit des informations sur la source d'une base de données ouverte.</span><span class="sxs-lookup"><span data-stu-id="8094f-104">Sets or returns a value that provides information about the source an open database.</span></span> <span data-ttu-id="8094f-105">**String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8094f-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8094f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8094f-106">Syntax</span></span>

<span data-ttu-id="8094f-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="8094f-107">*expression* .Connect</span></span>

<span data-ttu-id="8094f-108">*expression* Variable qui représente un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="8094f-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8094f-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="8094f-109">Remarks</span></span>

<span data-ttu-id="8094f-p102">Le **Connect** paramètre de la propriété est un **chaîne** composé d’un spécificateur de type base de données et de zéro ou plusieurs paramètres séparés par des points-virgules. Le **Connect** propriété transmet des informations supplémentaires à ODBC et certains pilotes ISAM selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8094f-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="8094f-112">Pour exécuter une requête SQL directe sur une table liée à votre fichier de base de données Microsoft Access, vous devez d'abord affecter une chaîne de connexion ODBC valide à la propriété **Connect** de la base de données de la table liée.</span><span class="sxs-lookup"><span data-stu-id="8094f-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="8094f-113">Le chemin d’accès, comme illustré dans le tableau suivant est le chemin d’accès complet pour l’annuaire contenant les fichiers de base de données et doit être précédée de l’identificateur de base de données =.</span><span class="sxs-lookup"><span data-stu-id="8094f-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="8094f-114">Dans certains cas (comme avec Microsoft Excel et Microsoft Access base de données de bases de données moteur), un nom de fichier spécifiques à inclure dans l’argument de chemin d’accès de base de données.</span><span class="sxs-lookup"><span data-stu-id="8094f-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="8094f-115">Le tableau suivant indique les types de base de données possible et leur spécificateurs de base de données correspondantes et les chemins d’accès relatifs le **Connect** paramètre de la propriété.</span><span class="sxs-lookup"><span data-stu-id="8094f-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8094f-116">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="8094f-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="8094f-117">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="8094f-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="8094f-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="8094f-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8094f-119">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="8094f-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="8094f-120">[database];</span><span class="sxs-lookup"><span data-stu-id="8094f-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="8094f-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8094f-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-122">dBase III</span><span class="sxs-lookup"><span data-stu-id="8094f-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="8094f-123">dBase III</span><span class="sxs-lookup"><span data-stu-id="8094f-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="8094f-124">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-125">dBase IV</span><span class="sxs-lookup"><span data-stu-id="8094f-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="8094f-126">dBase IV</span><span class="sxs-lookup"><span data-stu-id="8094f-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="8094f-127">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-128">dBase 5</span><span class="sxs-lookup"><span data-stu-id="8094f-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="8094f-129">dBase 5.0</span><span class="sxs-lookup"><span data-stu-id="8094f-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8094f-130">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="8094f-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="8094f-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="8094f-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="8094f-133">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="8094f-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="8094f-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="8094f-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="8094f-136">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="8094f-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="8094f-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="8094f-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="8094f-139">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-140">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="8094f-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="8094f-141">Excel 3.0 ;</span><span class="sxs-lookup"><span data-stu-id="8094f-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="8094f-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8094f-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-143">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="8094f-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="8094f-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="8094f-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="8094f-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8094f-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="8094f-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="8094f-147">Excel 5.0 ;</span><span class="sxs-lookup"><span data-stu-id="8094f-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="8094f-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8094f-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="8094f-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="8094f-150">Excel</span><span class="sxs-lookup"><span data-stu-id="8094f-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="8094f-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="8094f-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-152">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="8094f-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="8094f-153">Lotus WK1 ;</span><span class="sxs-lookup"><span data-stu-id="8094f-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="8094f-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="8094f-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-155">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="8094f-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="8094f-156">Lotus WK3 ;</span><span class="sxs-lookup"><span data-stu-id="8094f-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="8094f-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="8094f-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-158">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="8094f-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="8094f-159">Lotus WK4 ;</span><span class="sxs-lookup"><span data-stu-id="8094f-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="8094f-160">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="8094f-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-161">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="8094f-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="8094f-162">Importation HTML ;</span><span class="sxs-lookup"><span data-stu-id="8094f-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="8094f-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8094f-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-164">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="8094f-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="8094f-165">Exportation HTML ;</span><span class="sxs-lookup"><span data-stu-id="8094f-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="8094f-166">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-167">Texte</span><span class="sxs-lookup"><span data-stu-id="8094f-167">Text</span></span></p></td>
<td><p><span data-ttu-id="8094f-168">Text;</span><span class="sxs-lookup"><span data-stu-id="8094f-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="8094f-169">drive:\path</span><span class="sxs-lookup"><span data-stu-id="8094f-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8094f-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="8094f-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="8094f-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="8094f-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="8094f-172">Aucun</span><span class="sxs-lookup"><span data-stu-id="8094f-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8094f-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8094f-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="8094f-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="8094f-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="8094f-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="8094f-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8094f-176">Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="8094f-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="8094f-177">Si un mot de passe est requis sans être fourni dans le **Connect** propriété définissant, une boîte de dialogue Connexion s’affiche la première fois une table est accessible par le pilote ODBC puis de nouveau si la connexion est fermée et rouvert.</span><span class="sxs-lookup"><span data-stu-id="8094f-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="8094f-178">Pour les données dans Microsoft Exchange, vous devez définir la clé MAPILEVEL obligatoire pour un chemin d’accès du dossier entièrement résolu (par exemple, « boîte aux lettres – Pat SmithIAlpha/aujourd'hui »).</span><span class="sxs-lookup"><span data-stu-id="8094f-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="8094f-179">Le chemin n’inclut pas le nom du dossier qui sera ouvert en tant que table. Au lieu de cela, le nom du dossier doit être spécifié comme argument Name de la méthode **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="8094f-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="8094f-180">La clé TABLETYPE doit être définie sur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8094f-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="8094f-181">Les valeurs par défaut clés profil au profil actuellement utilisent.</span><span class="sxs-lookup"><span data-stu-id="8094f-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="8094f-182">Vous pouvez définir la **propriété Connect** d’un objet **Database** en fournissant un argument source à la **méthode OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="8094f-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="8094f-183">Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8094f-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="8094f-184">Vous devez définir la **Connect** propriété avant de définir la **ReturnsRecords** propriété.</span><span class="sxs-lookup"><span data-stu-id="8094f-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="8094f-185">Vous devez disposer des autorisations d’accès à l’ordinateur qui contient le serveur de base de données que vous essayez d’accéder.</span><span class="sxs-lookup"><span data-stu-id="8094f-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


