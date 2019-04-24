---
title: SchemaEnum (référence de base de données de bureau Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308862"
---
# <a name="schemaenum"></a><span data-ttu-id="beae1-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="beae1-102">SchemaEnum</span></span>

<span data-ttu-id="beae1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="beae1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="beae1-104">Spécifie le type de **Recordset** de schéma extrait par la méthode [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="beae1-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="beae1-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="beae1-105">Remarks</span></span>

<span data-ttu-id="beae1-106">D'autres informations sur la fonction et les colonnes renvoyées pour chaque constante ADO sont présentes dans les rubriques de l'Annexe B du manuel *OLE DB Programmers Reference*.</span><span class="sxs-lookup"><span data-stu-id="beae1-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="beae1-107">Le nom de chaque rubrique est mentionné entre parenthèses dans la section Description du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="beae1-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="beae1-108">D'autres informations sur la fonction et les colonnes renvoyées pour chaque constante ADO MD sont présentes dans les rubriques du chapitre 23 du manuel *OLE DB Programmers Reference*.</span><span class="sxs-lookup"><span data-stu-id="beae1-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="beae1-109">Le nom de chaque rubrique est indiqué entre parenthèses et marqué d'un astérisque (\*) dans la colonne Description du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="beae1-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="beae1-110">Convertissez les types de données des colonnes de la documentation OLE DB en types de données ADO en vous reportant à la colonne de la rubrique [DataTypeEnum](datatypeenum.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="beae1-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="beae1-111">Par exemple, un type de données OLE DB **de\_DbType WSTR** équivaut à un type de données ADO **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="beae1-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="beae1-112">ADO génère des résultats de type schéma pour les constantes **adSchemaDBInfoKeywords** et **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="beae1-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="beae1-113">ADO crée un **objet Recordset**, puis remplit chaque ligne avec les valeurs renvoyées par les méthodes **IDBInfo:: GetKeywords** et **IDBInfo:: GetLiteralInfo** .</span><span class="sxs-lookup"><span data-stu-id="beae1-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="beae1-114">Vous trouverez des informations supplémentaires sur ces méthodes dans la section IDBInfo du *Guide OLE DB Programmer's Reference*(en anglais).</span><span class="sxs-lookup"><span data-stu-id="beae1-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="beae1-115">Constante</span><span class="sxs-lookup"><span data-stu-id="beae1-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="beae1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="beae1-116">Value</span></span></p></th>
<th><p><span data-ttu-id="beae1-117">Description</span><span class="sxs-lookup"><span data-stu-id="beae1-117">Description</span></span></p></th>
<th><p><span data-ttu-id="beae1-118">Colonnes de contrainte</span><span class="sxs-lookup"><span data-stu-id="beae1-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="beae1-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-120">0</span><span class="sxs-lookup"><span data-stu-id="beae1-120">0</span></span></p></td>
<td><p><span data-ttu-id="beae1-121">Renvoie les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-122">(ASSERTIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="beae1-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="beae1-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-127">0,1</span><span class="sxs-lookup"><span data-stu-id="beae1-127">1</span></span></p></td>
<td><p><span data-ttu-id="beae1-128">Renvoie les attributs physiques associés aux catalogues accessibles depuis le DBMS.</span><span class="sxs-lookup"><span data-stu-id="beae1-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="beae1-129">(CATALOGS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-132">n°2</span><span class="sxs-lookup"><span data-stu-id="beae1-132">2</span></span></p></td>
<td><p><span data-ttu-id="beae1-133">Renvoie les jeux de caractères définis dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="beae1-134">(CHARACTER_SETS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="beae1-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="beae1-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-139">disque</span><span class="sxs-lookup"><span data-stu-id="beae1-139">5</span></span></p></td>
<td><p><span data-ttu-id="beae1-140">Renvoie les contraintes de contrôle définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-141">(CHECK_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="beae1-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="beae1-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-146">3</span><span class="sxs-lookup"><span data-stu-id="beae1-146">3</span></span></p></td>
<td><p><span data-ttu-id="beae1-147">Renvoie les collations de caractères définies dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="beae1-148">(COLLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="beae1-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="beae1-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-153">kg</span><span class="sxs-lookup"><span data-stu-id="beae1-153">13</span></span></p></td>
<td><p><span data-ttu-id="beae1-154">Renvoie les privilèges des colonnes des tables définies dans le catalogue,  accordés à un utilisateur donné, ou accordés par ce dernier.</span><span class="sxs-lookup"><span data-stu-id="beae1-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="beae1-155">(COLUMN_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-158">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-158">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-159">COMPORTE</span><span class="sxs-lookup"><span data-stu-id="beae1-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="beae1-160">ACCORDEROU</span><span class="sxs-lookup"><span data-stu-id="beae1-160">GRANTOR</span></span><br />
<span data-ttu-id="beae1-161">BÉNÉFICIAIRE</span><span class="sxs-lookup"><span data-stu-id="beae1-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-163">4</span><span class="sxs-lookup"><span data-stu-id="beae1-163">4</span></span></p></td>
<td><p><span data-ttu-id="beae1-164">Renvoie les colonnes des tables (vues comprises) définies dans le catalogue et accessibles à un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="beae1-165">(COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-168">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-168">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-169">COMPORTE</span><span class="sxs-lookup"><span data-stu-id="beae1-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-171">a4</span><span class="sxs-lookup"><span data-stu-id="beae1-171">11</span></span></p></td>
<td><p><span data-ttu-id="beae1-172">Renvoie les colonnes définies dans le catalogue et qui dépendent d'un domaine défini dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="beae1-173">(COLUMN_DOMAIN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="beae1-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="beae1-176">NOM_DOMAINE</span><span class="sxs-lookup"><span data-stu-id="beae1-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="beae1-177">COMPORTE</span><span class="sxs-lookup"><span data-stu-id="beae1-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-179">6.x</span><span class="sxs-lookup"><span data-stu-id="beae1-179">6</span></span></p></td>
<td><p><span data-ttu-id="beae1-180">Renvoie les colonnes utilisées par les contraintes référentielles, uniques et de contrôle, ainsi que par les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="beae1-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-184">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-184">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-185">COMPORTE</span><span class="sxs-lookup"><span data-stu-id="beae1-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-187">7j/7</span><span class="sxs-lookup"><span data-stu-id="beae1-187">7</span></span></p></td>
<td><p><span data-ttu-id="beae1-188">Renvoie les tables utilisées par les contraintes référentielles, uniques et de contrôle, ainsi que par les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="beae1-189">(CONSTRAINT_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-192">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-194">32</span><span class="sxs-lookup"><span data-stu-id="beae1-194">32</span></span></p></td>
<td><p><span data-ttu-id="beae1-195">Renvoie des informations sur les cubes disponibles dans un schéma (ou catalogue, si le fournisseur ne prend pas en charge les schémas).</span><span class="sxs-lookup"><span data-stu-id="beae1-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="beae1-196">(CUBES Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="beae1-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-201">0,30</span><span class="sxs-lookup"><span data-stu-id="beae1-201">30</span></span></p></td>
<td><p><span data-ttu-id="beae1-202">Renvoie la liste des mots réservés spécifiques aux fournisseur.</span><span class="sxs-lookup"><span data-stu-id="beae1-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="beae1-203">(IDBInfo:: GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-204">&lt;Nul&gt;</span><span class="sxs-lookup"><span data-stu-id="beae1-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-206">31</span><span class="sxs-lookup"><span data-stu-id="beae1-206">31</span></span></p></td>
<td><p><span data-ttu-id="beae1-207">Renvoie la liste des chaînes littérales spécifiques aux fournisseurs et utilisées dans les commandes texte.</span><span class="sxs-lookup"><span data-stu-id="beae1-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="beae1-208">(IDBInfo:: GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-209">&lt;Nul&gt;</span><span class="sxs-lookup"><span data-stu-id="beae1-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-211">33</span><span class="sxs-lookup"><span data-stu-id="beae1-211">33</span></span></p></td>
<td><p><span data-ttu-id="beae1-212">Renvoie des informations sur les dimensions d'un cube donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="beae1-213">Chaque dimension possède sa ligne propre.</span><span class="sxs-lookup"><span data-stu-id="beae1-213">It has one row for each dimension.</span></span> <span data-ttu-id="beae1-214">(DIMENSIONS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-217">CUBE_NAME</span></span><br />
<span data-ttu-id="beae1-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="beae1-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-221">vingt</span><span class="sxs-lookup"><span data-stu-id="beae1-221">27</span></span></p></td>
<td><p><span data-ttu-id="beae1-222">Renvoie les colonnes de clés étrangères définies dans le catalogue par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="beae1-223">(FOREIGN_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-231">34</span><span class="sxs-lookup"><span data-stu-id="beae1-231">34</span></span></p></td>
<td><p><span data-ttu-id="beae1-232">Renvoie des informations sur les hiérarchies disponibles dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="beae1-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="beae1-233">(HIERARCHIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-236">CUBE_NAME</span></span><br />
<span data-ttu-id="beae1-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="beae1-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-241">an</span><span class="sxs-lookup"><span data-stu-id="beae1-241">12</span></span></p></td>
<td><p><span data-ttu-id="beae1-242">Renvoie les index définis dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-243">(INDEXES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-246">INDEX_NAME</span></span><br />
<span data-ttu-id="beae1-247">ENTRER</span><span class="sxs-lookup"><span data-stu-id="beae1-247">TYPE</span></span><br />
<span data-ttu-id="beae1-248">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-250">8bits</span><span class="sxs-lookup"><span data-stu-id="beae1-250">8</span></span></p></td>
<td><p><span data-ttu-id="beae1-251">Renvoie les colonnes définies dans le catalogue et qui sont contraintes sous forme de clés par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="beae1-252">(KEY_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="beae1-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="beae1-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="beae1-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-258">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-258">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-259">COMPORTE</span><span class="sxs-lookup"><span data-stu-id="beae1-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-261">35</span><span class="sxs-lookup"><span data-stu-id="beae1-261">35</span></span></p></td>
<td><p><span data-ttu-id="beae1-262">Renvoie des informations sur les niveaux disponibles dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="beae1-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="beae1-263">(LEVELS Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="beae1-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-266">CUBE_NAME</span></span><br />
<span data-ttu-id="beae1-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="beae1-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-272">36</span><span class="sxs-lookup"><span data-stu-id="beae1-272">36</span></span></p></td>
<td><p><span data-ttu-id="beae1-273">Renvoie des informations sur les mesures disponibles.</span><span class="sxs-lookup"><span data-stu-id="beae1-273">Returns information about the available measures.</span></span> <span data-ttu-id="beae1-274">(MEASURES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-277">CUBE_NAME</span></span><br />
<span data-ttu-id="beae1-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="beae1-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-281">38</span><span class="sxs-lookup"><span data-stu-id="beae1-281">38</span></span></p></td>
<td><p><span data-ttu-id="beae1-282">Renvoie des informations sur les membres disponibles.</span><span class="sxs-lookup"><span data-stu-id="beae1-282">Returns information about the available members.</span></span> <span data-ttu-id="beae1-283">(MEMBERS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-286">CUBE_NAME</span></span><br />
<span data-ttu-id="beae1-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="beae1-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="beae1-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="beae1-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="beae1-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="beae1-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="beae1-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="beae1-295">Opérateur d'arborescence (pour plus d'informations, reportez-vous à la documentation OLE DB pour OLAP.)</span><span class="sxs-lookup"><span data-stu-id="beae1-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-297">vingt</span><span class="sxs-lookup"><span data-stu-id="beae1-297">28</span></span></p></td>
<td><p><span data-ttu-id="beae1-298">Renvoie les colonnes de clés primaires définies dans le catalogue par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="beae1-299">(PRIMARY_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-304">29</span><span class="sxs-lookup"><span data-stu-id="beae1-304">29</span></span></p></td>
<td><p><span data-ttu-id="beae1-305">Renvoie des informations sur les colonnes de jeux de lignes renvoyées par des procédures.</span><span class="sxs-lookup"><span data-stu-id="beae1-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="beae1-306">(PROCEDURE_COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="beae1-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="beae1-310">COMPORTE</span><span class="sxs-lookup"><span data-stu-id="beae1-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-312">27</span><span class="sxs-lookup"><span data-stu-id="beae1-312">26</span></span></p></td>
<td><p><span data-ttu-id="beae1-313">Renvoie des informations sur les paramètres et les codes de retour des procédures.</span><span class="sxs-lookup"><span data-stu-id="beae1-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="beae1-314">(PROCEDURE_PARAMETERS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="beae1-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="beae1-318">NOM_DE_PARAMÈTRE</span><span class="sxs-lookup"><span data-stu-id="beae1-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-320">Seiz</span><span class="sxs-lookup"><span data-stu-id="beae1-320">16</span></span></p></td>
<td><p><span data-ttu-id="beae1-321">Renvoie les procédures définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-322">(PROCEDURES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="beae1-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="beae1-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="beae1-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-328">37</span><span class="sxs-lookup"><span data-stu-id="beae1-328">37</span></span></p></td>
<td><p><span data-ttu-id="beae1-329">Renvoie des informations sur les propriétés disponibles pour chaque niveau de la dimension.</span><span class="sxs-lookup"><span data-stu-id="beae1-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="beae1-330">(PROPERTIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="beae1-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="beae1-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-333">CUBE_NAME</span></span><br />
<span data-ttu-id="beae1-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="beae1-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="beae1-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="beae1-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-341">-1</span><span class="sxs-lookup"><span data-stu-id="beae1-341">-1</span></span></p></td>
<td><p><span data-ttu-id="beae1-342">Utilisé si le fournisseur définit ses propres requêtes de schéma non standard.</span><span class="sxs-lookup"><span data-stu-id="beae1-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="beae1-343">&lt;Spécifique au fournisseur&gt;</span><span class="sxs-lookup"><span data-stu-id="beae1-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-345">22,5</span><span class="sxs-lookup"><span data-stu-id="beae1-345">22</span></span></p></td>
<td><p><span data-ttu-id="beae1-346">Renvoie les types de données (primaires) pris en charge par le fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="beae1-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="beae1-347">(PROVIDER_TYPES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-348">TYPE_DE_DONNÉES</span><span class="sxs-lookup"><span data-stu-id="beae1-348">DATA_TYPE</span></span><br />
<span data-ttu-id="beae1-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="beae1-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-351">4,9</span><span class="sxs-lookup"><span data-stu-id="beae1-351">9</span></span></p></td>
<td><p><span data-ttu-id="beae1-352">Renvoie les contraintes référentielles définies dans le catalogie et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-353">(REFERENTIAL_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="beae1-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="beae1-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-358">cm</span><span class="sxs-lookup"><span data-stu-id="beae1-358">17</span></span></p></td>
<td><p><span data-ttu-id="beae1-359">Renvoie les schémas (objets de la base de données) dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="beae1-360">(SCHEMATA Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="beae1-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="beae1-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="beae1-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-365">18</span><span class="sxs-lookup"><span data-stu-id="beae1-365">18</span></span></p></td>
<td><p><span data-ttu-id="beae1-366">Renvoie les niveaux de conformité, les options et les dialectes pris en charge par les données de traitement d'implémentation SQL définies dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="beae1-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="beae1-367">(SQL_LANGUAGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-368">&lt;Nul&gt;</span><span class="sxs-lookup"><span data-stu-id="beae1-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-370">neuf</span><span class="sxs-lookup"><span data-stu-id="beae1-370">19</span></span></p></td>
<td><p><span data-ttu-id="beae1-371">Renvoie les statistiques définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-372">(STATISTICS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-375">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-377">10</span><span class="sxs-lookup"><span data-stu-id="beae1-377">10</span></span></p></td>
<td><p><span data-ttu-id="beae1-378">Renvoie les contraintes de table définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="beae1-379">(TABLE_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="beae1-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="beae1-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="beae1-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-385">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-385">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="beae1-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-388">13</span><span class="sxs-lookup"><span data-stu-id="beae1-388">14</span></span></p></td>
<td><p><span data-ttu-id="beae1-389">Renvoie les privilèges sur les tables définies dans le catalogue et qui sont disponibles pour un utilisateur donné, ou accordés par ce dernier.</span><span class="sxs-lookup"><span data-stu-id="beae1-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="beae1-390">(TABLE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-393">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-393">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-394">ACCORDEROU</span><span class="sxs-lookup"><span data-stu-id="beae1-394">GRANTOR</span></span><br />
<span data-ttu-id="beae1-395">BÉNÉFICIAIRE</span><span class="sxs-lookup"><span data-stu-id="beae1-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-397">vingtaine</span><span class="sxs-lookup"><span data-stu-id="beae1-397">20</span></span></p></td>
<td><p><span data-ttu-id="beae1-398">Renvoie les tables (notamment les vues) définies dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="beae1-399">(TABLES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-402">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-402">TABLE_NAME</span></span><br />
<span data-ttu-id="beae1-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="beae1-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-405">21</span><span class="sxs-lookup"><span data-stu-id="beae1-405">21</span></span></p></td>
<td><p><span data-ttu-id="beae1-406">Renvoie les conversions de caractères définies dans le catalogue et auxquelles un utilisateur donné a accès.</span><span class="sxs-lookup"><span data-stu-id="beae1-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="beae1-407">(TRANSLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="beae1-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="beae1-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-412">39</span><span class="sxs-lookup"><span data-stu-id="beae1-412">39</span></span></p></td>
<td><p><span data-ttu-id="beae1-413">Réservé pour usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="beae1-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-415">0,15</span><span class="sxs-lookup"><span data-stu-id="beae1-415">15</span></span></p></td>
<td><p><span data-ttu-id="beae1-416">Renvoie les privilèges USAGE sur les objets définis dans le catalogue et qui sont disponibles pour un utilisateur donné, ou accordés par ce dernier.</span><span class="sxs-lookup"><span data-stu-id="beae1-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="beae1-417">(USAGE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="beae1-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="beae1-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="beae1-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="beae1-421">TYPE_OBJET</span><span class="sxs-lookup"><span data-stu-id="beae1-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="beae1-422">ACCORDEROU</span><span class="sxs-lookup"><span data-stu-id="beae1-422">GRANTOR</span></span><br />
<span data-ttu-id="beae1-423">BÉNÉFICIAIRE</span><span class="sxs-lookup"><span data-stu-id="beae1-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-425">heures/24</span><span class="sxs-lookup"><span data-stu-id="beae1-425">24</span></span></p></td>
<td><p><span data-ttu-id="beae1-426">Renvoie les colonnes desquelles dépendent les tables vues, définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="beae1-427">(VIEW_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="beae1-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="beae1-430">NOM_DE_VUE</span><span class="sxs-lookup"><span data-stu-id="beae1-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-432">23</span><span class="sxs-lookup"><span data-stu-id="beae1-432">23</span></span></p></td>
<td><p><span data-ttu-id="beae1-433">Renvoie les vues définies dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="beae1-434">(VIEWS Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="beae1-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="beae1-437">NOM_DE_TABLE</span><span class="sxs-lookup"><span data-stu-id="beae1-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="beae1-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="beae1-439">25</span><span class="sxs-lookup"><span data-stu-id="beae1-439">25</span></span></p></td>
<td><p><span data-ttu-id="beae1-440">Renvoie les tables desquelles dépendent les tables vues, définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="beae1-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="beae1-441">(VIEW_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="beae1-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="beae1-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="beae1-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="beae1-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="beae1-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="beae1-444">NOM_DE_VUE</span><span class="sxs-lookup"><span data-stu-id="beae1-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="beae1-445">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="beae1-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="beae1-446">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="beae1-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="beae1-447">Constante</span><span class="sxs-lookup"><span data-stu-id="beae1-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="beae1-448">AdoEnums. Schema. asSERTs</span><span class="sxs-lookup"><span data-stu-id="beae1-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-449">AdoEnums. Schema. CATALOGs</span><span class="sxs-lookup"><span data-stu-id="beae1-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-450">AdoEnums. Schema. CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="beae1-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-451">AdoEnums. Schema. CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="beae1-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-452">AdoEnums. Schema. COLLATIONs</span><span class="sxs-lookup"><span data-stu-id="beae1-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-453">AdoEnums. Schema. COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="beae1-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-454">AdoEnums. Schema. COLUMNs</span><span class="sxs-lookup"><span data-stu-id="beae1-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-455">AdoEnums. Schema. COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="beae1-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-456">AdoEnums. Schema. CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="beae1-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-457">AdoEnums. Schema. CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="beae1-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-458">AdoEnums. Schema. CUBEs</span><span class="sxs-lookup"><span data-stu-id="beae1-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-459">AdoEnums. Schema. DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="beae1-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-460">AdoEnums. Schema. DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="beae1-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-461">AdoEnums. Schema. DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="beae1-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-462">AdoEnums. Schema. FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="beae1-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-463">AdoEnums. Schema. HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="beae1-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-464">AdoEnums. Schema. INDEXes</span><span class="sxs-lookup"><span data-stu-id="beae1-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-465">AdoEnums. Schema. KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="beae1-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-466">AdoEnums. Schema. LEVELs</span><span class="sxs-lookup"><span data-stu-id="beae1-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-467">AdoEnums. Schema. MEASURes</span><span class="sxs-lookup"><span data-stu-id="beae1-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-468">AdoEnums. Schema. MEMBERs</span><span class="sxs-lookup"><span data-stu-id="beae1-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-469">AdoEnums. Schema. PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="beae1-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-470">AdoEnums. Schema. PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="beae1-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-471">AdoEnums. Schema. PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beae1-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-472">AdoEnums. Schema. PROCEDUREs</span><span class="sxs-lookup"><span data-stu-id="beae1-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-473">AdoEnums. Schema. PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="beae1-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-474">AdoEnums. Schema. PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="beae1-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-475">AdoEnums. Schema. PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="beae1-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-476">AdoEnums. Schema. REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="beae1-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-477">AdoEnums. Schema. SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="beae1-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-478">AdoEnums. Schema. SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="beae1-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-479">AdoEnums. Schema. STATISTICs</span><span class="sxs-lookup"><span data-stu-id="beae1-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-480">AdoEnums. Schema. TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="beae1-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-481">AdoEnums. Schema. TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="beae1-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-482">AdoEnums. Schema. TABLES</span><span class="sxs-lookup"><span data-stu-id="beae1-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-483">AdoEnums. Schema. TRANSLATIONs</span><span class="sxs-lookup"><span data-stu-id="beae1-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-484">Énumération AdoEnums. Schema. TRUSTed</span><span class="sxs-lookup"><span data-stu-id="beae1-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-485">AdoEnums. Schema. USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="beae1-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-486">AdoEnums. Schema. VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="beae1-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beae1-487">AdoEnums. Schema. VIEWS</span><span class="sxs-lookup"><span data-stu-id="beae1-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beae1-488">AdoEnums. Schema. VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="beae1-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

