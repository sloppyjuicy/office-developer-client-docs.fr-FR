---
title: Connection.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1b4baff3bd1ca7d39fbf86f2002b73bda996f1a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471600"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="6ec97-102">Connection.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6ec97-102">Connection.Connect Property (DAO)</span></span>


<span data-ttu-id="6ec97-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ec97-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6ec97-p101">Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte. Valeur de type **String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6ec97-p101">Sets or returns a value that provides information about the source of an open connection. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec97-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ec97-106">Syntax</span></span>

<span data-ttu-id="6ec97-107">*expression* . Se connecter</span><span class="sxs-lookup"><span data-stu-id="6ec97-107">*expression* .Connect</span></span>

<span data-ttu-id="6ec97-108">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="6ec97-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec97-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ec97-109">Remarks</span></span>

<span data-ttu-id="6ec97-p102">Le paramètre de la propriété **Connect** est une valeur **String** constituée d'un spécificateur de type de base de données et de paramètres séparés par des points-virgules (ou aucun paramètre). La propriété **Connect** transmet des informations supplémentaires à ODBC et à certains pilotes ISAM, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6ec97-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="6ec97-112">Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.</span><span class="sxs-lookup"><span data-stu-id="6ec97-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="6ec97-113">Dans le cas d'un objet **TableDef** représentant une table liée, la valeur de la propriété **Connect** est constituée d'un ou de deux éléments (un spécificateur de type de base de données et un chemin d'accès à la base de données), se terminant chacun par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="6ec97-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="6ec97-p103">Le chemin d'accès indiqué dans le tableau ci-dessous correspond au chemin d'accès complet au répertoire contenant les fichiers de base de données. Il doit être précédé de l'identificateur DATABASE=. Dans certains cas (bases de données du moteur de base de données Microsoft Access et Microsoft Excel, par exemple), vous devez inclure un nom de fichier spécifique dans l'argument du chemin d'accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="6ec97-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="6ec97-116">Le tableau suivant indique les types de bases de données possibles, ainsi que leurs spécificateurs et chemins correspondants, pour la valeur de la propriété **Connect**.</span><span class="sxs-lookup"><span data-stu-id="6ec97-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ec97-117">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="6ec97-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="6ec97-118">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="6ec97-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="6ec97-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ec97-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-120">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="6ec97-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="6ec97-121">[base de données ;]</span><span class="sxs-lookup"><span data-stu-id="6ec97-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="6ec97-122">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="6ec97-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="6ec97-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="6ec97-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="6ec97-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-125">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="6ec97-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="6ec97-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="6ec97-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-128">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="6ec97-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="6ec97-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="6ec97-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-131">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="6ec97-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="6ec97-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="6ec97-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-134">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="6ec97-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="6ec97-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="6ec97-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-137">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="6ec97-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="6ec97-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="6ec97-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-140">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="6ec97-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="6ec97-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="6ec97-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-143">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="6ec97-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="6ec97-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="6ec97-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="6ec97-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-146">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="6ec97-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-147">Microsoft Excel 5.0 or Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="6ec97-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="6ec97-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="6ec97-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-149">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="6ec97-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="6ec97-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="6ec97-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="6ec97-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-152">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="6ec97-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-153">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="6ec97-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="6ec97-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="6ec97-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-155">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="6ec97-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="6ec97-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="6ec97-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="6ec97-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-158">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="6ec97-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="6ec97-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="6ec97-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="6ec97-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-161">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="6ec97-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-162">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="6ec97-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="6ec97-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="6ec97-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-164">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="6ec97-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-165">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="6ec97-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="6ec97-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="6ec97-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-167">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-168">Texte</span><span class="sxs-lookup"><span data-stu-id="6ec97-168">Text</span></span></p></td>
<td><p><span data-ttu-id="6ec97-169">Text;</span><span class="sxs-lookup"><span data-stu-id="6ec97-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="6ec97-170">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="6ec97-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec97-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="6ec97-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="6ec97-172">ODBC ; Base de données = base de données ; UID = utilisateur ; PWD = mot de passe ; DSN = NomSourceDonnées ; [LOGINTIMEOUT = secondes ;]</span><span class="sxs-lookup"><span data-stu-id="6ec97-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="6ec97-173">Aucune</span><span class="sxs-lookup"><span data-stu-id="6ec97-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec97-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="6ec97-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="6ec97-175">Exchange 4.0 ; MAPILEVEL = CheminDossier ; [TABLETYPE = {0 | 1}] ; [PROFILE = profil ;] [PWD = mot de passe ;] [Base de données = base de données ;]</span><span class="sxs-lookup"><span data-stu-id="6ec97-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="6ec97-176">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="6ec97-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6ec97-177">Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="6ec97-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="6ec97-178">Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.</span><span class="sxs-lookup"><span data-stu-id="6ec97-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="6ec97-179">Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »).</span><span class="sxs-lookup"><span data-stu-id="6ec97-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="6ec97-180">Le chemin d’accès n’inclut pas le nom du dossier qui s’ouvre sous forme de tableau ; nom du dossier doit être spécifié à la place l’argument nom de la méthode **Create table** .</span><span class="sxs-lookup"><span data-stu-id="6ec97-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="6ec97-181">La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="6ec97-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="6ec97-182">La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="6ec97-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="6ec97-183">Pour les tables de base d'une base de données Microsoft Access, la valeur de la propriété **Connect** est une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="6ec97-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="6ec97-184">Vous pouvez définir la propriété **Connect** d’un objet de **base de données** en fournissant un argument source dans la méthode **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="6ec97-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="6ec97-185">Consultez le paramètre pour connaître le type, le chemin d'accès, l'ID d'utilisateur, le mot de passe ou la source de données ODBC de la base de données.</span><span class="sxs-lookup"><span data-stu-id="6ec97-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="6ec97-186">Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC.</span><span class="sxs-lookup"><span data-stu-id="6ec97-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="6ec97-187">Databasetype de la chaîne de connexion est « ODBC ; », et le reste de la chaîne contient des informations spécifiques au pilote ODBC utilisé pour accéder aux données à distance.</span><span class="sxs-lookup"><span data-stu-id="6ec97-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="6ec97-188">Pour plus d'informations, consultez la documentation relative au pilote.</span><span class="sxs-lookup"><span data-stu-id="6ec97-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="6ec97-189">Vous devez définir la propriété <STRONG>Connect</STRONG> avant de définir la propriété <STRONG>ReturnsRecords</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6ec97-189">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="6ec97-190">Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.</span><span class="sxs-lookup"><span data-stu-id="6ec97-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


