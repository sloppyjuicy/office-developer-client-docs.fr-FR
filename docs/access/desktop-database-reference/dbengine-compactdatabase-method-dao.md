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
ms.openlocfilehash: 1be6f910c8ab4aefed483c147ef88e8cecfa3a84
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470335"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="2da1a-102">DBEngine.CompactDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2da1a-102">DBEngine.CompactDatabase Method (DAO)</span></span>

<span data-ttu-id="2da1a-103">**S’applique à**: Access 2013 | Accès 2016</span><span class="sxs-lookup"><span data-stu-id="2da1a-103">**Applies to**: Access 2013 | Access 2016</span></span>

<span data-ttu-id="2da1a-104">Copie et compacte une base de données fermée et vous donne la possibilité de changer sa version, l’ordre de classement et le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2da1a-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="2da1a-105">(Espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2da1a-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="2da1a-106">Lors de l’utilisation de tables liées chiffrées pour action, mise à jour et les requêtes SQL [par exemple une instruction SQL UPDATE (« Mise à jour … » CurrentDb.Execute)], vous devez fournir la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2da1a-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="2da1a-107">En outre, les tables liées sont limités à 19 caractères pour la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2da1a-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="2da1a-108">Consultez la section **Encrypted des tables liées** à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2da1a-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da1a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2da1a-109">Syntax</span></span>

<span data-ttu-id="2da1a-110">*expression* . CompactDatabase (***NomSource***, ***NomDest***, ***ParamètresRégionauxDst***, ***Options***, ***le mot de passe***)</span><span class="sxs-lookup"><span data-stu-id="2da1a-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="2da1a-111">*expression* Expression qui renvoie un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="2da1a-111">*expression* An expression that returns a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2da1a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2da1a-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2da1a-113">Name</span><span class="sxs-lookup"><span data-stu-id="2da1a-113">Name</span></span></p></th>
<th><p><span data-ttu-id="2da1a-114">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="2da1a-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2da1a-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="2da1a-115">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2da1a-116">Description</span><span class="sxs-lookup"><span data-stu-id="2da1a-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-117">NomSource</span><span class="sxs-lookup"><span data-stu-id="2da1a-117">SrcName</span></span></p></td>
<td><p><span data-ttu-id="2da1a-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2da1a-118">Required</span></span></p></td>
<td><p><span data-ttu-id="2da1a-119"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-120">Identifie une base de données existante et fermée.</span><span class="sxs-lookup"><span data-stu-id="2da1a-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="2da1a-121">Il peut être un chemin d’accès complet et le nom de fichier, tel que &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="2da1a-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="2da1a-122">Si le nom de fichier doté d’une extension, vous devez le spécifier.</span><span class="sxs-lookup"><span data-stu-id="2da1a-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="2da1a-123">Si votre réseau prend en charge, vous pouvez également spécifier un chemin d’accès réseau, tel que &quot; \\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="2da1a-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-124">NomDest</span><span class="sxs-lookup"><span data-stu-id="2da1a-124">DstName</span></span></p></td>
<td><p><span data-ttu-id="2da1a-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2da1a-125">Required</span></span></p></td>
<td><p><span data-ttu-id="2da1a-126"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-127">nom de fichier (et chemin d’accès) de la base de données compactée que vous créez.</span><span class="sxs-lookup"><span data-stu-id="2da1a-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="2da1a-128">Vous pouvez également spécifier un chemin d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="2da1a-128">You can also specify a network path.</span></span> <span data-ttu-id="2da1a-129">Vous ne pouvez pas utiliser cet argument pour spécifier le même fichier de base de données que NomSource.</span><span class="sxs-lookup"><span data-stu-id="2da1a-129">You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-130">ParamètresRégionauxDst</span><span class="sxs-lookup"><span data-stu-id="2da1a-130">DstLocale</span></span></p></td>
<td><p><span data-ttu-id="2da1a-131">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2da1a-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="2da1a-132"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-133">Expression de chaîne qui indique un ordre de classement pour la création de NomDest, de la façon décrite dans la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="2da1a-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="2da1a-134">Si vous omettez cet argument, les paramètres régionaux de NomDest et NomSource seront identiques.</span><span class="sxs-lookup"><span data-stu-id="2da1a-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="2da1a-135">Vous pouvez également créer un mot de passe pour NomDest par la concaténation de la chaîne de mot de passe (commençant par &quot;; pwd =&quot;) avec une constante dans l’argument ParamètresRégionauxDst, comme suit : dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;.</span><span class="sxs-lookup"><span data-stu-id="2da1a-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="2da1a-136">Si vous souhaitez utiliser le même argument ParamètresRégionauxDst que NomSource (valeur par défaut), mais un nouveau mot de passe, entrez simplement une chaîne de mot de passe pour ParamètresRégionauxDst : &quot;; pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="2da1a-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-137">Options</span><span class="sxs-lookup"><span data-stu-id="2da1a-137">Options</span></span></p></td>
<td><p><span data-ttu-id="2da1a-138">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2da1a-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="2da1a-139"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-p105">Facultatif. Constante ou combinaison de constantes qui indique une ou plusieurs options, comme indiqué dans la section Remarques. Vous pouvez combiner des options en associant les constantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="2da1a-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-143">password</span><span class="sxs-lookup"><span data-stu-id="2da1a-143">password</span></span></p></td>
<td><p><span data-ttu-id="2da1a-144">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2da1a-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="2da1a-145"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-146">Expression chaîne contenant une clé de chiffrement, si la base de données est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="2da1a-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="2da1a-147">La chaîne &quot;; pwd =&quot; doivent précéder le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2da1a-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="2da1a-148">Si vous incluez un paramètre de mot de passe dans ParamètresRégionauxDst, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="2da1a-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="2da1a-149">Cela est le paramètre désapprouvé et n’est pas pris en charge. Format de fichier ACCDB.</span><span class="sxs-lookup"><span data-stu-id="2da1a-149">This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="2da1a-150">Pour chiffrer une. Fichier ACCDB, utilisez le « pwd = « chaîne d’option.</span><span class="sxs-lookup"><span data-stu-id="2da1a-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="2da1a-151">[!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles.</span><span class="sxs-lookup"><span data-stu-id="2da1a-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="2da1a-152">Les mots de passe faibles ne regroupent pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="2da1a-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="2da1a-153">Mot de passe fort : Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="2da1a-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="2da1a-154">Mot de passe faible : Maison27.</span><span class="sxs-lookup"><span data-stu-id="2da1a-154">Weak password: House27.</span></span> <span data-ttu-id="2da1a-155">Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="2da1a-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2da1a-156">Remarques</span><span class="sxs-lookup"><span data-stu-id="2da1a-156">Remarks</span></span>

<span data-ttu-id="2da1a-157">Vous pouvez utiliser l'une des constantes suivantes pour l'argument ParamètresRégionauxDst afin de définir la propriété **CollatingOrder** pour des comparaisons de chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="2da1a-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2da1a-158">Constante</span><span class="sxs-lookup"><span data-stu-id="2da1a-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="2da1a-159">Ordre de classement</span><span class="sxs-lookup"><span data-stu-id="2da1a-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-161">Anglais, allemand, français, portugais, italien et espagnol</span><span class="sxs-lookup"><span data-stu-id="2da1a-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-163">Arabe</span><span class="sxs-lookup"><span data-stu-id="2da1a-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-165">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="2da1a-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-167">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="2da1a-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-169">Russe</span><span class="sxs-lookup"><span data-stu-id="2da1a-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-171">Tchèque</span><span class="sxs-lookup"><span data-stu-id="2da1a-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-173">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="2da1a-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-175">Grec</span><span class="sxs-lookup"><span data-stu-id="2da1a-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-177">Hébreu</span><span class="sxs-lookup"><span data-stu-id="2da1a-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-179">Hongrois</span><span class="sxs-lookup"><span data-stu-id="2da1a-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-181">Islandais</span><span class="sxs-lookup"><span data-stu-id="2da1a-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-183">Japonais</span><span class="sxs-lookup"><span data-stu-id="2da1a-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-185">Coréen</span><span class="sxs-lookup"><span data-stu-id="2da1a-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-187">Langues nordiques (Moteur de base de données Microsoft Jet version 1.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="2da1a-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-189">Norvégien et danois</span><span class="sxs-lookup"><span data-stu-id="2da1a-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-191">Polonais</span><span class="sxs-lookup"><span data-stu-id="2da1a-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-193">Slovène</span><span class="sxs-lookup"><span data-stu-id="2da1a-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-195">Espagnol traditionnel</span><span class="sxs-lookup"><span data-stu-id="2da1a-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-197">Suédois et finnois</span><span class="sxs-lookup"><span data-stu-id="2da1a-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-199">Thaï</span><span class="sxs-lookup"><span data-stu-id="2da1a-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-201">Turc</span><span class="sxs-lookup"><span data-stu-id="2da1a-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="2da1a-202">Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier s'il faut chiffrer ou déchiffrer la base de données pendant son compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="2da1a-203">Les constantes dbEncrypt dbDecrypt déconseillée et sont pas pris en charge. Formats de fichier ACCDB.</span><span class="sxs-lookup"><span data-stu-id="2da1a-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2da1a-204">Constant</span><span class="sxs-lookup"><span data-stu-id="2da1a-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="2da1a-205">Description</span><span class="sxs-lookup"><span data-stu-id="2da1a-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-207">Chiffre la base de données pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-209">Déchiffre la base de données pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="2da1a-210">Si vous omettez la constante de chiffrement ou que vous incluez à la fois **dbDecrypt** et **dbEncrypt**, NomDest aura le même chiffrement que NomSource.</span><span class="sxs-lookup"><span data-stu-id="2da1a-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="2da1a-p108">Vous pouvez utiliser l'une des constantes suivantes dans l'argument options pour spécifier la version du format de données de la base de données compactée. Cette constante n'affecte que la version du format des données de NomDest mais non la version des objets définis par Microsoft Access, tels que les formulaires et les états.</span><span class="sxs-lookup"><span data-stu-id="2da1a-p108">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database. This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2da1a-213">Constant</span><span class="sxs-lookup"><span data-stu-id="2da1a-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="2da1a-214">Description</span><span class="sxs-lookup"><span data-stu-id="2da1a-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-216">Crée une base de données qui utilise le format de fichier de la version 1.0 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-218">Crée une base de données qui utilise le format de fichier de la version 1.1 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-220">Crée une base de données qui utilise le format de fichier de la version 2.0 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-222">Crée une base de données qui utilise le format de fichier de la version 3.0 (compatible avec la version 3.5) du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2da1a-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-224">Crée une base de données qui utilise le format de fichier de la version 4.0 du moteur de base de données Microsoft Jet pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2da1a-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="2da1a-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="2da1a-226">Crée une base de données qui utilise le format de fichier de la version 12.0 du moteur de base de données Microsoft Access pendant le compactage.</span><span class="sxs-lookup"><span data-stu-id="2da1a-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="2da1a-227">Vous ne pouvez spécifier qu'une seule constante de version.</span><span class="sxs-lookup"><span data-stu-id="2da1a-227">You can specify only one version constant.</span></span> <span data-ttu-id="2da1a-228">Si vous omettez, NomDest aura la même version que NomSource.</span><span class="sxs-lookup"><span data-stu-id="2da1a-228">If you omit a version constant, DstName will have the same version as SrcName.</span></span> <span data-ttu-id="2da1a-229">Vous pouvez compacter NomDest que dans une version est la même ou version ultérieure à celle de NomSource.</span><span class="sxs-lookup"><span data-stu-id="2da1a-229">You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="2da1a-p110">À mesure que vous modifiez les données dans une base de données, le fichier de base de données peut se fragmenter et utiliser plus d'espace disque que nécessaire. Vous pouvez périodiquement utiliser la méthode **CompactDatabase** pour compacter la base de données et défragmenter le fichier de base de données. La base compactée est généralement plus petite et s'exécute plus rapidement. Il est également possible de modifier l'ordre de classement, le chiffrement et la version du format de données pendant la copie et le compactage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2da1a-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="2da1a-234">Vous devez fermer NomSource avant de la compacter.</span><span class="sxs-lookup"><span data-stu-id="2da1a-234">You must close SrcName before you compact it.</span></span> <span data-ttu-id="2da1a-235">Dans un environnement multi-utilisateurs, les autres utilisateurs ne peuvent pas avoir NomSource ouverte pendant que vous la compactez.</span><span class="sxs-lookup"><span data-stu-id="2da1a-235">In a multiuser environment, other users can't have SrcName open while you're compacting it.</span></span> <span data-ttu-id="2da1a-236">Si NomSource n’est pas fermée ou n’est pas disponible pour une utilisation exclusive, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="2da1a-236">If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="2da1a-237">Dans la mesure où **CompactDatabase** crée une copie de la base de données, vous devez avoir suffisamment d'espace disque pour la base de données d'origine et la base dupliquée.</span><span class="sxs-lookup"><span data-stu-id="2da1a-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="2da1a-238">L'opération de compactage échoue si il n'y a pas suffisamment d'espace disque.</span><span class="sxs-lookup"><span data-stu-id="2da1a-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="2da1a-239">La base de données dupliquée NomDest ne doit se trouver sur le même disque que NomSource.</span><span class="sxs-lookup"><span data-stu-id="2da1a-239">The DstName duplicate database doesn't have to be on the same disk as SrcName.</span></span> <span data-ttu-id="2da1a-240">Après le compactage réussi d’une base de données, vous pouvez supprimer le fichier NomSource et renommer le fichier NomDest compacté au nom du fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="2da1a-240">After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="2da1a-241">La méthode **CompactDatabase** copie toutes les données et les paramètres d’autorisation de sécurité à partir de la base de données spécifiée par NomSource vers la base de données spécifiée par NomDest.</span><span class="sxs-lookup"><span data-stu-id="2da1a-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="2da1a-242">[!REMARQUE] Comme la méthode **CompactDatabase** ne convertit pas les objets Microsoft Access, vous ne devez pas utiliser **CompactDatabase** pour convertir une base de données contenant de tels objets.</span><span class="sxs-lookup"><span data-stu-id="2da1a-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="2da1a-243">Tables liées chiffrés</span><span class="sxs-lookup"><span data-stu-id="2da1a-243">Encrypted linked tables</span></span>

<span data-ttu-id="2da1a-244">Les mots de passe chiffrés dépendent de la base de données que vous utilisez le format de fichier.</span><span class="sxs-lookup"><span data-stu-id="2da1a-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="2da1a-245">Si vous utilisez un Access 2003 (.mdb) ou une base de données antérieure, vous aurez un mot de passe pour protéger la base de données et un mot de passe distinct pour crypter la base de données.</span><span class="sxs-lookup"><span data-stu-id="2da1a-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="2da1a-246">Pour Access 2007 (.accdb) et version ultérieure bases de données (.mdb), la seule option consiste à chiffrer et protéger la base de données avec un mot de passe, comme l’option pour que les deux mots de passe a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="2da1a-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="2da1a-247">Pour les bases de données Access 2007 (.accdb), le mot de passe est la clé de chiffrement</span><span class="sxs-lookup"><span data-stu-id="2da1a-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="2da1a-248">Vous pouvez utiliser l’exemple de code VBA suivant pour un bouton de commande :</span><span class="sxs-lookup"><span data-stu-id="2da1a-248">You can use the following example VBA code for a command button:</span></span>

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

<span data-ttu-id="2da1a-249">L’exemple de code suivant montre comment utiliser CompactDatabase avec un mot de passe (clé de chiffrement), puis lier à une table dans cette base de données compactée.</span><span class="sxs-lookup"><span data-stu-id="2da1a-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="2da1a-250">Notez que le mot de passe doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="2da1a-250">Note that a password must be supplied.</span></span>

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
