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
ms.openlocfilehash: f711e9814e32742c89c37ae3357111143ca18b6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469178"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="1ea0b-102">Initialisation du pilote de source de données Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea0b-102">Initializing the Microsoft Exchange Data Source Driver</span></span>

<span data-ttu-id="1ea0b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ea0b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1ea0b-p101">Lorsque vous installez le pilote de source de données Microsoft® Exchange, le programme d'installation écrit un ensemble de valeurs par défaut dans les sous-clé Engines et ISAM Formats du registre Microsoft Windows®. Vous ne devez pas modifier directement ces paramètres. Utilisez le programme d'installation de votre application pour ajouter, supprimer ou modifier ces paramètres. Les sections suivantes décrivent l'initialisation et les paramètres de format ISAM pour le pilote de source de données Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-p101">When you install the Microsoft® Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="1ea0b-107">Paramètres d'initialisation de source de données Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea0b-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="1ea0b-108">Le **Access Connectivity Engine\\moteurs\\Exchange** dossier contient des paramètres d’initialisation du pilote Aceexch.dll, utilisé pour l’accès externe aux dossiers Microsoft Outlook et Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="1ea0b-109">L'unique entrée dans ce dossier est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1ea0b-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="1ea0b-110">Le moteur de base de données Microsoft Exchange utilise ce paramètre pour indiquer l'emplacement du pilote Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="1ea0b-111">Le chemin d'accès complet est déterminé au moment de l'installation.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="1ea0b-112">Les valeurs sont de type de Registre\_SZ.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="1ea0b-p104">Le format ISAM du client Outlook et le format ISAM du client Exchange donnent des résultats similaires. La seule différence est que ces deux clients utilisent des noms différents pour les mêmes colonnes. Les deux formats ISAM ont été créés afin que le moteur de base de données Microsoft Access puisse retourner les noms de colonnes dans un style particulier souhaité par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="1ea0b-116">Formats ISAM du client Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="1ea0b-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="1ea0b-117">Le **Access Connectivity Engine\\Formats ISAM\\Outlook 9.0** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea0b-118">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="1ea0b-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="1ea0b-119">Type</span><span class="sxs-lookup"><span data-stu-id="1ea0b-119">Type</span></span></p></th>
<th><p><span data-ttu-id="1ea0b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ea0b-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-121">Engine</span><span class="sxs-lookup"><span data-stu-id="1ea0b-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1ea0b-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea0b-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="1ea0b-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1ea0b-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="1ea0b-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="1ea0b-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-129">01</span><span class="sxs-lookup"><span data-stu-id="1ea0b-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="1ea0b-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-132">00</span><span class="sxs-lookup"><span data-stu-id="1ea0b-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="1ea0b-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1ea0b-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-135">3</span><span class="sxs-lookup"><span data-stu-id="1ea0b-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="1ea0b-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-138">00</span><span class="sxs-lookup"><span data-stu-id="1ea0b-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="1ea0b-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-141">00</span><span class="sxs-lookup"><span data-stu-id="1ea0b-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="1ea0b-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-144">01</span><span class="sxs-lookup"><span data-stu-id="1ea0b-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="1ea0b-145">Si vous modifiez les paramètres du Registre Windows, vous devez quitter puis redémarrer le moteur de base de données pour que les nouveaux paramètres soient appliqués.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="1ea0b-146">Formats ISAM du client Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea0b-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="1ea0b-147">Le **Access Connectivity Engine\\Formats ISAM\\Exchange 4.0** dossier contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ea0b-148">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="1ea0b-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="1ea0b-149">Type</span><span class="sxs-lookup"><span data-stu-id="1ea0b-149">Type</span></span></p></th>
<th><p><span data-ttu-id="1ea0b-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ea0b-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-151">Engine</span><span class="sxs-lookup"><span data-stu-id="1ea0b-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1ea0b-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea0b-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="1ea0b-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1ea0b-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="1ea0b-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="1ea0b-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-159">01</span><span class="sxs-lookup"><span data-stu-id="1ea0b-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="1ea0b-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-162">00</span><span class="sxs-lookup"><span data-stu-id="1ea0b-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="1ea0b-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1ea0b-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-165">3</span><span class="sxs-lookup"><span data-stu-id="1ea0b-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="1ea0b-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-168">00</span><span class="sxs-lookup"><span data-stu-id="1ea0b-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ea0b-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="1ea0b-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-171">00</span><span class="sxs-lookup"><span data-stu-id="1ea0b-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ea0b-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="1ea0b-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea0b-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1ea0b-174">01</span><span class="sxs-lookup"><span data-stu-id="1ea0b-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="1ea0b-175">Si vous modifiez les paramètres du Registre Windows, vous devez quitter puis redémarrer le moteur de base de données afin que les nouveaux paramètres prennent effet.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="1ea0b-176">Personnalisation du fichier schema.ini pour les données Outlook et Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea0b-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="1ea0b-p105">Le fichier Schema.ini est utilisé par le format ISAM Outlook et le format ISAM Exchange pratiquement de la même manière que par le format ISAM texte. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en fome des données, noms des colonnes auxquelles accéder.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="1ea0b-p106">Il n'est pas nécessaire de modifier le fichier Schema.ini pour pouvoir lire, importer ou exporter des données pour Outlook et Exchange. De nombreux paramètres du fichier Schema.ini pour Outlook et Exchange sont spécifiques à des balises internes requises par MAPI. Vous ne devez pas tenter de modifier les valeurs de ces balises.</span><span class="sxs-lookup"><span data-stu-id="1ea0b-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

