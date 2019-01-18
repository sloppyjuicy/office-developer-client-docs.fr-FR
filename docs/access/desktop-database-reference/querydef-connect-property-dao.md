---
title: Propriété QueryDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698273"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="67872-102">Propriété QueryDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="67872-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="67872-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67872-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67872-p101">Définit ou renvoie une valeur qui fournit des informations sur la source de base de données dans une requête SQL directe. Type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="67872-p101">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="67872-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67872-106">Syntax</span></span>

<span data-ttu-id="67872-107">*expression* . Se connecter</span><span class="sxs-lookup"><span data-stu-id="67872-107">*expression* .Connect</span></span>

<span data-ttu-id="67872-108">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="67872-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67872-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="67872-109">Remarks</span></span>

<span data-ttu-id="67872-p102">Le paramètre de la propriété **Connect** est une valeur **String** constituée d'un spécificateur de type de base de données et de paramètres séparés par des points-virgules (ou aucun paramètre). La propriété **Connect** transmet des informations supplémentaires à ODBC et à certains pilotes ISAM, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="67872-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="67872-112">Pour exécuter une requête SQL directe sur une table liée au fichier de base de données Microsoft Access, vous devez d'abord définir la propriété **Connect** de la base de données de la table liée sur une chaîne de connexion ODBC valide.</span><span class="sxs-lookup"><span data-stu-id="67872-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="67872-p103">Le chemin d'accès indiqué dans le tableau ci-dessous correspond au chemin d'accès complet au répertoire contenant les fichiers de base de données. Il doit être précédé de l'identificateur DATABASE=. Dans certains cas (bases de données du moteur de base de données Microsoft Access et Microsoft Excel, par exemple), vous devez inclure un nom de fichier spécifique dans l'argument du chemin d'accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="67872-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="67872-115">Le tableau suivant indique les types de bases de données possibles, ainsi que leurs spécificateurs et chemins correspondants, pour la valeur de la propriété **Connect**.</span><span class="sxs-lookup"><span data-stu-id="67872-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67872-116">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="67872-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="67872-117">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="67872-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="67872-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="67872-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67872-119">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="67872-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="67872-120">[base de données ;]</span><span class="sxs-lookup"><span data-stu-id="67872-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="67872-121">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="67872-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="67872-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="67872-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="67872-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="67872-124">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="67872-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="67872-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="67872-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="67872-127">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="67872-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="67872-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="67872-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="67872-130">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="67872-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="67872-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="67872-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="67872-133">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="67872-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="67872-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="67872-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="67872-136">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="67872-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="67872-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="67872-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="67872-139">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="67872-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="67872-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="67872-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="67872-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="67872-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="67872-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="67872-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="67872-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="67872-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="67872-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-146">Microsoft Excel 5.0 or Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="67872-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="67872-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="67872-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="67872-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="67872-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="67872-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="67872-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="67872-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="67872-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="67872-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-152">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="67872-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="67872-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="67872-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="67872-154">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="67872-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="67872-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="67872-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="67872-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="67872-157">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="67872-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="67872-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="67872-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="67872-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="67872-160">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="67872-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-161">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="67872-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="67872-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="67872-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="67872-163">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="67872-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-164">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="67872-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="67872-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="67872-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="67872-166">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-167">Texte</span><span class="sxs-lookup"><span data-stu-id="67872-167">Text</span></span></p></td>
<td><p><span data-ttu-id="67872-168">Text;</span><span class="sxs-lookup"><span data-stu-id="67872-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="67872-169">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="67872-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67872-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="67872-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="67872-171">ODBC ; Base de données = base de données ; UID = utilisateur ; PWD = mot de passe ; DSN = NomSourceDonnées ; [LOGINTIMEOUT = secondes ;]</span><span class="sxs-lookup"><span data-stu-id="67872-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="67872-172">Aucun</span><span class="sxs-lookup"><span data-stu-id="67872-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67872-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="67872-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="67872-174">Exchange 4.0 ; MAPILEVEL = CheminDossier ; [TABLETYPE = {0 | 1}] ; [PROFILE = profil ;] [PWD = mot de passe ;] [Base de données = base de données ;]</span><span class="sxs-lookup"><span data-stu-id="67872-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="67872-175">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="67872-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67872-176">Si le spécificateur est uniquement "ODBC;", le pilote ODBC affiche une boîte de dialogue répertoriant tous les noms des sources de données ODBC enregistrées pour permettre à l'utilisateur de sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="67872-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="67872-177">Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.</span><span class="sxs-lookup"><span data-stu-id="67872-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="67872-178">Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »).</span><span class="sxs-lookup"><span data-stu-id="67872-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="67872-179">Le chemin d’accès n’inclut pas le nom du dossier qui s’ouvre sous forme de tableau ; nom du dossier doit être spécifié à la place l’argument nom de la méthode **Create table** .</span><span class="sxs-lookup"><span data-stu-id="67872-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="67872-180">La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="67872-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="67872-181">La clé PROFILE a par défaut la valeur du profil actuellement utilisé.</span><span class="sxs-lookup"><span data-stu-id="67872-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="67872-182">Dans un objet **QueryDef** d'un espace de travail Microsoft Access, vous pouvez utiliser la propriété **Connect** avec la propriété ReturnsRecords afin de créer une requête SQL directe ODBC.</span><span class="sxs-lookup"><span data-stu-id="67872-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="67872-183">Databasetype de la chaîne de connexion est « ODBC ; », et le reste de la chaîne contient des informations spécifiques au pilote ODBC utilisé pour accéder aux données à distance.</span><span class="sxs-lookup"><span data-stu-id="67872-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="67872-184">Pour plus d'informations, consultez la documentation relative au pilote.</span><span class="sxs-lookup"><span data-stu-id="67872-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="67872-185">Vous devez définir la propriété **Connect** avant de définir la propriété **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="67872-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="67872-186">Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.</span><span class="sxs-lookup"><span data-stu-id="67872-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


