---
title: Workspace. CreateDatabase, méthode (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6d271676ef91d29dca78ba9ee4b6142e055b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305865"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="1e754-102">Workspace. CreateDatabase, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e754-102">Workspace.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="1e754-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e754-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e754-104">Crée un objet **[Database](database-object-dao.md)**, enregistre la base de données sur le disque, et renvoie un objet **Database** ouvert (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="1e754-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e754-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e754-105">Syntax</span></span>

<span data-ttu-id="1e754-106">*expression* . CreateDatabase (***Name***, ***Connect***, ***option***)</span><span class="sxs-lookup"><span data-stu-id="1e754-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="1e754-107">*expression* Variable qui représente un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="1e754-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e754-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e754-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e754-109">Nom</span><span class="sxs-lookup"><span data-stu-id="1e754-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1e754-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="1e754-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1e754-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="1e754-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1e754-112">Description</span><span class="sxs-lookup"><span data-stu-id="1e754-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e754-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="1e754-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="1e754-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1e754-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1e754-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-116">String comportant jusqu’à 255 caractères formant le nom du fichier de base de données que vous créez.</span><span class="sxs-lookup"><span data-stu-id="1e754-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="1e754-117">Il peut s’agir du nom de fichier et du chemin d’accès complets.</span><span class="sxs-lookup"><span data-stu-id="1e754-117">It can be the full path and file name.</span></span> <span data-ttu-id="1e754-118">Si votre réseau le permet, vous pouvez également spécifier un chemin d'accès réseau, &quot; \\tel&quot;que server1\share1\dir1\db1.</span><span class="sxs-lookup"><span data-stu-id="1e754-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="1e754-119">Vous ne pouvez créer que des fichiers de base de données Microsoft Access avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1e754-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-120"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="1e754-120"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="1e754-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1e754-121">Required</span></span></p></td>
<td><p><span data-ttu-id="1e754-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1e754-p102">Expression de chaîne qui spécifie un ordre de classement pour la création de la base de données, tel qu'il est spécifié dans la section Remarques. Vous devez indiquer cet argument sans quoi une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1e754-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="1e754-125">Vous pouvez également créer un mot de passe pour le nouvel objet <strong>Database</strong> en concaténant la chaîne de mot &quot;de passe (&quot;en commençant par;p WD =) avec une constante dans l'argument <em>locale</em> , comme suit:</span><span class="sxs-lookup"><span data-stu-id="1e754-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="1e754-126">dbLangSpanish &amp; &quot;;p wd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="1e754-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="1e754-127">Si vous souhaitez utiliser la valeur par défaut de <em>locale</em> mais spécifier un mot de passe, entrez simplement une chaîne de mot de passe pour l'argument <em>locale</em> :</span><span class="sxs-lookup"><span data-stu-id="1e754-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="1e754-128">&quot;;p WD = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="1e754-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="1e754-p103">Utilisez des mots de passe forts qui associent des majuscules et des minuscules, des chiffres et des symboles. Les mots de passe faibles n'associent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : House27. Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</span><span class="sxs-lookup"><span data-stu-id="1e754-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-134"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="1e754-134"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="1e754-135">Facultatif</span><span class="sxs-lookup"><span data-stu-id="1e754-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="1e754-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-p104">Constante ou combinaison de constantes qui indique une ou plusieurs options, comme spécifié dans la section Remarques. Vous pouvez combiner des options en associant les constantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="1e754-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1e754-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e754-139">Remarks</span></span>

<span data-ttu-id="1e754-140">Vous pouvez utiliser l’une des constantes suivantes pour l’argument ParamètresRégionaux afin de spécifier la propriété [CollatingOrder](database-collatingorder-property-dao.md) du texte pour des comparaisons de chaînes.</span><span class="sxs-lookup"><span data-stu-id="1e754-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e754-141">Constante</span><span class="sxs-lookup"><span data-stu-id="1e754-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="1e754-142">Ordre de classement</span><span class="sxs-lookup"><span data-stu-id="1e754-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e754-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-144">Anglais, allemand, français, portugais, italien et espagnol</span><span class="sxs-lookup"><span data-stu-id="1e754-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-146">Arabic</span><span class="sxs-lookup"><span data-stu-id="1e754-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-148">Chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="1e754-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-150">Chinois traditionnel</span><span class="sxs-lookup"><span data-stu-id="1e754-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-152">Russe</span><span class="sxs-lookup"><span data-stu-id="1e754-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-154">Tchèque</span><span class="sxs-lookup"><span data-stu-id="1e754-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-156">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="1e754-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-158">Grec</span><span class="sxs-lookup"><span data-stu-id="1e754-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-160">Hébreu</span><span class="sxs-lookup"><span data-stu-id="1e754-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-162">Hongrois</span><span class="sxs-lookup"><span data-stu-id="1e754-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-164">Islandais</span><span class="sxs-lookup"><span data-stu-id="1e754-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-166">Japonais</span><span class="sxs-lookup"><span data-stu-id="1e754-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-168">Coréen</span><span class="sxs-lookup"><span data-stu-id="1e754-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-170">Langues nordiques (Moteur de base de données Microsoft Jet version 1.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="1e754-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-172">Norvégien et danois</span><span class="sxs-lookup"><span data-stu-id="1e754-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-174">Polonais</span><span class="sxs-lookup"><span data-stu-id="1e754-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-176">Slovène</span><span class="sxs-lookup"><span data-stu-id="1e754-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-178">Espagnol traditionnel</span><span class="sxs-lookup"><span data-stu-id="1e754-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-180">Suédois et finnois</span><span class="sxs-lookup"><span data-stu-id="1e754-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-182">Thaï</span><span class="sxs-lookup"><span data-stu-id="1e754-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-184">Turc</span><span class="sxs-lookup"><span data-stu-id="1e754-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1e754-185">Vous pouvez utiliser une ou plusieurs des constantes suivantes dans l'argument options pour indiquer la version du format de données et préciser s'il faut chiffrer ou non la base de données.</span><span class="sxs-lookup"><span data-stu-id="1e754-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e754-186">Constante</span><span class="sxs-lookup"><span data-stu-id="1e754-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="1e754-187">Description</span><span class="sxs-lookup"><span data-stu-id="1e754-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e754-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-189">Crée une base de données chiffrée.</span><span class="sxs-lookup"><span data-stu-id="1e754-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-191">Crée une base de données qui utilise le format de fichier de la version 1.0 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1e754-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-193">Crée une base de données qui utilise le format de fichier de la version 1.1 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1e754-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-195">Crée une base de données qui utilise le format de fichier de la version 2.0 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1e754-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-197">Crée une base de données qui utilise le format de fichier de la version 3.0 (compatible avec la version 3.5) du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1e754-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e754-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-199">Crée une base de données qui utilise le format de fichier de la version 4.0 du moteur de base de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="1e754-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e754-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="1e754-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="1e754-201">Crée une base de données qui utilise le format de fichier de la version 12.0 du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1e754-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1e754-202">Si vous omettez la constante de chiffrement, **CreateDatabase** crée une base de données non chiffrée.</span><span class="sxs-lookup"><span data-stu-id="1e754-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="1e754-p105">Utilisez la méthode **CreateDatabase** pour créer et ouvrir une nouvelle base de données vide, et renvoyer l'objet **Database**. Vous devez compléter sa structure et son contenu en utilisant des objets DAO supplémentaires. Si vous souhaitez réaliser une copie partielle ou totale d'une base de données existante, vous pouvez utiliser la méthode **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** pour effectuer une copie que vous pouvez personnaliser.</span><span class="sxs-lookup"><span data-stu-id="1e754-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="1e754-206">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e754-206">Example</span></span>

<span data-ttu-id="1e754-207">Cet exemple utilise **CreateDatabase** pour créer un objet **Database** chiffré.</span><span class="sxs-lookup"><span data-stu-id="1e754-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
