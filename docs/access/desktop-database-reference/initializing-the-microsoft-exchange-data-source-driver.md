---
title: Initialisation du pilote de source de données Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c1ba74f754ef0c998a14f7421914bd4bcd7c9cf9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870197"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="035f5-102">Initialisation du pilote de source de données Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="035f5-102">Initializing the Microsoft Exchange Data Source Driver</span></span>

<span data-ttu-id="035f5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="035f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="035f5-p101">Lorsque vous installez le pilote de source de données Microsoft® Exchange, le programme d'installation écrit un ensemble de valeurs par défaut dans les sous-clé Engines et ISAM Formats du registre Microsoft Windows®. Vous ne devez pas modifier directement ces paramètres. Utilisez le programme d'installation de votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l'initialisation et les paramètres de format ISAM pour le pilote de source de données Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="035f5-p101">When you install the Microsoft® Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="035f5-107">Paramètres d'initialisation de source de données Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="035f5-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="035f5-108">Le **Access Connectivity Engine\\moteurs\\Exchange** dossier contient des paramètres d’initialisation du pilote Aceexch.dll, utilisé pour l’accès externe aux dossiers Microsoft Outlook et Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="035f5-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="035f5-109">L'unique entrée dans ce dossier est la suivante :</span><span class="sxs-lookup"><span data-stu-id="035f5-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="035f5-110">Le moteur de base de données Microsoft Exchange utilise ce paramètre pour indiquer l'emplacement du pilote Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="035f5-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="035f5-111">Le chemin d'accès complet est déterminé au moment de l'installation.</span><span class="sxs-lookup"><span data-stu-id="035f5-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="035f5-112">Les valeurs sont de type de Registre\_SZ.</span><span class="sxs-lookup"><span data-stu-id="035f5-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="035f5-p104">Le format ISAM du client Outlook et le format ISAM du client Exchange donnent des résultats similaires. La seule différence est que ces deux clients utilisent des noms différents pour les mêmes colonnes. Les deux formats ISAM ont été créés afin que le moteur de base de données Microsoft Access puisse retourner les noms de colonnes dans un style particulier souhaité par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="035f5-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="035f5-116">Formats ISAM du client Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="035f5-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="035f5-117">Le **Access Connectivity Engine\\Formats ISAM\\Outlook 9.0** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="035f5-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="035f5-118">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="035f5-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="035f5-119">Type</span><span class="sxs-lookup"><span data-stu-id="035f5-119">Type</span></span></p></th>
<th><p><span data-ttu-id="035f5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="035f5-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="035f5-121">Engine</span><span class="sxs-lookup"><span data-stu-id="035f5-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="035f5-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="035f5-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="035f5-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="035f5-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="035f5-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="035f5-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="035f5-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="035f5-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="035f5-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="035f5-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="035f5-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="035f5-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-129">01</span><span class="sxs-lookup"><span data-stu-id="035f5-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="035f5-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="035f5-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-132">00</span><span class="sxs-lookup"><span data-stu-id="035f5-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="035f5-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="035f5-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="035f5-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="035f5-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="035f5-135">3</span><span class="sxs-lookup"><span data-stu-id="035f5-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="035f5-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="035f5-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-138">00</span><span class="sxs-lookup"><span data-stu-id="035f5-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="035f5-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="035f5-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="035f5-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-141">00</span><span class="sxs-lookup"><span data-stu-id="035f5-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="035f5-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="035f5-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-144">01</span><span class="sxs-lookup"><span data-stu-id="035f5-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="035f5-145">Si vous modifiez les paramètres du Registre Windows, vous devez quitter puis redémarrer le moteur de base de données pour que les nouveaux paramètres soient appliqués.</span><span class="sxs-lookup"><span data-stu-id="035f5-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="035f5-146">Formats ISAM du client Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="035f5-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="035f5-147">Le **Access Connectivity Engine\\Formats ISAM\\Exchange 4.0** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="035f5-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="035f5-148">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="035f5-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="035f5-149">Type</span><span class="sxs-lookup"><span data-stu-id="035f5-149">Type</span></span></p></th>
<th><p><span data-ttu-id="035f5-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="035f5-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="035f5-151">Engine</span><span class="sxs-lookup"><span data-stu-id="035f5-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="035f5-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="035f5-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="035f5-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="035f5-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="035f5-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="035f5-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="035f5-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="035f5-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="035f5-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="035f5-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="035f5-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="035f5-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-159">01</span><span class="sxs-lookup"><span data-stu-id="035f5-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="035f5-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="035f5-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-162">00</span><span class="sxs-lookup"><span data-stu-id="035f5-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="035f5-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="035f5-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="035f5-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="035f5-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="035f5-165">3</span><span class="sxs-lookup"><span data-stu-id="035f5-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="035f5-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="035f5-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-168">00</span><span class="sxs-lookup"><span data-stu-id="035f5-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="035f5-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="035f5-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="035f5-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-171">00</span><span class="sxs-lookup"><span data-stu-id="035f5-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="035f5-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="035f5-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="035f5-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="035f5-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="035f5-174">01</span><span class="sxs-lookup"><span data-stu-id="035f5-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="035f5-175">Si vous modifiez les paramètres du Registre Windows, vous devez quitter puis redémarrer le moteur de base de données afin que les nouveaux paramètres prennent effet.</span><span class="sxs-lookup"><span data-stu-id="035f5-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="035f5-176">Personnalisation du fichier schema.ini pour les données Outlook et Exchange</span><span class="sxs-lookup"><span data-stu-id="035f5-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="035f5-p105">Le fichier Schema.ini est utilisé par le format ISAM Outlook et le format ISAM Exchange pratiquement de la même manière que par le format ISAM texte. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en fome des données, noms des colonnes auxquelles accéder.</span><span class="sxs-lookup"><span data-stu-id="035f5-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="035f5-p106">Il n'est pas nécessaire de modifier le fichier Schema.ini pour pouvoir lire, importer ou exporter des données pour Outlook et Exchange. De nombreux paramètres du fichier Schema.ini pour Outlook et Exchange sont spécifiques à des balises internes requises par MAPI. Vous ne devez pas tenter de modifier les valeurs de ces balises.</span><span class="sxs-lookup"><span data-stu-id="035f5-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

