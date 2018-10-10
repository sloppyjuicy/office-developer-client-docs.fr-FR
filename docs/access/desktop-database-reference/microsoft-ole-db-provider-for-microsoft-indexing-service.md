---
title: Fournisseur Microsoft OLE DB pour le service d'indexation Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10af40231fc10e222f818896b3d65f44ac3d6d71
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470340"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="e2f22-102">Fournisseur Microsoft OLE DB pour le service d'indexation Microsoft</span><span class="sxs-lookup"><span data-stu-id="e2f22-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="e2f22-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2f22-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e2f22-p101">Le fournisseur Microsoft OLE DB pour le service d'indexation Microsoft fournit un accès en lecture seule par programmation au système de fichier et aux données Web indexées par le service d'indexation de Microsoft. Les applications ADO peuvent émettre des requêtes SQL pour extraire du contenu et des informations sur les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2f22-p101">The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and Web data indexed by Microsoft Indexing Service. ADO applications can issue SQL queries to retrieve content and file property information.</span></span>

<span data-ttu-id="e2f22-106">Le fournisseur est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2f22-106">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="e2f22-107">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="e2f22-107">Connection String Parameters</span></span>

<span data-ttu-id="e2f22-108">Pour vous connecter à ce fournisseur, définissez l'argument **Provider=** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="e2f22-108">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="e2f22-109">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e2f22-109">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="e2f22-110">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="e2f22-110">Typical Connection String</span></span>

<span data-ttu-id="e2f22-111">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="e2f22-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="e2f22-112">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="e2f22-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2f22-113">Mot clé</span><span class="sxs-lookup"><span data-stu-id="e2f22-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="e2f22-114">Description</span><span class="sxs-lookup"><span data-stu-id="e2f22-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="e2f22-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="e2f22-p102">Spécifie le fournisseur OLE DB pour le service d'indexation Microsoft. Ce mot clé est généralement le seul spécifié dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="e2f22-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-118"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="e2f22-118"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="e2f22-p103">Spécifie le nom du catalogue du service d'indexation. Si ce mot clé n'est pas spécifié, le catalogue système par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e2f22-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-121"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="e2f22-121"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="e2f22-p104">Spécifie un nombre unique 32 bits (par exemple, 1033) qui indique les préférences relatives à la langue de l'utilisateur. Ces préférences décrivent le format de la date et de l'heure, l'ordre alphabétique utilisé pour trier les éléments, le mode de comparaison des chaînes, et ainsi de suite. Si ce mot clé n'est pas spécifié, l'identificateur des paramètres régionaux par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e2f22-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="e2f22-125">Texte de la commande</span><span class="sxs-lookup"><span data-stu-id="e2f22-125">Command Text</span></span>

<span data-ttu-id="e2f22-p105">La syntaxe des requêtes SQL du service d'indexation est constituée d'extensions de l'instruction SQL-92 **SELECT** et des clauses **FROM** et **WHERE** associées. Les résultats de la requête sont renvoyés via des ensembles de lignes OLE DB, qui peuvent être utilisés par ADO et traités comme des objets [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e2f22-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="e2f22-p106">Vous pouvez rechercher des mots ou des phrases exacts ou utiliser des caractères génériques pour rechercher un modèle ou le radical d'un mot. La logique de recherche peut être basée sur des décisions booléennes, des termes pondérés ou la proximité d'autres mots. Vous pouvez également effectuer une recherche en « texte libre » : les correspondances trouvées seront dans ce cas basées non plus sur des mots exacts mais sur la signification.</span><span class="sxs-lookup"><span data-stu-id="e2f22-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="e2f22-131">Le fournisseur n’accepte pas les appels de procédures stockées ni les noms de table simples (par exemple, la propriété [CommandType](commandtype-property-ado.md) sera toujours **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="e2f22-131">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="e2f22-132">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="e2f22-132">Recordset Behavior</span></span>

<span data-ttu-id="e2f22-133">Les tableaux suivants répertorient les fonctionnalités disponibles pour un objet **Recordset** ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e2f22-133">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="e2f22-134">Le type de curseur statique (**adOpenStatic**) est disponible.</span><span class="sxs-lookup"><span data-stu-id="e2f22-134">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="e2f22-135">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection [Properties](properties-collection-ado.md) du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e2f22-135">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="e2f22-136">Disponibilité des propriétés ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="e2f22-136">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2f22-137">Propriété</span><span class="sxs-lookup"><span data-stu-id="e2f22-137">Property</span></span></p></th>
<th><p><span data-ttu-id="e2f22-138">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="e2f22-138">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-139"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-140">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-140">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-141"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-142">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-143"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-144">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-145"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-145"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-146">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-147"><a href="bookmark-property-ado.md">Signet</a>\*</span><span class="sxs-lookup"><span data-stu-id="e2f22-147"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="e2f22-148">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-148">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-149"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-149"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-150">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-151"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-152">Toujours <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="e2f22-152">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-153"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-153"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-154">Toujours <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="e2f22-154">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-156">Toujours <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="e2f22-156">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-157"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-157"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-158">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-159"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-160">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-160">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-161"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-161"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-162">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-162">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-163"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-164">non disponible</span><span class="sxs-lookup"><span data-stu-id="e2f22-164">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-165"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-166">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-166">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-167"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-167"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-168">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-168">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-169"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-169"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-170">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-170">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-171"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-171"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-172">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-172">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-173"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-173"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-174">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e2f22-174">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-175"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-175"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-176">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-176">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-177"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-177"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-178">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2f22-178">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2f22-179">\*Signets doivent être activés sur le fournisseur afin que cette fonctionnalité existe sur le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e2f22-179">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="e2f22-180">Disponibilité des méthodes ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="e2f22-180">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2f22-181">Méthode</span><span class="sxs-lookup"><span data-stu-id="e2f22-181">Method</span></span></p></th>
<th><p><span data-ttu-id="e2f22-182">Disponible ?</span><span class="sxs-lookup"><span data-stu-id="e2f22-182">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-183"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-183"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-184">Non</span><span class="sxs-lookup"><span data-stu-id="e2f22-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-185"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-185"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-186">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-187"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-188">Non</span><span class="sxs-lookup"><span data-stu-id="e2f22-188">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-189"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-190">Non</span><span class="sxs-lookup"><span data-stu-id="e2f22-190">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-191"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-191"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-192">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-192">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-193"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-193"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-194">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-194">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-195"><a href="delete-method-ado-recordset.md">Supprimer</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-195"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-196">Non</span><span class="sxs-lookup"><span data-stu-id="e2f22-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-197"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-197"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-198">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-199"><a href="move-method-ado.md">Déplacer</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-199"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-200">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-200">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-201"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-202">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-202">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-203"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-204">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-205"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-205"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-206">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-207"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-207"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-208">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-208">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-209"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-209"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-210">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-211"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-211"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-212">Oui</span><span class="sxs-lookup"><span data-stu-id="e2f22-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2f22-213"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-213"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-214">Non</span><span class="sxs-lookup"><span data-stu-id="e2f22-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2f22-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="e2f22-215"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e2f22-216">Non</span><span class="sxs-lookup"><span data-stu-id="e2f22-216">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e2f22-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2f22-217">See also</span></span>

<span data-ttu-id="e2f22-218">Pour plus d’informations spécifiques à l’implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour le Service d’indexation Microsoft, consultez la référence du programmeur Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e2f22-218">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

