---
title: Initialisation du pilote de source de données Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291406"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="0ac70-102">Initialisation du pilote de source de données Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac70-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="0ac70-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ac70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ac70-104">Lorsque vous installez le pilote de source de données Microsoft Exchange, le programme d’installation écrit un ensemble de valeurs par défaut dans le Registre Microsoft Windows dans les sous-clés Engines et ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="0ac70-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="0ac70-105">Vous ne devez pas modifier ces paramètres directement ; utilisez le programme d’installation de votre application pour ajouter, supprimer ou modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="0ac70-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="0ac70-106">Les sections suivantes décrivent l’initialisation et les paramètres de format ISAM pour le pilote de source de données Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ac70-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="0ac70-107">Paramètres d’initialisation de la source de données Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac70-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="0ac70-108">Le **dossier Exchange access Connectivity \\ Engines \\** inclut les paramètres d’initialisation du pilote Aceexch.dll, utilisé pour l’accès externe aux dossiers Microsoft Outlook et Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ac70-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="0ac70-109">L'unique entrée dans ce dossier est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0ac70-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="0ac70-110">Le moteur de base de données Microsoft Exchange utilise ce paramètre pour indiquer l'emplacement du pilote Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="0ac70-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="0ac70-111">Le chemin d'accès complet est déterminé au moment de l'installation.</span><span class="sxs-lookup"><span data-stu-id="0ac70-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="0ac70-112">Les valeurs sont de type REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="0ac70-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="0ac70-p104">Le format ISAM du client Outlook et le format ISAM du client Exchange donnent des résultats similaires. La seule différence est que ces deux clients utilisent des noms différents pour les mêmes colonnes. Les deux formats ISAM ont été créés afin que le moteur de base de données Microsoft Access puisse retourner les noms de colonnes dans un style particulier souhaité par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ac70-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="0ac70-116">Formats ISAM du client Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="0ac70-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="0ac70-117">Le **dossier \\ Outlook \\ 9.0 formats ISAM** du moteur de connectivité Access contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ac70-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ac70-118">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="0ac70-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="0ac70-119">Type</span><span class="sxs-lookup"><span data-stu-id="0ac70-119">Type</span></span></p></th>
<th><p><span data-ttu-id="0ac70-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ac70-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-121">Moteur</span><span class="sxs-lookup"><span data-stu-id="0ac70-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="0ac70-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0ac70-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0ac70-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac70-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="0ac70-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="0ac70-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0ac70-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0ac70-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="0ac70-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="0ac70-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="0ac70-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-129">01</span><span class="sxs-lookup"><span data-stu-id="0ac70-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="0ac70-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="0ac70-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-132">00</span><span class="sxs-lookup"><span data-stu-id="0ac70-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="0ac70-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="0ac70-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0ac70-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="0ac70-135">3 </span><span class="sxs-lookup"><span data-stu-id="0ac70-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="0ac70-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="0ac70-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-138">00</span><span class="sxs-lookup"><span data-stu-id="0ac70-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="0ac70-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="0ac70-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-141">00</span><span class="sxs-lookup"><span data-stu-id="0ac70-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="0ac70-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="0ac70-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-144">01</span><span class="sxs-lookup"><span data-stu-id="0ac70-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="0ac70-145">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="0ac70-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="0ac70-146">Formats ISAM du client Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac70-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="0ac70-147">Le **dossier Exchange \\ \\ 4.0 formats ISAM** du moteur de connectivité Access contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ac70-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ac70-148">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="0ac70-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="0ac70-149">Type</span><span class="sxs-lookup"><span data-stu-id="0ac70-149">Type</span></span></p></th>
<th><p><span data-ttu-id="0ac70-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ac70-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-151">Moteur</span><span class="sxs-lookup"><span data-stu-id="0ac70-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="0ac70-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0ac70-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0ac70-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac70-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="0ac70-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="0ac70-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0ac70-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0ac70-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="0ac70-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="0ac70-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="0ac70-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-159">01</span><span class="sxs-lookup"><span data-stu-id="0ac70-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="0ac70-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="0ac70-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-162">00</span><span class="sxs-lookup"><span data-stu-id="0ac70-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="0ac70-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="0ac70-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0ac70-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="0ac70-165">3 </span><span class="sxs-lookup"><span data-stu-id="0ac70-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="0ac70-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="0ac70-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-168">00</span><span class="sxs-lookup"><span data-stu-id="0ac70-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ac70-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="0ac70-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="0ac70-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-171">00</span><span class="sxs-lookup"><span data-stu-id="0ac70-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ac70-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="0ac70-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="0ac70-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ac70-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0ac70-174">01</span><span class="sxs-lookup"><span data-stu-id="0ac70-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="0ac70-175">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="0ac70-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="0ac70-176">Personnalisation du fichier Schema.ini pour les données Outlook et Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac70-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="0ac70-p105">Le fichier Schema.ini est utilisé par le format ISAM Outlook et le format ISAM Exchange pratiquement de la même manière que par le format ISAM texte. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en fome des données, noms des colonnes auxquelles accéder.</span><span class="sxs-lookup"><span data-stu-id="0ac70-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="0ac70-p106">Il n'est pas nécessaire de modifier le fichier Schema.ini pour pouvoir lire, importer ou exporter des données pour Outlook et Exchange. De nombreux paramètres du fichier Schema.ini pour Outlook et Exchange sont spécifiques à des balises internes requises par MAPI. Vous ne devez pas tenter de modifier les valeurs de ces balises.</span><span class="sxs-lookup"><span data-stu-id="0ac70-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

