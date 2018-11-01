---
title: Index des propriétés dynamiques ADO
TOCTitle: ADO Dynamic Property Index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f385f3637f9a64ff94d571345d88fbaa088d126
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876063"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="ba847-102">Index des propriétés dynamiques ADO</span><span class="sxs-lookup"><span data-stu-id="ba847-102">ADO Dynamic Property Index</span></span>


<span data-ttu-id="ba847-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba847-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba847-p101">Les fournisseurs de données, les fournisseurs de services et les composants de services peuvent ajouter des propriétés dynamiques aux collections **Properties** des objets [Connection](connection-object-ado.md) et [Recordset](recordset-object-ado.md) non ouverts. Un fournisseur donné peut également insérer des propriétés supplémentaires lors de l'ouverture de ces objets. Certaines de ces propriétés apparaissent dans la section [Propriétés dynamiques ADO](ado-dynamic-properties.md). D'autres sont répertoriées dans la section [Annexe A : Fournisseurs](appendix-a-providers.md) sous les fournisseurs concernés.</span><span class="sxs-lookup"><span data-stu-id="ba847-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="ba847-p102">Le tableau suivant est un index croisé des noms ADO et OLE DB pour chaque propriété dynamique standard de fournisseur OLE DB. Vos fournisseurs peuvent ajouter d'autres propriétés non répertoriées ici. Pour obtenir des informations spécifiques sur les propriétés dynamiques d'un fournisseur particulier, consultez la documentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ba847-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="ba847-p103">Le guide OLE DB Programmer's Reference (en anglais) référence les noms des propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés standard. Recherchez le nom de propriété OLE DB dans l'index ou consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ba847-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

  - <span data-ttu-id="ba847-114">Appendix C: OLE DB Properties</span><span class="sxs-lookup"><span data-stu-id="ba847-114">Appendix C: OLE DB Properties</span></span>

  - <span data-ttu-id="ba847-115">Supported Properties of the Cursor Service</span><span class="sxs-lookup"><span data-stu-id="ba847-115">Supported Properties of the Cursor Service</span></span>

  - <span data-ttu-id="ba847-116">Supported Properties of the Persistence Provider</span><span class="sxs-lookup"><span data-stu-id="ba847-116">Supported Properties of the Persistence Provider</span></span>

  - <span data-ttu-id="ba847-117">Supported OLE DB Properties of the Remoting Provider</span><span class="sxs-lookup"><span data-stu-id="ba847-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="ba847-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba847-118">Remarks</span></span>

<span data-ttu-id="ba847-119">Notez les numéros utilisés dans l'index croisé :</span><span class="sxs-lookup"><span data-stu-id="ba847-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="ba847-p104">(1) Cette propriété est un indicateur booléen indiquant si l'interface nommée doit être utilisée. Le nom de propriété OLE DB équivalent est répertorié s'il existe.</span><span class="sxs-lookup"><span data-stu-id="ba847-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="ba847-122">(2) la propriété ADO « Bookmarkable » est généré en interne pour descendante compatibilité et est mappé à la propriété OLE DB, DBPROP\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="ba847-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="ba847-123">Il s'agit de la même propriété que celle correspondant à la propriété ADO IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="ba847-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="ba847-124">(3) Le nom de propriété ADO Hidden Columns est différent du nom utilisé pour la description du nom de propriété OLE DB (Hidden Columns Count).</span><span class="sxs-lookup"><span data-stu-id="ba847-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="ba847-p106">(4) Pour les jeux d'enregistrements hiérarchiques, la propriété ADO Maximum Rows est appliquée à tous les enfants. Selon l'ordre dans lequel les lignes sont renvoyées, vous pouvez obtenir dans les résultats tous les enfants, certains enfants ou aucun enfant pour chaque parent ou les enfants orphelins. Par conséquent, lors de la modification des jeux d'enregistrements hiérarchiques, l'identificateur de chaque enfant doit être unique. En général le fournisseur [Microsoft Data Shaping Service pour OLE DB (MSDATASHAPE) ](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) n'autorise pas de distinction entre les propriétés qui peuvent être héritées du parent et celles qui ne peuvent pas être héritées.</span><span class="sxs-lookup"><span data-stu-id="ba847-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="ba847-129">(5) Non applicable.</span><span class="sxs-lookup"><span data-stu-id="ba847-129">(5) Does not apply.</span></span>

<span data-ttu-id="ba847-130">**Propriétés dynamiques de connexion**</span><span class="sxs-lookup"><span data-stu-id="ba847-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba847-131">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="ba847-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ba847-132">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="ba847-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba847-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="ba847-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="ba847-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="ba847-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="ba847-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="ba847-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="ba847-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="ba847-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="ba847-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="ba847-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="ba847-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="ba847-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="ba847-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="ba847-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="ba847-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="ba847-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="ba847-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="ba847-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="ba847-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="ba847-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="ba847-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="ba847-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="ba847-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="ba847-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ba847-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="ba847-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="ba847-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="ba847-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="ba847-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="ba847-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="ba847-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="ba847-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="ba847-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="ba847-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="ba847-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ba847-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ba847-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="ba847-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="ba847-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="ba847-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="ba847-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="ba847-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="ba847-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="ba847-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="ba847-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="ba847-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="ba847-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="ba847-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="ba847-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="ba847-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="ba847-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="ba847-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="ba847-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="ba847-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="ba847-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="ba847-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="ba847-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ba847-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="ba847-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="ba847-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="ba847-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="ba847-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="ba847-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="ba847-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="ba847-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="ba847-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="ba847-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-177">Location</span><span class="sxs-lookup"><span data-stu-id="ba847-177">Location</span></span></p></td>
<td><p><span data-ttu-id="ba847-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="ba847-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="ba847-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="ba847-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="ba847-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="ba847-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="ba847-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="ba847-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="ba847-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="ba847-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="ba847-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="ba847-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="ba847-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="ba847-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-187">Mode</span><span class="sxs-lookup"><span data-stu-id="ba847-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="ba847-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="ba847-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="ba847-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="ba847-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="ba847-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="ba847-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="ba847-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="ba847-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ba847-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ba847-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ba847-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="ba847-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="ba847-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="ba847-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="ba847-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="ba847-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="ba847-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="ba847-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="ba847-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ba847-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="ba847-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="ba847-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="ba847-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="ba847-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="ba847-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="ba847-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="ba847-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="ba847-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ba847-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="ba847-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="ba847-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="ba847-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="ba847-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="ba847-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="ba847-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="ba847-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="ba847-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="ba847-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="ba847-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="ba847-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="ba847-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-215">Password</span><span class="sxs-lookup"><span data-stu-id="ba847-215">Password</span></span></p></td>
<td><p><span data-ttu-id="ba847-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="ba847-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="ba847-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="ba847-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="ba847-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="ba847-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="ba847-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="ba847-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="ba847-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="ba847-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ba847-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="ba847-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="ba847-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ba847-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="ba847-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="ba847-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="ba847-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="ba847-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="ba847-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="ba847-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="ba847-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="ba847-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="ba847-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="ba847-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="ba847-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="ba847-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="ba847-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="ba847-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="ba847-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="ba847-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="ba847-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="ba847-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="ba847-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="ba847-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="ba847-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="ba847-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="ba847-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="ba847-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="ba847-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="ba847-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="ba847-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="ba847-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="ba847-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="ba847-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="ba847-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="ba847-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="ba847-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="ba847-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="ba847-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="ba847-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="ba847-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="ba847-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="ba847-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="ba847-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="ba847-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="ba847-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-253">User ID</span><span class="sxs-lookup"><span data-stu-id="ba847-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="ba847-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="ba847-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-255">User Name</span><span class="sxs-lookup"><span data-stu-id="ba847-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="ba847-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="ba847-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="ba847-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="ba847-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="ba847-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ba847-259">**Propriétés dynamiques du jeu d'enregistrements**</span><span class="sxs-lookup"><span data-stu-id="ba847-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="ba847-260">Notez que les **propriétés dynamiques** de l'objet **Recordset** deviennent inaccessibles (non disponibles) lorsque le **Recordset** est fermé.</span><span class="sxs-lookup"><span data-stu-id="ba847-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba847-261">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="ba847-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ba847-262">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="ba847-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba847-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="ba847-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="ba847-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="ba847-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="ba847-266">(1)</span><span class="sxs-lookup"><span data-stu-id="ba847-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ba847-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="ba847-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ba847-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="ba847-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ba847-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="ba847-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="ba847-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="ba847-274">(1)</span><span class="sxs-lookup"><span data-stu-id="ba847-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="ba847-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="ba847-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="ba847-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="ba847-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="ba847-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="ba847-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="ba847-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="ba847-282">(1)</span><span class="sxs-lookup"><span data-stu-id="ba847-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ba847-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="ba847-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="ba847-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="ba847-286">(1)</span><span class="sxs-lookup"><span data-stu-id="ba847-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="ba847-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="ba847-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ba847-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="ba847-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ba847-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="ba847-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ba847-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="ba847-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="ba847-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="ba847-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="ba847-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="ba847-298">(1)</span><span class="sxs-lookup"><span data-stu-id="ba847-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="ba847-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="ba847-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ba847-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="ba847-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="ba847-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="ba847-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="ba847-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="ba847-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ba847-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="ba847-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="ba847-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="ba847-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-311">IStream</span><span class="sxs-lookup"><span data-stu-id="ba847-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="ba847-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ba847-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="ba847-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="ba847-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="ba847-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="ba847-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="ba847-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="ba847-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="ba847-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="ba847-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="ba847-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="ba847-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="ba847-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="ba847-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="ba847-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="ba847-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="ba847-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="ba847-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="ba847-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="ba847-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="ba847-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="ba847-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="ba847-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="ba847-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="ba847-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ba847-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ba847-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ba847-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="ba847-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="ba847-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="ba847-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="ba847-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="ba847-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="ba847-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="ba847-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="ba847-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ba847-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="ba847-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="ba847-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="ba847-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="ba847-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="ba847-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ba847-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="ba847-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="ba847-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="ba847-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="ba847-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="ba847-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="ba847-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ba847-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="ba847-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="ba847-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="ba847-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="ba847-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="ba847-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="ba847-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="ba847-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="ba847-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ba847-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="ba847-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="ba847-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ba847-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="ba847-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="ba847-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="ba847-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="ba847-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="ba847-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="ba847-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="ba847-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="ba847-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="ba847-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="ba847-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="ba847-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="ba847-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ba847-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ba847-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ba847-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="ba847-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ba847-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ba847-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="ba847-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="ba847-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="ba847-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="ba847-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="ba847-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="ba847-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="ba847-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="ba847-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="ba847-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="ba847-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="ba847-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="ba847-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="ba847-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="ba847-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="ba847-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="ba847-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ba847-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ba847-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ba847-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ba847-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ba847-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="ba847-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ba847-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ba847-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ba847-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ba847-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ba847-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="ba847-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="ba847-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="ba847-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ba847-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="ba847-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="ba847-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ba847-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-403">Private1</span><span class="sxs-lookup"><span data-stu-id="ba847-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="ba847-404">(5)</span><span class="sxs-lookup"><span data-stu-id="ba847-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="ba847-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="ba847-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="ba847-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="ba847-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="ba847-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="ba847-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="ba847-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="ba847-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="ba847-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="ba847-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="ba847-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="ba847-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="ba847-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="ba847-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="ba847-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="ba847-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="ba847-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="ba847-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="ba847-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="ba847-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="ba847-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="ba847-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="ba847-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="ba847-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ba847-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="ba847-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="ba847-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ba847-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ba847-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="ba847-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="ba847-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="ba847-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="ba847-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="ba847-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="ba847-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="ba847-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="ba847-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="ba847-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="ba847-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ba847-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="ba847-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="ba847-446">DONNEZ</span><span class="sxs-lookup"><span data-stu-id="ba847-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ba847-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ba847-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="ba847-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="ba847-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ba847-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ba847-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="ba847-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="ba847-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="ba847-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="ba847-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="ba847-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="ba847-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="ba847-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="ba847-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="ba847-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="ba847-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="ba847-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="ba847-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="ba847-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="ba847-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="ba847-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="ba847-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="ba847-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="ba847-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba847-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="ba847-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="ba847-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="ba847-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba847-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ba847-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ba847-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ba847-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

