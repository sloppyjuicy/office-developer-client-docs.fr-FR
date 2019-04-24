---
title: Utilisation d’ActiveX Data Objects (ADO)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312739"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="afde3-103">Utilisation d’ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="afde3-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="afde3-104">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="afde3-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="afde3-105">Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="afde3-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="afde3-106">Objets de données Microsoft ActiveX (ADO)</span><span class="sxs-lookup"><span data-stu-id="afde3-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="afde3-107">ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="afde3-108">Microsoft ADO ext. for DDL and Security (ADOX)</span><span class="sxs-lookup"><span data-stu-id="afde3-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="afde3-109">ADOX fournit les objets DDL (Data Definition Language) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires à la gestion de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="afde3-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="afde3-110">Bibliothèque Microsoft Jet et rePlication Objects 2,5 (JRO)</span><span class="sxs-lookup"><span data-stu-id="afde3-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="afde3-111">Étant donné que les objets ADO ont été conçus pour fonctionner avec de nombreuses bases de données en plus des bases de données Microsoft Jet, les fonctionnalités propres à jet ont été décomposées dans la bibliothèque JRO.</span><span class="sxs-lookup"><span data-stu-id="afde3-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="afde3-112">Le tableau ci-dessous indique les fonctionnalités offertes par chaque composant par rapport à DAO.</span><span class="sxs-lookup"><span data-stu-id="afde3-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="afde3-113">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="afde3-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="afde3-114">DAO</span><span class="sxs-lookup"><span data-stu-id="afde3-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="afde3-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="afde3-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="afde3-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="afde3-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="afde3-117">JRO</span><span class="sxs-lookup"><span data-stu-id="afde3-117">JRO</span></span><br />
<span data-ttu-id="afde3-118">(MDB uniquement)</span><span class="sxs-lookup"><span data-stu-id="afde3-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afde3-119">Créez des jeux d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="afde3-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="afde3-120">X</span><span class="sxs-lookup"><span data-stu-id="afde3-120">X</span></span></p></td>
<td><p><span data-ttu-id="afde3-121">X</span><span class="sxs-lookup"><span data-stu-id="afde3-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-122">Modifier les propriétés de démarrage.</span><span class="sxs-lookup"><span data-stu-id="afde3-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="afde3-123">X</span><span class="sxs-lookup"><span data-stu-id="afde3-123">X</span></span></p></td>
<td><p><span data-ttu-id="afde3-124">X \* \*</span><span class="sxs-lookup"><span data-stu-id="afde3-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-125">Prendre en charge ANSI92 SQL. \* \* \*</span><span class="sxs-lookup"><span data-stu-id="afde3-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-126">X</span><span class="sxs-lookup"><span data-stu-id="afde3-126">X</span></span></p></td>
<td><p><span data-ttu-id="afde3-127">X</span><span class="sxs-lookup"><span data-stu-id="afde3-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-128">Créer des tables.</span><span class="sxs-lookup"><span data-stu-id="afde3-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="afde3-129">X</span><span class="sxs-lookup"><span data-stu-id="afde3-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-130">X</span><span class="sxs-lookup"><span data-stu-id="afde3-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-131">Créer une nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="afde3-132">X</span><span class="sxs-lookup"><span data-stu-id="afde3-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-133">ActiveX</span><span class="sxs-lookup"><span data-stu-id="afde3-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-134">Modifier les propriétés d'une table existante.</span><span class="sxs-lookup"><span data-stu-id="afde3-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="afde3-135">X</span><span class="sxs-lookup"><span data-stu-id="afde3-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-136">X</span><span class="sxs-lookup"><span data-stu-id="afde3-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-137">Créer des relations entre les tables.</span><span class="sxs-lookup"><span data-stu-id="afde3-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="afde3-138">X</span><span class="sxs-lookup"><span data-stu-id="afde3-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-139">ActiveX</span><span class="sxs-lookup"><span data-stu-id="afde3-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-140">Modifier les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="afde3-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="afde3-141">X</span><span class="sxs-lookup"><span data-stu-id="afde3-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-142">ActiveX</span><span class="sxs-lookup"><span data-stu-id="afde3-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-143">Prise en charge de l'attribut de compression pour les données de colonne.</span><span class="sxs-lookup"><span data-stu-id="afde3-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-144">X</span><span class="sxs-lookup"><span data-stu-id="afde3-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-145">Modifier des requêtes ou des vues SQL de base stockées.</span><span class="sxs-lookup"><span data-stu-id="afde3-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="afde3-146">X</span><span class="sxs-lookup"><span data-stu-id="afde3-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-147">ActiveX</span><span class="sxs-lookup"><span data-stu-id="afde3-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-148">Créer des requêtes permanentes uniquement accessibles par code</span><span class="sxs-lookup"><span data-stu-id="afde3-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-149">ActiveX</span><span class="sxs-lookup"><span data-stu-id="afde3-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-150">Créer des requêtes accessibles par conteneur/IU et code de base de données</span><span class="sxs-lookup"><span data-stu-id="afde3-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="afde3-151">X</span><span class="sxs-lookup"><span data-stu-id="afde3-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-152">Compacter/coder la base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="afde3-153">X</span><span class="sxs-lookup"><span data-stu-id="afde3-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-154">X</span><span class="sxs-lookup"><span data-stu-id="afde3-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-155">Actualiser le cache.</span><span class="sxs-lookup"><span data-stu-id="afde3-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="afde3-156">X</span><span class="sxs-lookup"><span data-stu-id="afde3-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-157">X</span><span class="sxs-lookup"><span data-stu-id="afde3-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-158">Rendez la base de données réplicable.</span><span class="sxs-lookup"><span data-stu-id="afde3-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="afde3-159">X</span><span class="sxs-lookup"><span data-stu-id="afde3-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-160">X3</span><span class="sxs-lookup"><span data-stu-id="afde3-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-161">Créer des réplicas de base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="afde3-162">X</span><span class="sxs-lookup"><span data-stu-id="afde3-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-163">X3</span><span class="sxs-lookup"><span data-stu-id="afde3-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-164">Synchroniser les réplicas.</span><span class="sxs-lookup"><span data-stu-id="afde3-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="afde3-165">X</span><span class="sxs-lookup"><span data-stu-id="afde3-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="afde3-166">X3</span><span class="sxs-lookup"><span data-stu-id="afde3-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-167">Modifier les propriétés de la base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="afde3-168">X</span><span class="sxs-lookup"><span data-stu-id="afde3-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afde3-169">Créer des propriétés de base de données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="afde3-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="afde3-170">X</span><span class="sxs-lookup"><span data-stu-id="afde3-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afde3-171">Modifier les propriétés d'une colonne de tableau.</span><span class="sxs-lookup"><span data-stu-id="afde3-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="afde3-172">X</span><span class="sxs-lookup"><span data-stu-id="afde3-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="afde3-p101">\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="afde3-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="afde3-175">\*\* Uniquement disponible pour la manipulation de projets Access.</span><span class="sxs-lookup"><span data-stu-id="afde3-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="afde3-176">\*\*\*Bien que le moteur de base de données Access prenne en charge certains ANSI 92 SQL, il n'est pas encore entièrement conforme à ANSI92.</span><span class="sxs-lookup"><span data-stu-id="afde3-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="afde3-177">1 utilise l'objet **Connection** pour référencer la base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="afde3-178">2 utilise l'objet **catalogue** pour référencer la base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="afde3-179">3 utilise \*\*\*\* l'objet Replica pour référencer la base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="afde3-180">4 utilise l'objet **JetEngine** pour référencer la base de données.</span><span class="sxs-lookup"><span data-stu-id="afde3-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="afde3-181">À la différence des objets DAO, les objets ADO et ADOX peuvent exécuter les actions marquées dans des bases de données autres que Jet tant que le fournisseur de ces bases de données prend en charge cette action.</span><span class="sxs-lookup"><span data-stu-id="afde3-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


