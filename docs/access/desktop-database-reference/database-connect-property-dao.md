---
title: Database.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b497e2859b265f5bb939fdd2b4913a54fdf2d170
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864199"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="595d2-102">Database.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="595d2-102">Database.Connect Property (DAO)</span></span>


<span data-ttu-id="595d2-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="595d2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="595d2-p101">Définit ou renvoie une valeur qui fournit des informations sur la source d'une base de données ouverte. Valeur de type **String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="595d2-p101">Sets or returns a value that provides information about the source an open database. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="595d2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="595d2-106">Syntax</span></span>

<span data-ttu-id="595d2-107">*expression* . Se connecter</span><span class="sxs-lookup"><span data-stu-id="595d2-107">*expression* .Connect</span></span>

<span data-ttu-id="595d2-108">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="595d2-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="595d2-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="595d2-109">Remarks</span></span>

<span data-ttu-id="595d2-p102">Le paramètre de la propriété **Connect** est une valeur **String** constituée d'un spécificateur de type de base de données et de paramètres séparés par des points-virgules (ou aucun paramètre). La propriété **Connect** transmet des informations supplémentaires à ODBC et à certains pilotes ISAM, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="595d2-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="595d2-112">Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.</span><span class="sxs-lookup"><span data-stu-id="595d2-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="595d2-p103">Le chemin d'accès indiqué dans le tableau ci-dessous correspond au chemin d'accès complet au répertoire contenant les fichiers de base de données. Il doit être précédé de l'identificateur DATABASE=. Dans certains cas (bases de données du moteur de base de données Microsoft Access et Microsoft Excel, par exemple), vous devez inclure un nom de fichier spécifique dans l'argument du chemin d'accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="595d2-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="595d2-115">Le tableau suivant indique les types de bases de données possibles, ainsi que leurs spécificateurs et chemins correspondants, pour la valeur de la propriété **Connect**.</span><span class="sxs-lookup"><span data-stu-id="595d2-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="595d2-116">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="595d2-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="595d2-117">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="595d2-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="595d2-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="595d2-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="595d2-119">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="595d2-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="595d2-120">[base de données ;]</span><span class="sxs-lookup"><span data-stu-id="595d2-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="595d2-121">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="595d2-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="595d2-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="595d2-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="595d2-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="595d2-124">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="595d2-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="595d2-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="595d2-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="595d2-127">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="595d2-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="595d2-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="595d2-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="595d2-130">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="595d2-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="595d2-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="595d2-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="595d2-133">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="595d2-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="595d2-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="595d2-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="595d2-136">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="595d2-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="595d2-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="595d2-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="595d2-139">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="595d2-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="595d2-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="595d2-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="595d2-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="595d2-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="595d2-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="595d2-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="595d2-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="595d2-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="595d2-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-146">Microsoft Excel 5.0 or Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="595d2-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="595d2-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="595d2-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="595d2-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="595d2-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="595d2-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="595d2-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="595d2-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="595d2-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="595d2-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-152">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="595d2-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="595d2-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="595d2-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="595d2-154">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="595d2-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="595d2-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="595d2-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="595d2-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="595d2-157">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="595d2-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="595d2-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="595d2-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="595d2-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="595d2-160">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="595d2-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-161">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="595d2-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="595d2-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="595d2-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="595d2-163">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="595d2-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-164">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="595d2-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="595d2-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="595d2-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="595d2-166">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-167">Texte</span><span class="sxs-lookup"><span data-stu-id="595d2-167">Text</span></span></p></td>
<td><p><span data-ttu-id="595d2-168">Text;</span><span class="sxs-lookup"><span data-stu-id="595d2-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="595d2-169">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="595d2-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="595d2-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="595d2-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="595d2-171">ODBC ; Base de données = base de données ; UID = utilisateur ; PWD = mot de passe ; DSN = NomSourceDonnées ; [LOGINTIMEOUT = secondes ;]</span><span class="sxs-lookup"><span data-stu-id="595d2-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="595d2-172">Aucune</span><span class="sxs-lookup"><span data-stu-id="595d2-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="595d2-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="595d2-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="595d2-174">Exchange 4.0 ; MAPILEVEL = CheminDossier ; [TABLETYPE = {0 | 1}] ; [PROFILE = profil ;] [PWD = mot de passe ;] [Base de données = base de données ;]</span><span class="sxs-lookup"><span data-stu-id="595d2-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="595d2-175">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="595d2-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="595d2-176">Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="595d2-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="595d2-177">Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.</span><span class="sxs-lookup"><span data-stu-id="595d2-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="595d2-178">Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »).</span><span class="sxs-lookup"><span data-stu-id="595d2-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="595d2-179">Le chemin d’accès n’inclut pas le nom du dossier qui s’ouvre sous forme de tableau ; nom du dossier doit être spécifié à la place l’argument nom de la méthode **Create table** .</span><span class="sxs-lookup"><span data-stu-id="595d2-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="595d2-180">La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="595d2-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="595d2-181">La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="595d2-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="595d2-182">Vous pouvez définir la propriété **Connect** d’un objet de **base de données** en fournissant un argument source dans la méthode **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="595d2-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="595d2-183">Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.</span><span class="sxs-lookup"><span data-stu-id="595d2-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="595d2-184">Vous devez définir la propriété **Connect** avant la propriété **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="595d2-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="595d2-185">Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.</span><span class="sxs-lookup"><span data-stu-id="595d2-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


