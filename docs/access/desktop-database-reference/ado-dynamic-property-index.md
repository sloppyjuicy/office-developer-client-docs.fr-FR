---
title: Index des propriétés dynamiques ADO
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19b7ddca0395869b5a1dba4182a123d33e54e66d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947601"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="64fe3-102">Index des propriétés dynamiques ADO</span><span class="sxs-lookup"><span data-stu-id="64fe3-102">ADO dynamic property index</span></span>

<span data-ttu-id="64fe3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64fe3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64fe3-p101">Les fournisseurs de données, les fournisseurs de services et les composants de services peuvent ajouter des propriétés dynamiques aux collections **Properties** des objets [Connection](connection-object-ado.md) et [Recordset](recordset-object-ado.md) non ouverts. Un fournisseur donné peut également insérer des propriétés supplémentaires lors de l'ouverture de ces objets. Certaines de ces propriétés apparaissent dans la section [Propriétés dynamiques ADO](ado-dynamic-properties.md). D'autres sont répertoriées dans la section [Annexe A : Fournisseurs](appendix-a-providers.md) sous les fournisseurs concernés.</span><span class="sxs-lookup"><span data-stu-id="64fe3-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="64fe3-p102">Le tableau suivant est un index croisé des noms ADO et OLE DB pour chaque propriété dynamique standard de fournisseur OLE DB. Vos fournisseurs peuvent ajouter d'autres propriétés non répertoriées ici. Pour obtenir des informations spécifiques sur les propriétés dynamiques d'un fournisseur particulier, consultez la documentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64fe3-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="64fe3-p103">Le guide OLE DB Programmer's Reference (en anglais) référence les noms des propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés standard. Recherchez le nom de propriété OLE DB dans l'index ou consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="64fe3-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="64fe3-114">Appendix C: OLE DB Properties</span><span class="sxs-lookup"><span data-stu-id="64fe3-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="64fe3-115">Supported Properties of the Cursor Service</span><span class="sxs-lookup"><span data-stu-id="64fe3-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="64fe3-116">Supported Properties of the Persistence Provider</span><span class="sxs-lookup"><span data-stu-id="64fe3-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="64fe3-117">Supported OLE DB Properties of the Remoting Provider</span><span class="sxs-lookup"><span data-stu-id="64fe3-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="64fe3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="64fe3-118">Remarks</span></span>

<span data-ttu-id="64fe3-119">Notez les numéros utilisés dans l'index croisé :</span><span class="sxs-lookup"><span data-stu-id="64fe3-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="64fe3-p104">(1) Cette propriété est un indicateur booléen indiquant si l'interface nommée doit être utilisée. Le nom de propriété OLE DB équivalent est répertorié s'il existe.</span><span class="sxs-lookup"><span data-stu-id="64fe3-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="64fe3-122">(2) la propriété ADO « Bookmarkable » est généré en interne pour descendante compatibilité et est mappé à la propriété OLE DB, DBPROP\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="64fe3-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="64fe3-123">Il s'agit de la même propriété que celle correspondant à la propriété ADO IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="64fe3-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="64fe3-124">(3) Le nom de propriété ADO Hidden Columns est différent du nom utilisé pour la description du nom de propriété OLE DB (Hidden Columns Count).</span><span class="sxs-lookup"><span data-stu-id="64fe3-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="64fe3-p106">(4) Pour les jeux d'enregistrements hiérarchiques, la propriété ADO Maximum Rows est appliquée à tous les enfants. Selon l'ordre dans lequel les lignes sont renvoyées, vous pouvez obtenir dans les résultats tous les enfants, certains enfants ou aucun enfant pour chaque parent ou les enfants orphelins. Par conséquent, lors de la modification des jeux d'enregistrements hiérarchiques, l'identificateur de chaque enfant doit être unique. En général le fournisseur [Microsoft Data Shaping Service pour OLE DB (MSDATASHAPE) ](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) n'autorise pas de distinction entre les propriétés qui peuvent être héritées du parent et celles qui ne peuvent pas être héritées.</span><span class="sxs-lookup"><span data-stu-id="64fe3-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="64fe3-129">(5) Non applicable.</span><span class="sxs-lookup"><span data-stu-id="64fe3-129">(5) Does not apply.</span></span>

<span data-ttu-id="64fe3-130">**Propriétés dynamiques de connexion**</span><span class="sxs-lookup"><span data-stu-id="64fe3-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64fe3-131">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="64fe3-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="64fe3-132">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="64fe3-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="64fe3-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="64fe3-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="64fe3-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="64fe3-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="64fe3-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="64fe3-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="64fe3-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="64fe3-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="64fe3-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="64fe3-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="64fe3-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="64fe3-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="64fe3-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="64fe3-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="64fe3-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="64fe3-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="64fe3-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="64fe3-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="64fe3-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="64fe3-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="64fe3-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="64fe3-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="64fe3-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="64fe3-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="64fe3-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="64fe3-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="64fe3-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="64fe3-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="64fe3-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="64fe3-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="64fe3-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="64fe3-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="64fe3-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="64fe3-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="64fe3-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="64fe3-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="64fe3-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="64fe3-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="64fe3-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="64fe3-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="64fe3-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="64fe3-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="64fe3-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="64fe3-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="64fe3-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="64fe3-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="64fe3-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="64fe3-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="64fe3-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="64fe3-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="64fe3-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="64fe3-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="64fe3-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="64fe3-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="64fe3-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="64fe3-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64fe3-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="64fe3-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="64fe3-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="64fe3-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="64fe3-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="64fe3-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="64fe3-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="64fe3-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="64fe3-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="64fe3-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-177">Location</span><span class="sxs-lookup"><span data-stu-id="64fe3-177">Location</span></span></p></td>
<td><p><span data-ttu-id="64fe3-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="64fe3-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="64fe3-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="64fe3-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="64fe3-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="64fe3-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="64fe3-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="64fe3-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="64fe3-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="64fe3-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="64fe3-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="64fe3-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="64fe3-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="64fe3-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-187">Mode</span><span class="sxs-lookup"><span data-stu-id="64fe3-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="64fe3-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="64fe3-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="64fe3-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="64fe3-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="64fe3-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="64fe3-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="64fe3-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="64fe3-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="64fe3-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="64fe3-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="64fe3-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="64fe3-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="64fe3-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="64fe3-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="64fe3-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="64fe3-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="64fe3-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="64fe3-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="64fe3-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="64fe3-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="64fe3-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="64fe3-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="64fe3-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="64fe3-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="64fe3-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="64fe3-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="64fe3-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="64fe3-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="64fe3-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="64fe3-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="64fe3-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="64fe3-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="64fe3-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="64fe3-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="64fe3-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="64fe3-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="64fe3-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="64fe3-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-215">Password</span><span class="sxs-lookup"><span data-stu-id="64fe3-215">Password</span></span></p></td>
<td><p><span data-ttu-id="64fe3-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="64fe3-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="64fe3-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="64fe3-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="64fe3-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="64fe3-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="64fe3-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="64fe3-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="64fe3-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="64fe3-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="64fe3-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="64fe3-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="64fe3-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="64fe3-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="64fe3-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="64fe3-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="64fe3-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="64fe3-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="64fe3-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="64fe3-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="64fe3-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="64fe3-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="64fe3-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="64fe3-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="64fe3-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="64fe3-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="64fe3-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="64fe3-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="64fe3-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="64fe3-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="64fe3-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="64fe3-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="64fe3-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="64fe3-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="64fe3-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="64fe3-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="64fe3-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="64fe3-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="64fe3-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="64fe3-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="64fe3-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="64fe3-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="64fe3-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="64fe3-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="64fe3-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="64fe3-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="64fe3-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="64fe3-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="64fe3-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="64fe3-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="64fe3-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="64fe3-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="64fe3-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="64fe3-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="64fe3-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="64fe3-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-253">User ID</span><span class="sxs-lookup"><span data-stu-id="64fe3-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="64fe3-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="64fe3-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-255">User Name</span><span class="sxs-lookup"><span data-stu-id="64fe3-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="64fe3-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="64fe3-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="64fe3-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="64fe3-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="64fe3-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64fe3-259">**Propriétés dynamiques du jeu d'enregistrements**</span><span class="sxs-lookup"><span data-stu-id="64fe3-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="64fe3-260">Notez que les **propriétés dynamiques** de l'objet **Recordset** deviennent inaccessibles (non disponibles) lorsque le **Recordset** est fermé.</span><span class="sxs-lookup"><span data-stu-id="64fe3-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64fe3-261">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="64fe3-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="64fe3-262">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="64fe3-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="64fe3-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="64fe3-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="64fe3-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="64fe3-266">(1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="64fe3-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="64fe3-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="64fe3-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="64fe3-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="64fe3-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="64fe3-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="64fe3-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="64fe3-274">(1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="64fe3-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="64fe3-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="64fe3-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="64fe3-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="64fe3-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="64fe3-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="64fe3-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="64fe3-282">(1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="64fe3-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="64fe3-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="64fe3-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="64fe3-286">(1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="64fe3-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="64fe3-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="64fe3-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="64fe3-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="64fe3-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="64fe3-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="64fe3-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="64fe3-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="64fe3-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="64fe3-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="64fe3-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="64fe3-298">(1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="64fe3-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="64fe3-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="64fe3-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="64fe3-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="64fe3-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="64fe3-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="64fe3-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="64fe3-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="64fe3-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="64fe3-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="64fe3-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="64fe3-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-311">IStream</span><span class="sxs-lookup"><span data-stu-id="64fe3-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="64fe3-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="64fe3-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="64fe3-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="64fe3-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="64fe3-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="64fe3-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="64fe3-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="64fe3-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="64fe3-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="64fe3-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="64fe3-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="64fe3-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="64fe3-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="64fe3-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="64fe3-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="64fe3-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="64fe3-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="64fe3-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="64fe3-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="64fe3-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="64fe3-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="64fe3-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="64fe3-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="64fe3-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="64fe3-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="64fe3-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="64fe3-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="64fe3-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="64fe3-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="64fe3-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="64fe3-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="64fe3-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="64fe3-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="64fe3-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="64fe3-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="64fe3-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="64fe3-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="64fe3-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="64fe3-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="64fe3-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="64fe3-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="64fe3-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="64fe3-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="64fe3-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="64fe3-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="64fe3-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="64fe3-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="64fe3-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="64fe3-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="64fe3-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="64fe3-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="64fe3-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="64fe3-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="64fe3-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="64fe3-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="64fe3-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="64fe3-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="64fe3-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="64fe3-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="64fe3-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="64fe3-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="64fe3-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="64fe3-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="64fe3-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="64fe3-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="64fe3-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="64fe3-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="64fe3-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="64fe3-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="64fe3-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="64fe3-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="64fe3-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="64fe3-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="64fe3-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="64fe3-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="64fe3-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="64fe3-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="64fe3-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="64fe3-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="64fe3-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="64fe3-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="64fe3-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="64fe3-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="64fe3-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="64fe3-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="64fe3-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="64fe3-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="64fe3-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="64fe3-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="64fe3-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="64fe3-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="64fe3-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="64fe3-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="64fe3-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="64fe3-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="64fe3-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="64fe3-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="64fe3-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="64fe3-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="64fe3-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="64fe3-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="64fe3-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="64fe3-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="64fe3-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="64fe3-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="64fe3-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="64fe3-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="64fe3-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="64fe3-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="64fe3-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="64fe3-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="64fe3-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-403">Private1</span><span class="sxs-lookup"><span data-stu-id="64fe3-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="64fe3-404">(5)</span><span class="sxs-lookup"><span data-stu-id="64fe3-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="64fe3-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="64fe3-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="64fe3-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="64fe3-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="64fe3-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="64fe3-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="64fe3-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="64fe3-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="64fe3-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="64fe3-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="64fe3-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="64fe3-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="64fe3-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="64fe3-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="64fe3-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="64fe3-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="64fe3-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="64fe3-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="64fe3-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="64fe3-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="64fe3-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="64fe3-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="64fe3-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="64fe3-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="64fe3-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="64fe3-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="64fe3-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="64fe3-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="64fe3-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="64fe3-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="64fe3-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="64fe3-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="64fe3-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="64fe3-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="64fe3-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="64fe3-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="64fe3-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="64fe3-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="64fe3-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="64fe3-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="64fe3-446">DONNEZ</span><span class="sxs-lookup"><span data-stu-id="64fe3-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="64fe3-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="64fe3-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="64fe3-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="64fe3-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="64fe3-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="64fe3-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="64fe3-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="64fe3-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="64fe3-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="64fe3-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="64fe3-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="64fe3-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="64fe3-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="64fe3-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="64fe3-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="64fe3-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="64fe3-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="64fe3-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="64fe3-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="64fe3-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="64fe3-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="64fe3-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="64fe3-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="64fe3-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fe3-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="64fe3-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="64fe3-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="64fe3-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fe3-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="64fe3-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="64fe3-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="64fe3-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

