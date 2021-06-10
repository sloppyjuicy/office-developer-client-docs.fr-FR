---
title: Fournisseur Microsoft OLE DB pour le service d'indexation Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba27bfdf6cc1317b441e626c61784e2c50b589f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288917"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="c9f7d-102">Fournisseur Microsoft OLE DB pour le service d’indexation Microsoft</span><span class="sxs-lookup"><span data-stu-id="c9f7d-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="c9f7d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9f7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9f7d-104">Le fournisseur Microsoft OLE DB pour le service d’indexation Microsoft fournit un accès en lecture seule par programme au système de fichiers et aux données web indexées par le service d’indexation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-104">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="c9f7d-105">Les applications ADO peuvent émettre des requêtes SQL pour extraire du contenu et des informations sur les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="c9f7d-106">Le fournisseur est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="c9f7d-107">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="c9f7d-107">Connection String Parameters</span></span>

<span data-ttu-id="c9f7d-108">Pour vous connecter à ce fournisseur, définissez l’argument **Provider=** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="c9f7d-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="c9f7d-109">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="c9f7d-110">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="c9f7d-110">Typical Connection String</span></span>

<span data-ttu-id="c9f7d-111">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="c9f7d-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="c9f7d-112">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="c9f7d-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9f7d-113">Mot clé</span><span class="sxs-lookup"><span data-stu-id="c9f7d-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="c9f7d-114">Description</span><span class="sxs-lookup"><span data-stu-id="c9f7d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="c9f7d-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-p102">Spécifie le fournisseur OLE DB pour le service d'indexation Microsoft. Ce mot clé est généralement le seul spécifié dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-118"><strong>Source des données</strong></span><span class="sxs-lookup"><span data-stu-id="c9f7d-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-p103">Spécifie le nom du catalogue du service d'indexation. Si ce mot clé n'est pas spécifié, le catalogue système par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-121"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="c9f7d-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-p104">Spécifie un nombre unique 32 bits (par exemple, 1033) qui indique les préférences relatives à la langue de l'utilisateur. Ces préférences décrivent le format de la date et de l'heure, l'ordre alphabétique utilisé pour trier les éléments, le mode de comparaison des chaînes, et ainsi de suite. Si ce mot clé n'est pas spécifié, l'identificateur des paramètres régionaux par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="c9f7d-125">Texte de la commande</span><span class="sxs-lookup"><span data-stu-id="c9f7d-125">Command Text</span></span>

<span data-ttu-id="c9f7d-p105">La syntaxe des requêtes SQL du service d'indexation est constituée d'extensions de l'instruction SQL-92 **SELECT** et des clauses **FROM** et **WHERE** associées. Les résultats de la requête sont renvoyés via des ensembles de lignes OLE DB, qui peuvent être utilisés par ADO et traités comme des objets [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c9f7d-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="c9f7d-p106">Vous pouvez rechercher des mots ou des phrases exacts ou utiliser des caractères génériques pour rechercher un modèle ou le radical d'un mot. La logique de recherche peut être basée sur des décisions booléennes, des termes pondérés ou la proximité d'autres mots. Vous pouvez également effectuer une recherche en « texte libre » : les correspondances trouvées seront dans ce cas basées non plus sur des mots exacts mais sur la signification.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="c9f7d-131">Le fournisseur n’accepte pas les appels de procédures stockées ni les noms de table simples (par exemple, la propriété [CommandType](commandtype-property-ado.md) sera toujours **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="c9f7d-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="c9f7d-132">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="c9f7d-132">Recordset Behavior</span></span>

<span data-ttu-id="c9f7d-133">Les tableaux suivants répertorient les fonctionnalités disponibles pour un objet **Recordset** ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="c9f7d-134">Seul le type de curseur statique (**adOpenStatic**) est disponible.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="c9f7d-135">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection [Properties](properties-collection-ado.md) du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="c9f7d-136">Disponibilité des propriétés ADO standard d'un **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="c9f7d-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9f7d-137">Propriété</span><span class="sxs-lookup"><span data-stu-id="c9f7d-137">Property</span></span></p></th>
<th><p><span data-ttu-id="c9f7d-138">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="c9f7d-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-140">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-142">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-144">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-146">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-147"><a href="bookmark-property-ado.md">Signet</a>\*</span><span class="sxs-lookup"><span data-stu-id="c9f7d-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="c9f7d-148">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-150">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-152">Toujours <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="c9f7d-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-153"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-154">Toujours <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="c9f7d-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-156">Toujours <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="c9f7d-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-158">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-159"><a href="filter-property-ado.md">Filtre</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-160">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-161"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-162">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-164">Non disponible</span><span class="sxs-lookup"><span data-stu-id="c9f7d-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-166">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-168">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-170">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-172">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-173"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-174">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c9f7d-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-175"><a href="state-property-ado.md">État</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-176">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-177"><a href="status-property-ado-recordset.md">État</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-178">lecture seule</span><span class="sxs-lookup"><span data-stu-id="c9f7d-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9f7d-179">\*Les signets doivent être activés sur le fournisseur pour que cette fonctionnalité existe sur le **recordset**.</span><span class="sxs-lookup"><span data-stu-id="c9f7d-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="c9f7d-180">Disponibilité des méthodes ADO standard d'un **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="c9f7d-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9f7d-181">Méthode</span><span class="sxs-lookup"><span data-stu-id="c9f7d-181">Method</span></span></p></th>
<th><p><span data-ttu-id="c9f7d-182">Disponible ?</span><span class="sxs-lookup"><span data-stu-id="c9f7d-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-184">Non</span><span class="sxs-lookup"><span data-stu-id="c9f7d-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-185"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-186">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-188">Non</span><span class="sxs-lookup"><span data-stu-id="c9f7d-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-190">Non</span><span class="sxs-lookup"><span data-stu-id="c9f7d-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-192">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-194">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-195"><a href="delete-method-ado-recordset.md">Supprimer</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-196">Non</span><span class="sxs-lookup"><span data-stu-id="c9f7d-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-197"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-198">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-199"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-200">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-202">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-204">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-206">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-207"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-208">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-209"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-210">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-211"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-212">Oui</span><span class="sxs-lookup"><span data-stu-id="c9f7d-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9f7d-213"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-214">Non</span><span class="sxs-lookup"><span data-stu-id="c9f7d-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9f7d-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="c9f7d-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="c9f7d-216">Non</span><span class="sxs-lookup"><span data-stu-id="c9f7d-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c9f7d-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9f7d-217">See also</span></span>

<span data-ttu-id="c9f7d-218">Pour obtenir des détails spécifiques d’implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour le service d’indexation Microsoft, consultez le guide Microsoft OLE DB Programmer’s Reference (en anglais).</span><span class="sxs-lookup"><span data-stu-id="c9f7d-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

