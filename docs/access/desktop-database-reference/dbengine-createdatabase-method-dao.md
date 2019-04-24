---
title: DBEngine. CreateDatabase, méthode (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 13e41dcd182f720b3611108311db6cd56fb4847e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294364"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="6da1e-102">DBEngine. CreateDatabase, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6da1e-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="6da1e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6da1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6da1e-104">Crée un objet **[Database](database-object-dao.md)**, enregistre la base de données sur le disque, et renvoie un objet **Database** ouvert (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="6da1e-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6da1e-105">.</span><span class="sxs-lookup"><span data-stu-id="6da1e-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="6da1e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6da1e-106">Syntax</span></span>

<span data-ttu-id="6da1e-107">*expression* . CreateDatabase (***nom***, ***paramètres régionaux***, ***option***)</span><span class="sxs-lookup"><span data-stu-id="6da1e-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="6da1e-108">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="6da1e-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6da1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6da1e-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6da1e-110">Nom</span><span class="sxs-lookup"><span data-stu-id="6da1e-110">Name</span></span></p></th>
<th><p><span data-ttu-id="6da1e-111">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="6da1e-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6da1e-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="6da1e-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="6da1e-113">Description</span><span class="sxs-lookup"><span data-stu-id="6da1e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="6da1e-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="6da1e-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6da1e-115">Required</span></span></p></td>
<td><p><span data-ttu-id="6da1e-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-117">String comportant jusqu’à 255 caractères formant le nom du fichier de base de données que vous créez.</span><span class="sxs-lookup"><span data-stu-id="6da1e-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="6da1e-118">Il peut s’agir du nom de fichier et du chemin d’accès complets.</span><span class="sxs-lookup"><span data-stu-id="6da1e-118">It can be the full path and file name.</span></span> <span data-ttu-id="6da1e-119">Si votre réseau le permet, vous pouvez également spécifier un chemin d'accès réseau, &quot; \\tel&quot;que server1\share1\dir1\db1.</span><span class="sxs-lookup"><span data-stu-id="6da1e-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="6da1e-120">Vous ne pouvez créer que des fichiers de base de données Microsoft Access avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6da1e-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-121"><em>Paramètres régionaux</em></span><span class="sxs-lookup"><span data-stu-id="6da1e-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="6da1e-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6da1e-122">Required</span></span></p></td>
<td><p><span data-ttu-id="6da1e-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="6da1e-p103">Expression de chaîne qui spécifie un ordre de classement pour la création de la base de données, tel qu'il est spécifié dans la section Remarques. Vous devez indiquer cet argument sans quoi une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="6da1e-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="6da1e-126">Vous pouvez également créer un mot de passe pour le nouvel objet <strong>Database</strong> en concaténant la chaîne de mot &quot;de passe (&quot; en commençant par;p WD =) avec une constante dans l'argument <em>locale</em> , comme suit:</span><span class="sxs-lookup"><span data-stu-id="6da1e-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="6da1e-127">dbLangSpanish &amp; &quot;;p wd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="6da1e-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="6da1e-128">Si vous souhaitez utiliser la valeur par défaut de <em>locale</em> mais spécifier un mot de passe, entrez simplement une chaîne de mot de passe pour l'argument <em>locale</em> :</span><span class="sxs-lookup"><span data-stu-id="6da1e-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="6da1e-129">&quot;;p WD = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="6da1e-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="6da1e-p104">Utilisez des mots de passe forts qui associent des majuscules et des minuscules, des chiffres et des symboles. Les mots de passe faibles n'associent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : House27. Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</span><span class="sxs-lookup"><span data-stu-id="6da1e-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-135"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="6da1e-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="6da1e-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="6da1e-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="6da1e-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-p105">Constante ou combinaison de constantes qui indique une ou plusieurs options, comme spécifié dans la section Remarques. Vous pouvez combiner des options en associant les constantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="6da1e-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6da1e-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="6da1e-140">Remarks</span></span>

<span data-ttu-id="6da1e-141">Vous pouvez utiliser l'une des constantes suivantes pour l'argument paramètres régionaux afin de spécifier la propriété **[CollatingOrder](database-collatingorder-property-dao.md)** de texte pour les comparaisons de chaînes.</span><span class="sxs-lookup"><span data-stu-id="6da1e-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6da1e-142">Constante</span><span class="sxs-lookup"><span data-stu-id="6da1e-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="6da1e-143">Ordre de classement</span><span class="sxs-lookup"><span data-stu-id="6da1e-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-145">Anglais, allemand, français, portugais, italien et espagnol</span><span class="sxs-lookup"><span data-stu-id="6da1e-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-147">Arabic</span><span class="sxs-lookup"><span data-stu-id="6da1e-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-149">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="6da1e-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-151">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="6da1e-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-153">Russe</span><span class="sxs-lookup"><span data-stu-id="6da1e-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-155">Tchèque</span><span class="sxs-lookup"><span data-stu-id="6da1e-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-157">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="6da1e-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-159">Grec</span><span class="sxs-lookup"><span data-stu-id="6da1e-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-161">Hébreu</span><span class="sxs-lookup"><span data-stu-id="6da1e-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-163">Hongrois</span><span class="sxs-lookup"><span data-stu-id="6da1e-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-165">Islandais</span><span class="sxs-lookup"><span data-stu-id="6da1e-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-167">Japonais</span><span class="sxs-lookup"><span data-stu-id="6da1e-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-169">Coréen</span><span class="sxs-lookup"><span data-stu-id="6da1e-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-171">Langues nordiques (Moteur de base de données Microsoft Jet version 1.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="6da1e-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-173">Norvégien et danois</span><span class="sxs-lookup"><span data-stu-id="6da1e-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-175">Polonais</span><span class="sxs-lookup"><span data-stu-id="6da1e-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-177">Slovène</span><span class="sxs-lookup"><span data-stu-id="6da1e-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-179">Espagnol traditionnel</span><span class="sxs-lookup"><span data-stu-id="6da1e-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-181">Suédois et finnois</span><span class="sxs-lookup"><span data-stu-id="6da1e-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-183">Thaï</span><span class="sxs-lookup"><span data-stu-id="6da1e-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-185">Turc</span><span class="sxs-lookup"><span data-stu-id="6da1e-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6da1e-186">Vous pouvez utiliser une ou plusieurs des constantes suivantes dans l'argument options pour indiquer la version du format de données et préciser s'il faut chiffrer ou non la base de données.</span><span class="sxs-lookup"><span data-stu-id="6da1e-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6da1e-187">Constante</span><span class="sxs-lookup"><span data-stu-id="6da1e-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="6da1e-188">Description</span><span class="sxs-lookup"><span data-stu-id="6da1e-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-190">Crée une base de données chiffrée.</span><span class="sxs-lookup"><span data-stu-id="6da1e-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-192">Crée une base de données qui utilise le format de fichier de la version 1.0 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="6da1e-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-194">Crée une base de données qui utilise le format de fichier de la version 1.1 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="6da1e-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-196">Crée une base de données qui utilise le format de fichier de la version 2.0 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="6da1e-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-198">Crée une base de données qui utilise le format de fichier de la version 3.0 (compatible avec la version 3.5) du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="6da1e-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6da1e-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-200">Crée une base de données qui utilise le format de fichier de la version 4.0 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="6da1e-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6da1e-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="6da1e-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="6da1e-202">Crée une base de données qui utilise le format de fichier de la version 12.0 du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6da1e-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6da1e-203">Si vous omettez la constante de chiffrement, **CreateDatabase** crée une base de données non chiffrée.</span><span class="sxs-lookup"><span data-stu-id="6da1e-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="6da1e-p106">Utilisez la méthode **CreateDatabase** pour créer et ouvrir une nouvelle base de données vide et renvoyer l'objet **Database**. Vous devez compléter sa structure et son contenu en utilisant des objets DAO supplémentaires. Si vous souhaitez réaliser une copie partielle ou complète d'une base de données existante, vous pouvez faire appel à la méthode **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** afin de créer une copie personnalisable.</span><span class="sxs-lookup"><span data-stu-id="6da1e-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

