---
title: TableDef.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eaedb53c8cb70746229e3f311ba5925e3b30ddef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470928"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="22a76-102">TableDef.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="22a76-102">TableDef.Connect Property (DAO)</span></span>


<span data-ttu-id="22a76-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22a76-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="22a76-p101">Définit ou renvoie une valeur qui donne des informations sur une table liée. Type de données **String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="22a76-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a76-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22a76-106">Syntax</span></span>

<span data-ttu-id="22a76-107">*expression* . Se connecter</span><span class="sxs-lookup"><span data-stu-id="22a76-107">*expression* .Connect</span></span>

<span data-ttu-id="22a76-108">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="22a76-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a76-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="22a76-109">Remarks</span></span>

<span data-ttu-id="22a76-p102">La valeur de la propriété **Connect** est un type de données **String** composé d'un spécificateur de type de base de données et de zéro caractères ou plus séparés par des points-virgules. La propriété **Connect** transmet des informations supplémentaires à ODBC et certains pilotes ISAM si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="22a76-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="22a76-112">Pour un objet **TableDef** qui représente une table liée, la valeur de la propriété **Connect** est constituée d'une ou de deux parties (un spécificateur de type de base de données et un chemin à la base de données), chacune se terminant par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="22a76-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="22a76-p103">Le chemin d'accès indiqué dans le tableau ci-dessous correspond au chemin d'accès complet au répertoire contenant les fichiers de base de données. Il doit être précédé de l'identificateur DATABASE=. Dans certains cas (bases de données du moteur de base de données Microsoft Access et Microsoft Excel, par exemple), vous devez inclure un nom de fichier spécifique dans l'argument du chemin d'accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="22a76-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="22a76-115">Le tableau suivant indique les types de bases de données possibles, ainsi que leurs spécificateurs et chemins correspondants, pour la valeur de la propriété **Connect**.</span><span class="sxs-lookup"><span data-stu-id="22a76-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22a76-116">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="22a76-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="22a76-117">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="22a76-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="22a76-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="22a76-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a76-119">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="22a76-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="22a76-120">[base de données ;]</span><span class="sxs-lookup"><span data-stu-id="22a76-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="22a76-121">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="22a76-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="22a76-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="22a76-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="22a76-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="22a76-124">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="22a76-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="22a76-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="22a76-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="22a76-127">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="22a76-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="22a76-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="22a76-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="22a76-130">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="22a76-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="22a76-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="22a76-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="22a76-133">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="22a76-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="22a76-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="22a76-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="22a76-136">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="22a76-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="22a76-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="22a76-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="22a76-139">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="22a76-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="22a76-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="22a76-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="22a76-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="22a76-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="22a76-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="22a76-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="22a76-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="22a76-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="22a76-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-146">Microsoft Excel 5.0 or Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="22a76-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="22a76-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="22a76-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="22a76-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="22a76-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="22a76-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="22a76-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="22a76-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="22a76-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="22a76-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-152">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="22a76-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="22a76-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="22a76-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="22a76-154">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="22a76-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="22a76-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="22a76-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="22a76-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="22a76-157">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="22a76-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="22a76-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="22a76-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="22a76-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="22a76-160">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="22a76-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-161">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="22a76-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="22a76-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="22a76-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="22a76-163">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="22a76-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-164">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="22a76-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="22a76-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="22a76-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="22a76-166">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-167">Texte</span><span class="sxs-lookup"><span data-stu-id="22a76-167">Text</span></span></p></td>
<td><p><span data-ttu-id="22a76-168">Text;</span><span class="sxs-lookup"><span data-stu-id="22a76-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="22a76-169">lecteur : \path</span><span class="sxs-lookup"><span data-stu-id="22a76-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a76-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="22a76-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="22a76-171">ODBC ; Base de données = base de données ; UID = utilisateur ; PWD = mot de passe ; DSN = NomSourceDonnées ; [LOGINTIMEOUT = secondes ;]</span><span class="sxs-lookup"><span data-stu-id="22a76-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="22a76-172">Aucune</span><span class="sxs-lookup"><span data-stu-id="22a76-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a76-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="22a76-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="22a76-174">Exchange 4.0 ; MAPILEVEL = CheminDossier ; [TABLETYPE = {0 | 1}] ; [PROFILE = profil ;] [PWD = mot de passe ;] [Base de données = base de données ;]</span><span class="sxs-lookup"><span data-stu-id="22a76-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="22a76-175">lecteur:\chemin_accès\nom_fichier</span><span class="sxs-lookup"><span data-stu-id="22a76-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22a76-176">Si un mot de passe est obligatoire et qu'il n'est pas fourni par la propriété **Connect**, une boîte de dialogue de connexion s'affiche la première fois que le pilote ODBC accède à une table et une nouvelle fois si la connexion est fermée et rouverte.</span><span class="sxs-lookup"><span data-stu-id="22a76-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="22a76-177">Pour les données dans Microsoft Exchange, la clé MAPILEVEL obligatoire doit être définie avec un chemin de dossier entièrement résolu (par exemple, « Mailbox - Pat SmithIAlpha/Today »).</span><span class="sxs-lookup"><span data-stu-id="22a76-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="22a76-178">Le chemin d’accès n’inclut pas le nom du dossier qui s’ouvre sous forme de tableau ; nom du dossier doit être spécifié à la place l’argument nom de la méthode **Create table** .</span><span class="sxs-lookup"><span data-stu-id="22a76-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="22a76-179">La clé TABLETYPE doit avoir la valeur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir un carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="22a76-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="22a76-180">La clé PROFILE prend la valeur par défaut du profil en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="22a76-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="22a76-181">Pour les tables de base d'une base de données Microsoft Access, la valeur de la propriété **Connect** est une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="22a76-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="22a76-182">Vous devez définir la propriété <STRONG>Connect</STRONG> avant de définir la propriété <STRONG>ReturnsRecords</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="22a76-182">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="22a76-183">Vous devez disposer des autorisations d'accès à l'ordinateur sur lequel se trouve le serveur de base de données auquel vous essayez d'accéder.</span><span class="sxs-lookup"><span data-stu-id="22a76-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>


