---
title: TableDef.Connect, propriété (DAO)
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
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314384"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="ace15-102">TableDef.Connect, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="ace15-102">TableDef.Connect Property (DAO)</span></span>

<span data-ttu-id="ace15-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ace15-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ace15-104">Définit ou renvoie une valeur qui fournit des informations sur une table liée.</span><span class="sxs-lookup"><span data-stu-id="ace15-104">Sets or returns a value that provides information about a linked table.</span></span> <span data-ttu-id="ace15-105">**String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ace15-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace15-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ace15-106">Syntax</span></span>

<span data-ttu-id="ace15-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="ace15-107">expression  . Connect</span></span>

<span data-ttu-id="ace15-108">*expression* Variable représentant un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="ace15-108">*expression*  A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace15-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="ace15-109">Remarks</span></span>

<span data-ttu-id="ace15-p102">Le **Connect** paramètre de la propriété est un **chaîne** composé d’un spécificateur de type base de données et de zéro ou plusieurs paramètres séparés par des points-virgules. Le **Connect** propriété transmet des informations supplémentaires à ODBC et certains pilotes ISAM selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ace15-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="ace15-112">Pour un **TableDef** objet qui représente une table liée, le **Connect** paramètre de la propriété se compose d’une ou deux parties (un spécificateur de type base de données et un chemin d’accès à la base de données), chacune se termine par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="ace15-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="ace15-113">Le chemin d’accès, comme illustré dans le tableau suivant est le chemin d’accès complet pour l’annuaire contenant les fichiers de base de données et doit être précédée de l’identificateur de base de données =.</span><span class="sxs-lookup"><span data-stu-id="ace15-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="ace15-114">Dans certains cas (comme avec Microsoft Excel et Microsoft Access base de données de bases de données moteur), un nom de fichier spécifiques à inclure dans l’argument de chemin d’accès de base de données.</span><span class="sxs-lookup"><span data-stu-id="ace15-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="ace15-115">Le tableau suivant indique les types de base de données possible et leur spécificateurs de base de données correspondantes et les chemins d’accès relatifs le **Connect** paramètre de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ace15-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ace15-116">Type de base de données</span><span class="sxs-lookup"><span data-stu-id="ace15-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="ace15-117">Spécificateur</span><span class="sxs-lookup"><span data-stu-id="ace15-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="ace15-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="ace15-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ace15-119">Base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="ace15-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="ace15-120">[database];</span><span class="sxs-lookup"><span data-stu-id="ace15-120">Database</span></span></p></td>
<td><p><span data-ttu-id="ace15-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="ace15-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-122">dBase III</span><span class="sxs-lookup"><span data-stu-id="ace15-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="ace15-123">dBase III</span><span class="sxs-lookup"><span data-stu-id="ace15-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="ace15-124">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-125">dBase IV</span><span class="sxs-lookup"><span data-stu-id="ace15-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="ace15-126">dBase IV</span><span class="sxs-lookup"><span data-stu-id="ace15-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="ace15-127">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-128">dBase 5</span><span class="sxs-lookup"><span data-stu-id="ace15-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="ace15-129">dBase 5.0</span><span class="sxs-lookup"><span data-stu-id="ace15-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="ace15-130">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="ace15-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="ace15-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="ace15-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="ace15-133">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="ace15-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="ace15-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="ace15-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="ace15-136">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="ace15-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="ace15-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="ace15-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="ace15-139">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-140">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="ace15-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="ace15-141">Excel 3.0 ;</span><span class="sxs-lookup"><span data-stu-id="ace15-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="ace15-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ace15-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-143">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="ace15-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="ace15-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="ace15-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="ace15-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ace15-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-146">Microsoft Excel 5.0 ou Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="ace15-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="ace15-147">Excel 5.0 ;</span><span class="sxs-lookup"><span data-stu-id="ace15-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="ace15-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ace15-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="ace15-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="ace15-150">Excel</span><span class="sxs-lookup"><span data-stu-id="ace15-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="ace15-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ace15-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-152">Lotus 1-2-3 WKS et WK1</span><span class="sxs-lookup"><span data-stu-id="ace15-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="ace15-153">Lotus WK1 ;</span><span class="sxs-lookup"><span data-stu-id="ace15-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="ace15-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="ace15-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-155">WK3 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="ace15-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="ace15-156">Lotus WK3 ;</span><span class="sxs-lookup"><span data-stu-id="ace15-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="ace15-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="ace15-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-158">WK4 Lotus 1-2-3</span><span class="sxs-lookup"><span data-stu-id="ace15-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="ace15-159">Lotus WK4 ;</span><span class="sxs-lookup"><span data-stu-id="ace15-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="ace15-160">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="ace15-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-161">Importation HTML</span><span class="sxs-lookup"><span data-stu-id="ace15-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="ace15-162">Importation HTML ;</span><span class="sxs-lookup"><span data-stu-id="ace15-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="ace15-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="ace15-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-164">Exportation HTML</span><span class="sxs-lookup"><span data-stu-id="ace15-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="ace15-165">Exportation HTML ;</span><span class="sxs-lookup"><span data-stu-id="ace15-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="ace15-166">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-167">Texte</span><span class="sxs-lookup"><span data-stu-id="ace15-167">Text</span></span></p></td>
<td><p><span data-ttu-id="ace15-168">Text;</span><span class="sxs-lookup"><span data-stu-id="ace15-168">Text</span></span></p></td>
<td><p><span data-ttu-id="ace15-169">drive:\path</span><span class="sxs-lookup"><span data-stu-id="ace15-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace15-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="ace15-170">ODBC Database</span></span></p></td>
<td><p><span data-ttu-id="ace15-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="ace15-171">ODBC;
DATABASE=database;
UID=user;
PWD=password;
DSN= datasourcename;
[LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="ace15-172">Aucun</span><span class="sxs-lookup"><span data-stu-id="ace15-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace15-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="ace15-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="ace15-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="ace15-174">Exchange 4.0;
MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;]
[PWD=password;]
[DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="ace15-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="ace15-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ace15-176">Si un mot de passe est requis sans être fourni dans le **Connect** propriété définissant, une boîte de dialogue Connexion s’affiche la première fois une table est accessible par le pilote ODBC puis de nouveau si la connexion est fermée et rouvert.</span><span class="sxs-lookup"><span data-stu-id="ace15-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="ace15-177">Pour les données dans Microsoft Exchange, vous devez définir la clé MAPILEVEL obligatoire pour un chemin d’accès du dossier entièrement résolu (par exemple, « boîte aux lettres – Pat SmithIAlpha/aujourd'hui »).</span><span class="sxs-lookup"><span data-stu-id="ace15-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="ace15-178">Le chemin n’inclut pas le nom du dossier qui sera ouvert en tant que table. Au lieu de cela, le nom du dossier doit être spécifié comme argument Name de la méthode **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="ace15-178">The path does not include the name of the folder that will be opened as a table; that folder's name should instead be specified as the  name argument to the **CreateTable** method.</span></span> <span data-ttu-id="ace15-179">La clé TABLETYPE doit être définie sur « 0 » pour ouvrir un dossier (par défaut) ou « 1 » pour ouvrir le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ace15-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="ace15-180">Les valeurs par défaut clés profil au profil actuellement utilisent.</span><span class="sxs-lookup"><span data-stu-id="ace15-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="ace15-181">Pour les tables de base dans une base de données Microsoft Access, la **Connect** paramètre de la propriété est une chaîne nulle (« »).</span><span class="sxs-lookup"><span data-stu-id="ace15-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="ace15-182">Vous devez définir la **Connect** propriété avant de définir la **ReturnsRecords** propriété.</span><span class="sxs-lookup"><span data-stu-id="ace15-182">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="ace15-183">Vous devez disposer des autorisations d’accès à l’ordinateur qui contient le serveur de base de données que vous essayez d’accéder.</span><span class="sxs-lookup"><span data-stu-id="ace15-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>
