---
title: DBEngine.CompactDatabase Method (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294336"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="73ee9-102">DBEngine.CompactDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="73ee9-102">DBEngine.CompactDatabase Method (DAO)</span></span>

<span data-ttu-id="73ee9-103">**S’applique à :** Access 2013 | Access 2016</span><span class="sxs-lookup"><span data-stu-id="73ee9-103">**Applies to:** Access 2013 | Access 2016</span></span>

<span data-ttu-id="73ee9-104">Copie et compacte une base de données fermée, et vous donne la possibilité de changer sa version, son ordre de tri, et son chiffrement.</span><span class="sxs-lookup"><span data-stu-id="73ee9-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, encryption, and other options.</span></span> <span data-ttu-id="73ee9-105">(Espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="73ee9-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="73ee9-106">Lorsque vous utilisez les tableaux liés chiffrés pour une action, mise à jour et requêtes SQL [par exemple, une instruction SQL de mise à jour (CurrentDb.Execute « Mettre à jour... »)], vous devez fournir la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="73ee9-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="73ee9-107">Par ailleurs, les tableaux liés sont limités à 19 caractères pour la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="73ee9-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="73ee9-108">Voir la section**Tables liés chiffrés** à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="73ee9-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ee9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73ee9-109">Syntax</span></span>

<span data-ttu-id="73ee9-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span><span class="sxs-lookup"><span data-stu-id="73ee9-110">CompactDatabase(\*\*\*\*SrcName\*\*\*\*, ***DstName***, ***DstLocale, \*\*\*\*\*\*Options, \*\*\*\*\*\*password***)</span></span>

<span data-ttu-id="73ee9-111">*expression*Expression renvoyant un objet **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-111">*expression*  An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="73ee9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73ee9-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73ee9-113">Nom</span><span class="sxs-lookup"><span data-stu-id="73ee9-113">Name</span></span></p></th>
<th><p><span data-ttu-id="73ee9-114">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="73ee9-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="73ee9-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="73ee9-115">Data type</span></span></p></th>
<th><p><span data-ttu-id="73ee9-116">Description</span><span class="sxs-lookup"><span data-stu-id="73ee9-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-117"><em>SrcName</em></span><span class="sxs-lookup"><span data-stu-id="73ee9-117"><em>SrcName</em></span></span></p></td>
<td><p><span data-ttu-id="73ee9-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73ee9-118">Required</span></span></p></td>
<td><p><span data-ttu-id="73ee9-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-120">Identifie une base de données existante, fermée.</span><span class="sxs-lookup"><span data-stu-id="73ee9-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="73ee9-121">Il peut s'agir d'un nom de fichier et chemin d'accès complet, par exemple&quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="73ee9-121">It can be a full path and file name, such as "C:\db1.mdb".</span></span> <span data-ttu-id="73ee9-122">Si le nom de fichier a une extension, vous devez la spécifier.</span><span class="sxs-lookup"><span data-stu-id="73ee9-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="73ee9-123">Si votre réseau assure la prise en charge des chemins d'accès réseau, vous pouvez également préciser celui-ci, par exemple &quot;\\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="73ee9-123">If your network supports it, you can also specify a network path, such as "\\server1\share1\dir1\db1.mdb"</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-124"><em>DstName</em></span><span class="sxs-lookup"><span data-stu-id="73ee9-124"><em>DstName</em></span></span></p></td>
<td><p><span data-ttu-id="73ee9-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="73ee9-125">Required</span></span></p></td>
<td><p><span data-ttu-id="73ee9-126"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-127">Nom de fichier (et chemin d'accès) de la base de données compactée que vous créez.</span><span class="sxs-lookup"><span data-stu-id="73ee9-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="73ee9-128">Il est également possible de spécifier un chemin d'accès réseau.</span><span class="sxs-lookup"><span data-stu-id="73ee9-128">You can also specify a network path.</span></span> <span data-ttu-id="73ee9-129">Vous ne pouvez pas utiliser cet argument pour indiquer le même fichier de base de données que SrcName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-129">You can't use this  argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-130"><em>DstLocale</em></span><span class="sxs-lookup"><span data-stu-id="73ee9-130"><em>DstLocale</em></span></span></p></td>
<td><p><span data-ttu-id="73ee9-131">Facultatif</span><span class="sxs-lookup"><span data-stu-id="73ee9-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="73ee9-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-133">Expression en chaîne qui spécifie un ordre d’assemblage pour créer DstName, comme spécifié dans Remarques.</span><span class="sxs-lookup"><span data-stu-id="73ee9-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="73ee9-134">Si vous omettez cet argument, les paramètres régionaux de DstName sont identiques à SrcName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="73ee9-135">Vous pouvez également créer un mot de passe pour DstName par la concaténation de la chaîne de mot de passe (en commençant par &quot;;pwd=&quot;) avec une constante dans l'argument DstLocale, comme suit : dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span><span class="sxs-lookup"><span data-stu-id="73ee9-135">You can also create a password for DstName by concatenating the password string (starting with ";pwd=") with a constant in the DstLocale argument, like this: dbLangSpanish & ";pwd=NewPassword".</span></span></p></li>
<li><p><span data-ttu-id="73ee9-136">Pour utiliser le même argument DstLocale que SrcName (valeur par défaut) mais un nouveau mot de passe, entrez simplement une chaîne de mot de passe pour DstLocale: &quot;;pwd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="73ee9-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: ";pwd=NewPassword"</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-137"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="73ee9-137"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="73ee9-138">Facultatif</span><span class="sxs-lookup"><span data-stu-id="73ee9-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="73ee9-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-p105">Facultatif. Constante ou combinaison de constantes qui indique une ou plusieurs options, comme indiqué dans la section Remarques. Vous pouvez combiner des options en associant les constantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="73ee9-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-143"><em>mot de passe</em></span><span class="sxs-lookup"><span data-stu-id="73ee9-143"><em>Password</em></span></span></p></td>
<td><p><span data-ttu-id="73ee9-144">Facultatif</span><span class="sxs-lookup"><span data-stu-id="73ee9-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="73ee9-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-146">Expression de chaîne contenant une clé de chiffrement, si la base de données est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="73ee9-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="73ee9-147">La chaîne &quot;; pwd =&quot; doit précéder le mot de passe réel.</span><span class="sxs-lookup"><span data-stu-id="73ee9-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="73ee9-148">Si vous incluez un paramètre de mot de passe dans DstLocale, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="73ee9-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p><p><span data-ttu-id="73ee9-149"><strong>Remarque</strong>: il s’agit d’un paramètre obsolète et n’est pas pris en charge dans le format .ACCDB.</span><span class="sxs-lookup"><span data-stu-id="73ee9-149"><strong>NOTE</strong>: This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="73ee9-150">Pour chiffrer un fichier .ACCDB, utilisez le « pwd = » option chaîne.</span><span class="sxs-lookup"><span data-stu-id="73ee9-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="73ee9-151">Il est recommandé d'utiliser des mots de passe forts qui combinent des lettres majuscules et minuscules, des chiffres et des signes.</span><span class="sxs-lookup"><span data-stu-id="73ee9-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="73ee9-152">Les mots de passe faibles ne regroupent pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="73ee9-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="73ee9-153">Mot de passe fort : Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="73ee9-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="73ee9-154">Mot de passe faible : Maison27.</span><span class="sxs-lookup"><span data-stu-id="73ee9-154">Weak password: House27.</span></span> <span data-ttu-id="73ee9-155">Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</span><span class="sxs-lookup"><span data-stu-id="73ee9-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="73ee9-156">Remarques</span><span class="sxs-lookup"><span data-stu-id="73ee9-156">Remarks</span></span>

<span data-ttu-id="73ee9-157">Vous pouvez utiliser l'une des constantes suivantes pour l'argument DstLocale afin de spécifier la propriété **CollatingOrder**du texte pour des comparaisons de chaînes.</span><span class="sxs-lookup"><span data-stu-id="73ee9-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73ee9-158">Constante</span><span class="sxs-lookup"><span data-stu-id="73ee9-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="73ee9-159">Ordre de classement</span><span class="sxs-lookup"><span data-stu-id="73ee9-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-161">Anglais, allemand, français, portugais, italien et espagnol</span><span class="sxs-lookup"><span data-stu-id="73ee9-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-163">Arabe</span><span class="sxs-lookup"><span data-stu-id="73ee9-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-165">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="73ee9-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-167">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="73ee9-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-169">Russe</span><span class="sxs-lookup"><span data-stu-id="73ee9-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-171">Tchèque</span><span class="sxs-lookup"><span data-stu-id="73ee9-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-173">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="73ee9-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-175">Grec</span><span class="sxs-lookup"><span data-stu-id="73ee9-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-177">Hébreu</span><span class="sxs-lookup"><span data-stu-id="73ee9-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-179">Hongrois</span><span class="sxs-lookup"><span data-stu-id="73ee9-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-181">Islandais</span><span class="sxs-lookup"><span data-stu-id="73ee9-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-183">Japonais</span><span class="sxs-lookup"><span data-stu-id="73ee9-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-185">Coréen</span><span class="sxs-lookup"><span data-stu-id="73ee9-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-187">Langues nordiques (Moteur de base de données Microsoft Jet version 1.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="73ee9-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-189">Norvégien et danois</span><span class="sxs-lookup"><span data-stu-id="73ee9-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-191">Polonais</span><span class="sxs-lookup"><span data-stu-id="73ee9-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-193">Slovène</span><span class="sxs-lookup"><span data-stu-id="73ee9-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-195">Espagnol traditionnel</span><span class="sxs-lookup"><span data-stu-id="73ee9-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-197">Suédois et finnois</span><span class="sxs-lookup"><span data-stu-id="73ee9-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-199">Thaï</span><span class="sxs-lookup"><span data-stu-id="73ee9-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-201">Turc</span><span class="sxs-lookup"><span data-stu-id="73ee9-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="73ee9-202">Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier s'il faut chiffrer ou déchiffrer la base de données pendant son compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="73ee9-203">Les constantes dbEncrypt dbDecrypt sont déconseillées et sont pas prises en charge dans les formats de fichier .ACCDB.</span><span class="sxs-lookup"><span data-stu-id="73ee9-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73ee9-204">Constante</span><span class="sxs-lookup"><span data-stu-id="73ee9-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="73ee9-205">Description</span><span class="sxs-lookup"><span data-stu-id="73ee9-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-207">Chiffre la base de données pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-209">Déchiffre la base de données pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="73ee9-210">Si vous ne spécifiez pas de constante de chiffrement ou que vous incluez à la fois **dbDecrypt** et **dbEncrypt**, DstName aura le même chiffrement que SrcName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-210">If you omit an encryption constant or if you include both dbDecrypt and dbEncrypt, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="73ee9-211">Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier la version du format de données de la base de données compactée.</span><span class="sxs-lookup"><span data-stu-id="73ee9-211">You can use one of the following constants in the  options argument to specify the version of the data format for the compacted database.</span></span> <span data-ttu-id="73ee9-212">Cette constante n'affecte que la version du format des données de NomDest mais non la version des objets définis par Microsoft Access, tels que les formulaires et les états.</span><span class="sxs-lookup"><span data-stu-id="73ee9-212">This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73ee9-213">Constante</span><span class="sxs-lookup"><span data-stu-id="73ee9-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="73ee9-214">Description</span><span class="sxs-lookup"><span data-stu-id="73ee9-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-216">Crée une base de données qui utilise le format de fichier de la version 1.0 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-218">Crée une base de données qui utilise le format de fichier de la version 1.1 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-220">Crée une base de données qui utilise le format de fichier de la version 2.0 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-222">Crée une base de données qui utilise le format de fichier de la version 3.0 (compatible avec la version 3.5) du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73ee9-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-224">Crée une base de données qui utilise le format de fichier de la version 4.0 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73ee9-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="73ee9-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="73ee9-226">Crée une base de données qui utilise le format fichier version 12.0 de moteur de base de données Microsoft Access pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="73ee9-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="73ee9-227">Vous pouvez spécifier un seul utilisateur par commande.</span><span class="sxs-lookup"><span data-stu-id="73ee9-227">You can specify only one version constant.</span></span> <span data-ttu-id="73ee9-228">Si vous l'omettez de renseigner une constante de la version, DstName aura la même version que SrcName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-228">If you omit a version constant,  DstName will have the same version as  SrcName.</span></span> <span data-ttu-id="73ee9-229">Vous ne pouvez compacter DstName que dans une version identique ou supérieure à celle de SrcName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-229">You can compact  DstName only to a version that is the same or later than that of  SrcName.</span></span>

<span data-ttu-id="73ee9-p110">À mesure que vous modifiez les données dans une base de données, le fichier de base de données peut se fragmenter et utiliser plus d'espace disque que nécessaire. Vous pouvez périodiquement utiliser la méthode **CompactDatabase** pour compacter la base de données et défragmenter le fichier de base de données. La base compactée est généralement plus petite et s'exécute plus rapidement. Il est également possible de modifier l'ordre de classement, le chiffrement et la version du format de données pendant la copie et le compactage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="73ee9-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="73ee9-234">Vous devez fermer SrcName avant de la compacter.</span><span class="sxs-lookup"><span data-stu-id="73ee9-234">You must close  SrcName before you compact it.</span></span> <span data-ttu-id="73ee9-235">Dans un environnement multi-utilisateur, les autres utilisateurs ne peuvent avoir SrcName ouverte pendant que vous la compactez.</span><span class="sxs-lookup"><span data-stu-id="73ee9-235">In a multiuser environment, other users can't have  SrcName open while you're compacting it.</span></span> <span data-ttu-id="73ee9-236">Si SrcName n'est pas fermée ou n'est pas accessible en mode exclusif, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="73ee9-236">If  SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="73ee9-237">Dans la mesure où **CompactDatabase** crée une copie de la base de données, vous devez avoir suffisamment d'espace disque pour la base de données d'origine et la base dupliquée.</span><span class="sxs-lookup"><span data-stu-id="73ee9-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="73ee9-238">L'opération de compactage échoue si il n'y a pas suffisamment d'espace disque.</span><span class="sxs-lookup"><span data-stu-id="73ee9-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="73ee9-239">La base de données dupliquée DstName ne doit pas nécessairement être sur le même disque que SrcName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-239">The  DstName duplicate database doesn't have to be on the same disk as  SrcName.</span></span> <span data-ttu-id="73ee9-240">Après le compactage réussi d'une base de données, vous pouvez supprimer le fichier SrcName et renommer le fichier DstName compacté avec le nom du fichier d'origine.</span><span class="sxs-lookup"><span data-stu-id="73ee9-240">After successfully compacting a database, you can delete the  SrcName file and rename the compacted  DstName file to the original file name.</span></span>

<span data-ttu-id="73ee9-241">La méthode **CompactDatabase** copie toutes les données et les options d'autorisation de sécurité de la base de données spécifiée par SrcName vers la base de données spécifiée par DstName.</span><span class="sxs-lookup"><span data-stu-id="73ee9-241">The CompactDatabase method copies all the data and the security permission settings from the database specified by  SrcName to the database specified by  DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="73ee9-242">Étant donné que la méthode**CompactDatabase** ne convertit pas les objets Microsoft Access, vous ne devez pas utiliser **CompactDatabase** pour convertir une base de données contenant ces objets.</span><span class="sxs-lookup"><span data-stu-id="73ee9-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="73ee9-243">Tableaux liés chiffrés</span><span class="sxs-lookup"><span data-stu-id="73ee9-243">Encrypted linked tables</span></span>

<span data-ttu-id="73ee9-244">Les mots de passe chiffrés dépendent du format de fichiers de la base de données que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="73ee9-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="73ee9-245">Si vous utilisez une base de données Access 2003 (.mdb) ou antérieure, vous aurez un mot de passe pour protéger la base de données et un mot de passe distinct pour chiffrer la base de données.</span><span class="sxs-lookup"><span data-stu-id="73ee9-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="73ee9-246">Pour les bases de données Access 2007 (.accdb) et version ultérieure (.mdb), la seule option consiste à chiffrer et protéger la base de données avec un mot de passe, comme l’option deux mots de passe distincts a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="73ee9-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="73ee9-247">Pour les bases de données Access 2007 (.accdb), le mot de passe est la clé de chiffrement</span><span class="sxs-lookup"><span data-stu-id="73ee9-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="73ee9-248">Vous pouvez utiliser l’exemple suivant du code VBA pour un bouton de commande :</span><span class="sxs-lookup"><span data-stu-id="73ee9-248">You can use the following example VBA code for a command button:</span></span>

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

<span data-ttu-id="73ee9-249">Exemple de code suivant montre comment utiliser CompactDatabase avec un mot de passe (clé de chiffrement) et créer un lien à un tableau dans cette base de données compactée.</span><span class="sxs-lookup"><span data-stu-id="73ee9-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="73ee9-250">Notez qu’un mot de passe doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="73ee9-250">Note that a password must be supplied.</span></span>

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
