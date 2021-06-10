---
title: Initialisation du pilote de source Exchange données Microsoft
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
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="593d5-102">Initialisation du pilote de source Exchange données Microsoft</span><span class="sxs-lookup"><span data-stu-id="593d5-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="593d5-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="593d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="593d5-104">Lorsque vous installez le pilote de source de données Microsoft Exchange, le programme d’installation écrit un ensemble de valeurs par défaut dans le Registre Microsoft Windows dans les sous-clés Engines et ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="593d5-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="593d5-105">Vous ne devez pas modifier ces paramètres directement ; utilisez le programme d’installation de votre application pour ajouter, supprimer ou modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="593d5-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="593d5-106">Les sections suivantes décrivent l’initialisation et les paramètres de format ISAM pour le pilote de source de données Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="593d5-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="593d5-107">Paramètres d Exchange d’initialisation de la source de données Microsoft</span><span class="sxs-lookup"><span data-stu-id="593d5-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="593d5-108">Le dossier Exchange Access **Connectivity \\ Engines \\** inclut les paramètres d’initialisation du pilote Aceexch.dll, utilisé pour l’accès externe aux dossiers Microsoft Outlook et Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="593d5-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="593d5-109">L'unique entrée dans ce dossier est la suivante :</span><span class="sxs-lookup"><span data-stu-id="593d5-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="593d5-110">Le moteur de base de données Microsoft Exchange utilise ce paramètre pour indiquer l'emplacement du pilote Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="593d5-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="593d5-111">Le chemin d'accès complet est déterminé au moment de l'installation.</span><span class="sxs-lookup"><span data-stu-id="593d5-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="593d5-112">Les valeurs sont de type REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="593d5-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="593d5-p104">Le format ISAM du client Outlook et le format ISAM du client Exchange donnent des résultats similaires. La seule différence est que ces deux clients utilisent des noms différents pour les mêmes colonnes. Les deux formats ISAM ont été créés afin que le moteur de base de données Microsoft Access puisse retourner les noms de colonnes dans un style particulier souhaité par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="593d5-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="593d5-116">Formats ISAM du client Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="593d5-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="593d5-117">Les formats ISAM du moteur **de connectivité Access Outlook \\ \\ 9.0** contiennent les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="593d5-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="593d5-118">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="593d5-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="593d5-119">Type</span><span class="sxs-lookup"><span data-stu-id="593d5-119">Type</span></span></p></th>
<th><p><span data-ttu-id="593d5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d5-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="593d5-121">Moteur</span><span class="sxs-lookup"><span data-stu-id="593d5-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="593d5-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="593d5-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="593d5-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="593d5-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="593d5-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="593d5-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="593d5-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="593d5-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="593d5-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="593d5-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="593d5-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="593d5-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-129">01</span><span class="sxs-lookup"><span data-stu-id="593d5-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="593d5-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="593d5-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-132">00</span><span class="sxs-lookup"><span data-stu-id="593d5-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="593d5-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="593d5-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="593d5-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="593d5-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="593d5-135">3</span><span class="sxs-lookup"><span data-stu-id="593d5-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="593d5-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="593d5-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-138">00</span><span class="sxs-lookup"><span data-stu-id="593d5-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="593d5-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="593d5-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="593d5-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-141">00</span><span class="sxs-lookup"><span data-stu-id="593d5-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="593d5-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="593d5-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-144">01</span><span class="sxs-lookup"><span data-stu-id="593d5-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="593d5-145">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="593d5-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="593d5-146">Formats ISAM du client Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="593d5-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="593d5-147">Les formats ISAM du moteur **de connectivité Access Exchange \\ \\ 4.0** contiennent les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="593d5-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="593d5-148">Nom d'entrée</span><span class="sxs-lookup"><span data-stu-id="593d5-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="593d5-149">Type</span><span class="sxs-lookup"><span data-stu-id="593d5-149">Type</span></span></p></th>
<th><p><span data-ttu-id="593d5-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d5-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="593d5-151">Moteur</span><span class="sxs-lookup"><span data-stu-id="593d5-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="593d5-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="593d5-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="593d5-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="593d5-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="593d5-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="593d5-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="593d5-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="593d5-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="593d5-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="593d5-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="593d5-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="593d5-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-159">01</span><span class="sxs-lookup"><span data-stu-id="593d5-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="593d5-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="593d5-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-162">00</span><span class="sxs-lookup"><span data-stu-id="593d5-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="593d5-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="593d5-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="593d5-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="593d5-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="593d5-165">3</span><span class="sxs-lookup"><span data-stu-id="593d5-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="593d5-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="593d5-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-168">00</span><span class="sxs-lookup"><span data-stu-id="593d5-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="593d5-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="593d5-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="593d5-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-171">00</span><span class="sxs-lookup"><span data-stu-id="593d5-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="593d5-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="593d5-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="593d5-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="593d5-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="593d5-174">01</span><span class="sxs-lookup"><span data-stu-id="593d5-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="593d5-175">Lorsque vous modifiez des paramètres de registre Windows, vous devez redémarrer le moteur de base de données pour que les nouveaux paramètres entrent en vigueur.</span><span class="sxs-lookup"><span data-stu-id="593d5-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="593d5-176">Personnalisation du fichier Schema.ini pour les données Outlook et Exchange données</span><span class="sxs-lookup"><span data-stu-id="593d5-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="593d5-p105">Le fichier Schema.ini est utilisé par le format ISAM Outlook et le format ISAM Exchange pratiquement de la même manière que par le format ISAM texte. Le fichier Schema.ini contient les paramètres spécifiques d'une source de données : mise en fome des données, noms des colonnes auxquelles accéder.</span><span class="sxs-lookup"><span data-stu-id="593d5-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="593d5-p106">Il n'est pas nécessaire de modifier le fichier Schema.ini pour pouvoir lire, importer ou exporter des données pour Outlook et Exchange. De nombreux paramètres du fichier Schema.ini pour Outlook et Exchange sont spécifiques à des balises internes requises par MAPI. Vous ne devez pas tenter de modifier les valeurs de ces balises.</span><span class="sxs-lookup"><span data-stu-id="593d5-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

