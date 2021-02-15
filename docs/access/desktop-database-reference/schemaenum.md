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
# <a name="schemaenum"></a><span data-ttu-id="4eeb0-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="4eeb0-102">SchemaEnum</span></span>

<span data-ttu-id="4eeb0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eeb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4eeb0-104">Spécifie le type de **Recordset** de schéma extrait par la méthode [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4eeb0-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eeb0-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="4eeb0-105">Remarks</span></span>

<span data-ttu-id="4eeb0-106">D'autres informations sur la fonction et les colonnes renvoyées pour chaque constante ADO sont présentes dans les rubriques de l'Annexe B du manuel *OLE DB Programmers Reference*.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="4eeb0-107">Le nom de chaque rubrique est répertorié entre parenthèses dans la section Description du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="4eeb0-108">D'autres informations sur la fonction et les colonnes renvoyées pour chaque constante ADO MD sont présentes dans les rubriques du chapitre 23 du manuel *OLE DB Programmers Reference*.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="4eeb0-109">Le nom de chaque rubrique est répertorié entre parenthèses et marqué d’un astérisque ( ) dans la colonne \* Description du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="4eeb0-110">Convertissez les types de données des colonnes de la documentation OLE DB en types de données ADO en vous reportant à la colonne de la rubrique [DataTypeEnum](datatypeenum.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="4eeb0-111">Par exemple, un type de données OLE DB **de DBTYPE \_ WSTR** équivaut à un type de données ADO **d’adWChar**.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="4eeb0-112">ADO génère des résultats de type schéma pour les constantes **adSchemaDBInfoKeywords** et **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="4eeb0-113">ADO crée un **recordset,** puis remplit chaque ligne avec les valeurs renvoyées respectivement par les méthodes **IDBInfo::GetKeywords** et **IDBInfo::GetLiteralInfo.**</span><span class="sxs-lookup"><span data-stu-id="4eeb0-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="4eeb0-114">Vous pouvez trouver des informations supplémentaires sur ces méthodes dans la section IDBInfo du *OLE DB Programmer’s Reference*.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="4eeb0-115">Constante</span><span class="sxs-lookup"><span data-stu-id="4eeb0-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="4eeb0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eeb0-116">Value</span></span></p></th>
<th><p><span data-ttu-id="4eeb0-117">Description</span><span class="sxs-lookup"><span data-stu-id="4eeb0-117">Description</span></span></p></th>
<th><p><span data-ttu-id="4eeb0-118">Colonnes de contrainte</span><span class="sxs-lookup"><span data-stu-id="4eeb0-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-120">0</span><span class="sxs-lookup"><span data-stu-id="4eeb0-120">0</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-121">Renvoie les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-122">(ASSERTIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-127">1 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-127">1</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-128">Renvoie les attributs physiques associés aux catalogues accessibles depuis le DBMS.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="4eeb0-129">(CATALOGS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-132">2 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-132">2</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-133">Renvoie les jeux de caractères définis dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4eeb0-134">(CHARACTER_SETS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-139">5 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-139">5</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-140">Renvoie les contraintes de contrôle définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-141">(CHECK_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-146">3 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-146">3</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-147">Renvoie les collations de caractères définies dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4eeb0-148">(COLLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-153">13 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-153">13</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-154">Renvoie les privilèges des colonnes des tables définies dans le catalogue,  accordés à un utilisateur donné, ou accordés par ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4eeb0-155">(COLUMN_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-158">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="4eeb0-160">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="4eeb0-160">GRANTOR</span></span><br />
<span data-ttu-id="4eeb0-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-163">4 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-163">4</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-164">Renvoie les colonnes des tables (vues comprises) définies dans le catalogue et accessibles à un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4eeb0-165">(COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-168">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-171">11</span><span class="sxs-lookup"><span data-stu-id="4eeb0-171">11</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-172">Renvoie les colonnes définies dans le catalogue et qui dépendent d'un domaine défini dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4eeb0-173">(COLUMN_DOMAIN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="4eeb0-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-179">6 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-179">6</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-180">Renvoie les colonnes utilisées par les contraintes référentielles, uniques et de contrôle, ainsi que par les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4eeb0-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-184">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-187">7 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-187">7</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-188">Renvoie les tables utilisées par les contraintes référentielles, uniques et de contrôle, ainsi que par les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="4eeb0-189">(CONSTRAINT_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-194">32</span><span class="sxs-lookup"><span data-stu-id="4eeb0-194">32</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-195">Renvoie des informations sur les cubes disponibles dans un schéma (ou catalogue, si le fournisseur ne prend pas en charge les schémas).</span><span class="sxs-lookup"><span data-stu-id="4eeb0-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="4eeb0-196">(CUBES Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-201">30</span><span class="sxs-lookup"><span data-stu-id="4eeb0-201">30</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-202">Renvoie la liste des mots réservés spécifiques aux fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="4eeb0-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-204">&lt;Aucun&gt;</span><span class="sxs-lookup"><span data-stu-id="4eeb0-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-206">31</span><span class="sxs-lookup"><span data-stu-id="4eeb0-206">31</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-207">Renvoie la liste des chaînes littérales spécifiques aux fournisseurs et utilisées dans les commandes texte.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="4eeb0-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-209">&lt;Aucun&gt;</span><span class="sxs-lookup"><span data-stu-id="4eeb0-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-211">33</span><span class="sxs-lookup"><span data-stu-id="4eeb0-211">33</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-212">Renvoie des informations sur les dimensions d'un cube donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="4eeb0-213">Chaque dimension possède sa ligne propre.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-213">It has one row for each dimension.</span></span> <span data-ttu-id="4eeb0-214">(DIMENSIONS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-217">CUBE_NAME</span></span><br />
<span data-ttu-id="4eeb0-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="4eeb0-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-221">27</span><span class="sxs-lookup"><span data-stu-id="4eeb0-221">27</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-222">Renvoie les colonnes de clés étrangères définies dans le catalogue par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="4eeb0-223">(FOREIGN_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-231">34</span><span class="sxs-lookup"><span data-stu-id="4eeb0-231">34</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-232">Renvoie des informations sur les hiérarchies disponibles dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="4eeb0-233">(HIERARCHIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-236">CUBE_NAME</span></span><br />
<span data-ttu-id="4eeb0-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="4eeb0-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-241">12 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-241">12</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-242">Renvoie les index définis dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-243">(INDEXES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-246">INDEX_NAME</span></span><br />
<span data-ttu-id="4eeb0-247">TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-247">TYPE</span></span><br />
<span data-ttu-id="4eeb0-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-250">8 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-250">8</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-251">Renvoie les colonnes définies dans le catalogue et qui sont contraintes sous forme de clés par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="4eeb0-252">(KEY_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="4eeb0-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-258">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-261">35</span><span class="sxs-lookup"><span data-stu-id="4eeb0-261">35</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-262">Renvoie des informations sur les niveaux disponibles dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="4eeb0-263">(LEVELS Rowset\*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-266">CUBE_NAME</span></span><br />
<span data-ttu-id="4eeb0-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="4eeb0-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-272">36</span><span class="sxs-lookup"><span data-stu-id="4eeb0-272">36</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-273">Renvoie des informations sur les mesures disponibles.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-273">Returns information about the available measures.</span></span> <span data-ttu-id="4eeb0-274">(MEASURES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-277">CUBE_NAME</span></span><br />
<span data-ttu-id="4eeb0-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="4eeb0-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-281">38</span><span class="sxs-lookup"><span data-stu-id="4eeb0-281">38</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-282">Renvoie des informations sur les membres disponibles.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-282">Returns information about the available members.</span></span> <span data-ttu-id="4eeb0-283">(MEMBERS Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-286">CUBE_NAME</span></span><br />
<span data-ttu-id="4eeb0-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="4eeb0-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="4eeb0-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="4eeb0-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="4eeb0-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="4eeb0-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="4eeb0-295">Opérateur d’arborescence (pour plus d’informations, voir la documentation OLE DB pour OLAP.)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-297">28</span><span class="sxs-lookup"><span data-stu-id="4eeb0-297">28</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-298">Renvoie les colonnes de clés primaires définies dans le catalogue par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="4eeb0-299">(PRIMARY_KEYS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-304">29</span><span class="sxs-lookup"><span data-stu-id="4eeb0-304">29</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-305">Renvoie des informations sur les colonnes de jeux de lignes renvoyées par des procédures.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="4eeb0-306">(PROCEDURE_COLUMNS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4eeb0-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-312">26</span><span class="sxs-lookup"><span data-stu-id="4eeb0-312">26</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-313">Renvoie des informations sur les paramètres et les codes de retour des procédures.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="4eeb0-314">(PROCEDURE_PARAMETERS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4eeb0-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-320">16 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-320">16</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-321">Renvoie les procédures définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-322">(PROCEDURES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="4eeb0-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-328">37</span><span class="sxs-lookup"><span data-stu-id="4eeb0-328">37</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-329">Renvoie des informations sur les propriétés disponibles pour chaque niveau de la dimension.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="4eeb0-330">(PROPERTIES Rowset \*)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-333">CUBE_NAME</span></span><br />
<span data-ttu-id="4eeb0-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="4eeb0-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="4eeb0-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-341">-1</span><span class="sxs-lookup"><span data-stu-id="4eeb0-341">-1</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-342">Utilisé si le fournisseur définit ses propres requêtes de schéma non standard.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-343">&lt;Spécifique au fournisseur&gt;</span><span class="sxs-lookup"><span data-stu-id="4eeb0-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-345">22</span><span class="sxs-lookup"><span data-stu-id="4eeb0-345">22</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-346">Renvoie les types de données (primaires) pris en charge par le fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="4eeb0-347">(PROVIDER_TYPES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-348">DATA_TYPE</span></span><br />
<span data-ttu-id="4eeb0-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="4eeb0-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-351">9 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-351">9</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-352">Renvoie les contraintes référentielles définies dans le catalogie et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-353">(REFERENTIAL_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-358">17 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-358">17</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-359">Renvoie les schémas (objets de la base de données) dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-360">(SCHEMATA Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="4eeb0-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="4eeb0-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="4eeb0-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-365">18 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-365">18</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-366">Renvoie les niveaux de conformité, les options et les dialectes pris en charge par les données de traitement d'implémentation SQL définies dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="4eeb0-367">(SQL_LANGUAGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-368">&lt;Aucun&gt;</span><span class="sxs-lookup"><span data-stu-id="4eeb0-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-370">19</span><span class="sxs-lookup"><span data-stu-id="4eeb0-370">19</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-371">Renvoie les statistiques définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-372">(STATISTICS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-377">10 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-377">10</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-378">Renvoie les contraintes de table définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="4eeb0-379">(TABLE_CONSTRAINTS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="4eeb0-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-385">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-388">14 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-388">14</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-389">Renvoie les privilèges sur les tables définies dans le catalogue et qui sont disponibles pour un utilisateur donné, ou accordés par ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4eeb0-390">(TABLE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-393">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-394">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="4eeb0-394">GRANTOR</span></span><br />
<span data-ttu-id="4eeb0-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-397">20</span><span class="sxs-lookup"><span data-stu-id="4eeb0-397">20</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-398">Renvoie les tables (notamment les vues) définies dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4eeb0-399">(TABLES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-402">TABLE_NAME</span></span><br />
<span data-ttu-id="4eeb0-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-405"> 21</span><span class="sxs-lookup"><span data-stu-id="4eeb0-405">21</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-406">Renvoie les conversions de caractères définies dans le catalogue et auxquelles un utilisateur donné a accès.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4eeb0-407">(TRANSLATIONS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-412">39</span><span class="sxs-lookup"><span data-stu-id="4eeb0-412">39</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-413">Réservé pour usage ultérieur.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-415">15 </span><span class="sxs-lookup"><span data-stu-id="4eeb0-415">15</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-416">Renvoie les privilèges USAGE sur les objets définis dans le catalogue et qui sont disponibles pour un utilisateur donné, ou accordés par ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="4eeb0-417">(USAGE_PRIVILEGES Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="4eeb0-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="4eeb0-422">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="4eeb0-422">GRANTOR</span></span><br />
<span data-ttu-id="4eeb0-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-425">24</span><span class="sxs-lookup"><span data-stu-id="4eeb0-425">24</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-426">Renvoie les colonnes desquelles dépendent les tables vues, définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="4eeb0-427">(VIEW_COLUMN_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-432">23</span><span class="sxs-lookup"><span data-stu-id="4eeb0-432">23</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-433">Renvoie les vues définies dans le catalogue et accessibles par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="4eeb0-434">(VIEWS Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="4eeb0-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="4eeb0-439">25</span><span class="sxs-lookup"><span data-stu-id="4eeb0-439">25</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-440">Renvoie les tables desquelles dépendent les tables vues, définies dans le catalogue et dont est propriétaire un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="4eeb0-441">(VIEW_TABLE_USAGE Rowset)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="4eeb0-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="4eeb0-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="4eeb0-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="4eeb0-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="4eeb0-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4eeb0-445">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4eeb0-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="4eeb0-446">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4eeb0-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4eeb0-447">Constante</span><span class="sxs-lookup"><span data-stu-id="4eeb0-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="4eeb0-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="4eeb0-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="4eeb0-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eeb0-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="4eeb0-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eeb0-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="4eeb0-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

