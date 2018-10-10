---
title: Utilisation des objets de données ActiveX
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470213"
---
# <a name="using-activex-data-objects"></a><span data-ttu-id="3f5d5-102">Utilisation des objets de données ActiveX</span><span class="sxs-lookup"><span data-stu-id="3f5d5-102">Using ActiveX Data Objects</span></span>


<span data-ttu-id="3f5d5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f5d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3f5d5-104">Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-104">Microsoft Access provides three object models to use in the creation, maintaining and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="3f5d5-105">Objets de données Microsoft ActiveX (ADO)</span><span class="sxs-lookup"><span data-stu-id="3f5d5-105">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="3f5d5-106">ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-106">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="3f5d5-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3f5d5-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span></span>

<span data-ttu-id="3f5d5-108">ADOX comprend les objets DDL (Data Definition Language, langage de définition de données) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires pour gérer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-108">ADOX provides the Data Definition Language(DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

<span data-ttu-id="3f5d5-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span><span class="sxs-lookup"><span data-stu-id="3f5d5-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span></span>

<span data-ttu-id="3f5d5-110">Du fait que les objets ADO ont été créés pour fonctionner avec de nombreuses bases de données, en plus des bases de données Microsoft Jet, la fonctionnalité propre à Jet a été intégrée dans la bibliothèque JRO.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-110">Since ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="3f5d5-111">Le tableau ci-dessous indique les fonctionnalités offertes par chaque composant par rapport à DAO.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-111">The following table lists the functionality provided by each compared to DAO.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f5d5-112">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="3f5d5-112">Functionality</span></span></p></th>
<th><p><span data-ttu-id="3f5d5-113">DAO</span><span class="sxs-lookup"><span data-stu-id="3f5d5-113">DAO</span></span></p></th>
<th><p><span data-ttu-id="3f5d5-114">ADO1</span><span class="sxs-lookup"><span data-stu-id="3f5d5-114">ADO1</span></span></p></th>
<th><p><span data-ttu-id="3f5d5-115">ADOX2</span><span class="sxs-lookup"><span data-stu-id="3f5d5-115">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="3f5d5-116">JRO</span><span class="sxs-lookup"><span data-stu-id="3f5d5-116">JRO</span></span><br />
<span data-ttu-id="3f5d5-117">(Uniquement MDB)</span><span class="sxs-lookup"><span data-stu-id="3f5d5-117">(MDB's Only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-118">Créer des jeux d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="3f5d5-118">Create Recordsets</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-119">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-119">X</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-120">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-120">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-121">Modifier des propriétés de démarrage</span><span class="sxs-lookup"><span data-stu-id="3f5d5-121">Edit Startup properties</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-122">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-122">X</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-123">X\*\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-123">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-124">Prendre en charge ANSI92 SQL\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-124">Support ANSI92 SQL\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-125">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-125">X</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-126">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-126">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-127">Créer des tables</span><span class="sxs-lookup"><span data-stu-id="3f5d5-127">Create Tables</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-128">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-128">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-129">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-129">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-130">Créer une nouvelle base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-130">Create New Database</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-131">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-131">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-132">X\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-132">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-133">Modifier des propriétés de table existantes</span><span class="sxs-lookup"><span data-stu-id="3f5d5-133">Edit Existing Table properties</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-134">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-134">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-135">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-135">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-136">Créer des relations de table</span><span class="sxs-lookup"><span data-stu-id="3f5d5-136">Create table relationships</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-137">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-138">X\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-138">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-139">Modifier des paramètres de sécurité</span><span class="sxs-lookup"><span data-stu-id="3f5d5-139">Edit security settings</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-140">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-140">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-141">X\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-141">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-142">Prendre en charge l’attribut de compression pour les données de colonne</span><span class="sxs-lookup"><span data-stu-id="3f5d5-142">Support for Compression attribute for column data</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-143">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-143">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-144">Modifier des requêtes ou des vues SQL de base stockées</span><span class="sxs-lookup"><span data-stu-id="3f5d5-144">Edit stored, basic SQL queries or views</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-145">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-145">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-146">X\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-146">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-147">Créer des requêtes permanentes uniquement accessibles par code</span><span class="sxs-lookup"><span data-stu-id="3f5d5-147">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-148">X\*</span><span class="sxs-lookup"><span data-stu-id="3f5d5-148">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-149">Créer des requêtes accessibles par conteneur/IU et code de base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-149">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-150">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-150">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-151">Compacter/coder une base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-151">Compact/Encode database</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-152">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-152">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-153">X4</span><span class="sxs-lookup"><span data-stu-id="3f5d5-153">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-154">Actualiser mémoire cache</span><span class="sxs-lookup"><span data-stu-id="3f5d5-154">Refresh Cache</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-155">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-155">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-156">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-156">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-157">Rendre une base de données réplicable</span><span class="sxs-lookup"><span data-stu-id="3f5d5-157">Make Database Replicable</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-158">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-158">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-159">X3</span><span class="sxs-lookup"><span data-stu-id="3f5d5-159">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-160">Faire des réplicas de base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-160">Make Database Replicas</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-161">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-161">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-162">X3</span><span class="sxs-lookup"><span data-stu-id="3f5d5-162">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-163">Synchroniser des réplicas</span><span class="sxs-lookup"><span data-stu-id="3f5d5-163">Synchronize Replicas</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-164">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-164">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3f5d5-165">X3</span><span class="sxs-lookup"><span data-stu-id="3f5d5-165">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-166">Modifier des propriétés de base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-166">Edit Database properties</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-167">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-167">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f5d5-168">Créer des propriétés de base de données personnalisées</span><span class="sxs-lookup"><span data-stu-id="3f5d5-168">Create custom database properties</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-169">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-169">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f5d5-170">Modifier les propriétés d’une colonne de table</span><span class="sxs-lookup"><span data-stu-id="3f5d5-170">Edit table column properties</span></span></p></td>
<td><p><span data-ttu-id="3f5d5-171">X </span><span class="sxs-lookup"><span data-stu-id="3f5d5-171">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3f5d5-p101">\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="3f5d5-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="3f5d5-174">\*\* Uniquement disponible pour la manipulation de projets Access.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-174">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="3f5d5-175">\*\*\* Même si le moteur de base de données Access prend en charge certains codes ANSI 92 SQL, il n'est pas encore totalement compatible à ANSI92.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-175">\*\*\* Though the Access database engine does support some ANSI 92 SQL it is not yet fully ANSI92 compliant.</span></span>

<span data-ttu-id="3f5d5-176">1Utilise un objet **Connection** pour faire référence à une base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-176">1 Uses **Connection** object to reference to database</span></span>

<span data-ttu-id="3f5d5-177">2Utilise un objet **Catalog** pour faire référence à une base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-177">2 Uses **Catalog** object to reference database</span></span>

<span data-ttu-id="3f5d5-178">3Utilise un objet **Replica** pour faire référence à une base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-178">3 Uses **Replica** object to reference database</span></span>

<span data-ttu-id="3f5d5-179">4Utilise un objet **JetEngine** pour faire référence à une base de données</span><span class="sxs-lookup"><span data-stu-id="3f5d5-179">4 Uses **JetEngine** object to reference database</span></span>


> [!NOTE]
> <P><span data-ttu-id="3f5d5-180">[!REMARQUE] À la différence des objets DAO, les objets ADO et ADOX peuvent exécuter les actions indiquées dans des bases de données autres que Jet tant que le fournisseur de celles-ci prend en charge ces actions.</span><span class="sxs-lookup"><span data-stu-id="3f5d5-180">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other then Jet as long as the provider for those databases supports that action.</span></span></P>


