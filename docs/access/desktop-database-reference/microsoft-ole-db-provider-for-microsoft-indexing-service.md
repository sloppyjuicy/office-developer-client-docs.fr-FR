---
title: Fournisseur Microsoft OLE DB pour le service d'indexation Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e41633ddb2730af66ddeee400ad035d5a17ed90d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607052"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a><span data-ttu-id="f00e7-102">Fournisseur Microsoft OLE DB pour le service d'indexation Microsoft</span><span class="sxs-lookup"><span data-stu-id="f00e7-102">Microsoft OLE DB Provider for Microsoft Indexing Service</span></span>


<span data-ttu-id="f00e7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f00e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f00e7-104"><<<<<<< Tête le fournisseur Microsoft OLE DB pour le Service d’indexation Microsoft fournit l’accès en lecture seule par programme à un système de fichiers et des données Web indexées par le Service d’indexation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f00e7-104"><<<<<<< HEAD The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and Web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="f00e7-105">Les applications ADO peuvent émettre des requêtes SQL pour extraire du contenu et des informations sur les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="f00e7-105">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>
<span data-ttu-id="f00e7-106">=== Le fournisseur Microsoft OLE DB pour le Service d’indexation Microsoft fournit l’accès en lecture seule par programme aux données de web et le système de fichiers indexés par le Service d’indexation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f00e7-106">======= The Microsoft OLE DB Provider for Microsoft Indexing Service provides programmatic read-only access to file system and web data indexed by Microsoft Indexing Service.</span></span> <span data-ttu-id="f00e7-107">Les applications ADO peuvent émettre des requêtes SQL pour extraire du contenu et des informations sur les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="f00e7-107">ADO applications can issue SQL queries to retrieve content and file property information.</span></span>
>>>>>>> <span data-ttu-id="f00e7-108">master</span><span class="sxs-lookup"><span data-stu-id="f00e7-108">master</span></span>

<span data-ttu-id="f00e7-109">Le fournisseur est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="f00e7-109">The provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="f00e7-110">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="f00e7-110">Connection String Parameters</span></span>

<span data-ttu-id="f00e7-111">Pour vous connecter à ce fournisseur, définissez l'argument **Provider=** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="f00e7-111">To connect to this provider, set the **Provider=** argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSIDXS 
```

<span data-ttu-id="f00e7-112">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="f00e7-112">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="f00e7-113">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="f00e7-113">Typical Connection String</span></span>

<span data-ttu-id="f00e7-114">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="f00e7-114">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

<span data-ttu-id="f00e7-115">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="f00e7-115">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f00e7-116">Mot clé</span><span class="sxs-lookup"><span data-stu-id="f00e7-116">Keyword</span></span></p></th>
<th><p><span data-ttu-id="f00e7-117">Description</span><span class="sxs-lookup"><span data-stu-id="f00e7-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-118"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="f00e7-118"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="f00e7-p102">Spécifie le fournisseur OLE DB pour le service d'indexation Microsoft. Ce mot clé est généralement le seul spécifié dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="f00e7-p102">Specifies the OLE DB Provider for Microsoft Indexing Service. Typically this is the only keyword specified in the connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-121"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="f00e7-121"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="f00e7-p103">Spécifie le nom du catalogue du service d'indexation. Si ce mot clé n'est pas spécifié, le catalogue système par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f00e7-p103">Specifies the Indexing Service catalog name. If this keyword is not specified, the default system catalog is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-124"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="f00e7-124"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="f00e7-p104">Spécifie un nombre unique 32 bits (par exemple, 1033) qui indique les préférences relatives à la langue de l'utilisateur. Ces préférences décrivent le format de la date et de l'heure, l'ordre alphabétique utilisé pour trier les éléments, le mode de comparaison des chaînes, et ainsi de suite. Si ce mot clé n'est pas spécifié, l'identificateur des paramètres régionaux par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f00e7-p104">Specifies a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on. If this keyword is not specified, the default system locale identifier is used.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="f00e7-128">Texte de la commande</span><span class="sxs-lookup"><span data-stu-id="f00e7-128">Command Text</span></span>

<span data-ttu-id="f00e7-p105">La syntaxe des requêtes SQL du service d'indexation est constituée d'extensions de l'instruction SQL-92 **SELECT** et des clauses **FROM** et **WHERE** associées. Les résultats de la requête sont renvoyés via des ensembles de lignes OLE DB, qui peuvent être utilisés par ADO et traités comme des objets [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f00e7-p105">The Indexing Service SQL query syntax consists of extensions to the SQL-92 **SELECT** statement and its **FROM** and **WHERE** clauses. The results of the query are returned via OLE DB rowsets, which can be consumed by ADO and manipulated as [Recordset](recordset-object-ado.md) objects.</span></span>

<span data-ttu-id="f00e7-p106">Vous pouvez rechercher des mots ou des phrases exacts ou utiliser des caractères génériques pour rechercher un modèle ou le radical d'un mot. La logique de recherche peut être basée sur des décisions booléennes, des termes pondérés ou la proximité d'autres mots. Vous pouvez également effectuer une recherche en « texte libre » : les correspondances trouvées seront dans ce cas basées non plus sur des mots exacts mais sur la signification.</span><span class="sxs-lookup"><span data-stu-id="f00e7-p106">You can search for exact words or phrases, or use wildcards to search for patterns or stems of words. The search logic can be based on Boolean decisions, weighted terms, or proximity to other words. You can also search by "free text," which finds matches based on meaning, rather than exact words.</span></span>

<span data-ttu-id="f00e7-134">Le fournisseur n’accepte pas les appels de procédures stockées ni les noms de table simples (par exemple, la propriété [CommandType](commandtype-property-ado.md) sera toujours **adCmdText**).</span><span class="sxs-lookup"><span data-stu-id="f00e7-134">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**).</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="f00e7-135">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="f00e7-135">Recordset Behavior</span></span>

<span data-ttu-id="f00e7-136">Les tableaux suivants répertorient les fonctionnalités disponibles pour un objet **Recordset** ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f00e7-136">The following tables list the features available with a **Recordset** object opened with this provider.</span></span> <span data-ttu-id="f00e7-137">Le type de curseur statique (**adOpenStatic**) est disponible.</span><span class="sxs-lookup"><span data-stu-id="f00e7-137">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="f00e7-138">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection [Properties](properties-collection-ado.md) du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f00e7-138">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="f00e7-139">Disponibilité des propriétés ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="f00e7-139">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f00e7-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="f00e7-140">Property</span></span></p></th>
<th><p><span data-ttu-id="f00e7-141">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="f00e7-141">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-142"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-142"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-143">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-144"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-144"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-145">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-145">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-146"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-146"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-147">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-148"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-148"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-149">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-149">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-150"><a href="bookmark-property-ado.md">Signet</a>\*</span><span class="sxs-lookup"><span data-stu-id="f00e7-150"><a href="bookmark-property-ado.md">Bookmark</a>\*</span></span></p></td>
<td><p><span data-ttu-id="f00e7-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-151">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-152"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-152"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-153">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-153">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-154"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-154"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-155">Toujours <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="f00e7-155">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-156"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-156"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-157">Toujours <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="f00e7-157">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-158"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-158"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-159">Toujours <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="f00e7-159">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-160"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-160"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-161">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-161">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-162"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-162"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-163">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-163">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-164"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-164"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-165">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-165">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-166"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-166"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-167">non disponible</span><span class="sxs-lookup"><span data-stu-id="f00e7-167">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-168"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-168"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-169">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-169">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-170"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-170"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-171">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-171">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-172"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-172"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-173">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-173">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-174"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-174"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-175">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-175">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-176"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-176"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-177">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f00e7-177">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-178"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-178"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-179">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-179">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-180"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-180"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-181">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f00e7-181">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f00e7-182">\*Signets doivent être activés sur le fournisseur afin que cette fonctionnalité existe sur le **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f00e7-182">\*Bookmarks must be enabled on the provider in order for this feature to exist on the **Recordset**.</span></span>

<span data-ttu-id="f00e7-183">Disponibilité des méthodes ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="f00e7-183">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f00e7-184">Méthode</span><span class="sxs-lookup"><span data-stu-id="f00e7-184">Method</span></span></p></th>
<th><p><span data-ttu-id="f00e7-185">Disponible ?</span><span class="sxs-lookup"><span data-stu-id="f00e7-185">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-186"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-186"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-187">Non</span><span class="sxs-lookup"><span data-stu-id="f00e7-187">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-188"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-188"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-189">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-189">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-190"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-190"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-191">Non</span><span class="sxs-lookup"><span data-stu-id="f00e7-191">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-192"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-192"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-193">Non</span><span class="sxs-lookup"><span data-stu-id="f00e7-193">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-194"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-194"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-195">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-195">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-196"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-196"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-197">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-197">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-198"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-198"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-199">Non</span><span class="sxs-lookup"><span data-stu-id="f00e7-199">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-200"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-200"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-201">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-201">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-202"><a href="move-method-ado.md">Déplacer</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-202"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-203">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-204"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-204"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-205">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-206"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-206"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-207">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-207">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-208"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-208"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-209">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-209">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-210"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-210"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-211">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-211">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-212"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-212"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-213">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-213">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-214"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-214"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-215">Oui</span><span class="sxs-lookup"><span data-stu-id="f00e7-215">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00e7-216"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-216"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-217">Non</span><span class="sxs-lookup"><span data-stu-id="f00e7-217">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00e7-218"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="f00e7-218"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="f00e7-219">Non</span><span class="sxs-lookup"><span data-stu-id="f00e7-219">No</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f00e7-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f00e7-220">See also</span></span>

<span data-ttu-id="f00e7-221">Pour plus d’informations spécifiques à l’implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour le Service d’indexation Microsoft, consultez la référence du programmeur Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f00e7-221">For specific implementation details and functional information about the Microsoft OLE DB Provider for Microsoft Indexing Service, consult the Microsoft OLE DB Programmer's Reference.</span></span>

