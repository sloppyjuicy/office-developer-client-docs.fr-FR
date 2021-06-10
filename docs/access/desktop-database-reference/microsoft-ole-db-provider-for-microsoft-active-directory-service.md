---
title: Fournisseur Microsoft OLE DB pour le service Microsoft Active Directory
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23e1cab32fee6103a046219a7cda8c90f02d9f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288938"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a><span data-ttu-id="cb120-102">Fournisseur Microsoft OLE DB pour Microsoft Active Directory Service</span><span class="sxs-lookup"><span data-stu-id="cb120-102">Microsoft OLE DB Provider for Microsoft Active Directory Service</span></span>

<span data-ttu-id="cb120-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb120-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb120-p101">Le fournisseur ADSI (Microsoft Active Directory Service Interfaces) permet à ADO de se connecter à des services d'annuaire hétérogènes via ADSI. Les applications ADO bénéficient ainsi d'un accès en lecture seule aux services d'annuaire de Microsoft Windows NT 4.0 et de Microsoft Windows 2000, ainsi qu'aux services d'annuaire Novell ou compatibles avec LDAP. ADSI est basé sur un modèle de fournisseur ; par conséquent, si un nouveau fournisseur donne accès à un autre annuaire, l'application ADO pourra y accéder de façon transparente. Le fournisseur ADSI est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb120-p101">The Microsoft Active Directory Service Interfaces (ADSI) Provider allows ADO to connect to heterogeneous directory services through ADSI. This gives ADO applications read-only access to the Microsoft Windows NT 4.0 and Microsoft Windows 2000 directory services, in addition to any LDAP-compliant directory service and Novell Directory Services. ADSI itself is based on a provider model, so if there is a new provider giving access to another directory, the ADO application will be able to access it seamlessly. The ADSI provider is free-threaded and unicode enabled.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="cb120-108">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="cb120-108">Connection String Parameters</span></span>

<span data-ttu-id="cb120-109">Pour vous connecter à ce fournisseur, définissez l’argument **Provider** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="cb120-109">To connect to this provider, set the **Provider** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
ADSDSOObject 
```

<span data-ttu-id="cb120-110">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="cb120-110">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="cb120-111">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="cb120-111">Typical Connection String</span></span>

<span data-ttu-id="cb120-112">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="cb120-112">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="cb120-113">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="cb120-113">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb120-114">Mot clé</span><span class="sxs-lookup"><span data-stu-id="cb120-114">Keyword</span></span></p></th>
<th><p><span data-ttu-id="cb120-115">Description</span><span class="sxs-lookup"><span data-stu-id="cb120-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb120-116"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="cb120-116"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="cb120-117">Spécifie le fournisseur OLE DB pour le service Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb120-117">Specifies the OLE DB Provider for Microsoft Active Directory Service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-118"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="cb120-118"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="cb120-p102">Spécifie le nom de l'utilisateur. Si ce mot clé n'est pas spécifié, les paramètres de connexion actuels sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="cb120-p102">Specifies the user name. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="cb120-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="cb120-p103">Spécifie le mot de passe de l'utilisateur. Si ce mot clé n'est pas spécifié, les paramètres de connexion actuels sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="cb120-p103">Specifies the user password. If this keyword is omitted, then the current logon is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb120-124">**Texte de la commande**</span><span class="sxs-lookup"><span data-stu-id="cb120-124">**Command Text**</span></span>

<span data-ttu-id="cb120-125">Dans la syntaxe suivante, une chaîne de texte de commande en quatre parties est reconnue par le fournisseur :</span><span class="sxs-lookup"><span data-stu-id="cb120-125">A four-part command text string is recognized by the provider in the following syntax:</span></span>

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb120-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb120-126">Value</span></span></p></th>
<th><p><span data-ttu-id="cb120-127">Description</span><span class="sxs-lookup"><span data-stu-id="cb120-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb120-128"><em>Root</em></span><span class="sxs-lookup"><span data-stu-id="cb120-128"><em>Root</em></span></span></p></td>
<td><p><span data-ttu-id="cb120-129">Indique l'objet <strong>ADsPath</strong> à partir duquel lancer la recherche (c'est-à-dire la racine de la recherche).</span><span class="sxs-lookup"><span data-stu-id="cb120-129">Indicates the <strong>ADsPath</strong> object from which to start the search (that is, the root of the search).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-130"><em>Filtre</em></span><span class="sxs-lookup"><span data-stu-id="cb120-130"><em>Filter</em></span></span></p></td>
<td><p><span data-ttu-id="cb120-131">Indique le filtre de recherche au format RFC 1960.</span><span class="sxs-lookup"><span data-stu-id="cb120-131">Indicates the search filter in the RFC 1960 format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-132"><em>Attributs</em></span><span class="sxs-lookup"><span data-stu-id="cb120-132"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="cb120-133">Indique une liste délimitée par des virgules d'attributs à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="cb120-133">Indicates a comma-delimited list of attributes to be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-134"><em>Scope</em></span><span class="sxs-lookup"><span data-stu-id="cb120-134"><em>Scope</em></span></span></p></td>
<td><p><span data-ttu-id="cb120-135">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="cb120-135">Optional.</span></span> <span data-ttu-id="cb120-136"><strong>Chaîne</strong> spécifiant l'étendue de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cb120-136">A <strong>String</strong> that specifies the scope of the search.</span></span> <span data-ttu-id="cb120-137">Il peut s’agit de l’une des opérations suivantes : Base — Rechercher uniquement l’objet de base (racine de la recherche).</span><span class="sxs-lookup"><span data-stu-id="cb120-137">Can be one of the following: Base — Search only the base object (root of the search).</span></span><br />
<span data-ttu-id="cb120-138">OneLevel : recherchez un seul niveau.</span><span class="sxs-lookup"><span data-stu-id="cb120-138">OneLevel — Search only one level.</span></span><br />
<span data-ttu-id="cb120-139">Sous-arbre : recherchez l’intégralité de la sous-arbre.</span><span class="sxs-lookup"><span data-stu-id="cb120-139">Subtree — Search the entire subtree.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb120-140">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cb120-140">For example:</span></span>

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

<span data-ttu-id="cb120-p105">Le fournisseur prend aussi en charge SQL SELECT pour le texte de commande. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cb120-p105">The provider also supports SQL SELECT for command text. For example:</span></span>

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

<span data-ttu-id="cb120-p106">Le fournisseur n’accepte pas les appels de procédures stockées ni les noms de table simples (par exemple, la propriété [CommandType](commandtype-property-ado.md) sera toujours **adCmdText**). Pour obtenir une description plus complète des éléments du texte de commande, consultez la documentation ADSI.</span><span class="sxs-lookup"><span data-stu-id="cb120-p106">The provider does not accept stored procedure calls or simple table names (for example, the [CommandType](commandtype-property-ado.md) property will always be **adCmdText**). See the Active Directory Service Interfaces documentation for a more complete description of the command text elements.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="cb120-145">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="cb120-145">Recordset Behavior</span></span>

<span data-ttu-id="cb120-146">Les tableaux suivants répertorient les fonctionnalités disponibles pour un objet [Recordset](recordset-object-ado.md) ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cb120-146">The following tables list the features available on a [Recordset](recordset-object-ado.md) object opened with this provider.</span></span> <span data-ttu-id="cb120-147">Seul le type de curseur statique (**adOpenStatic**) est disponible.</span><span class="sxs-lookup"><span data-stu-id="cb120-147">Only the Static cursor type (**adOpenStatic**) is available.</span></span>

<span data-ttu-id="cb120-148">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection [Properties](properties-collection-ado.md) du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cb120-148">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the [Properties](properties-collection-ado.md) collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="cb120-149">Disponibilité des propriétés ADO standard d'un **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="cb120-149">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb120-150">Propriété</span><span class="sxs-lookup"><span data-stu-id="cb120-150">Property</span></span></p></th>
<th><p><span data-ttu-id="cb120-151">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="cb120-151">Availability</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb120-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="cb120-152"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-153">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-153">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="cb120-154"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-155">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-155">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="cb120-156"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-157">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-157">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-158"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="cb120-158"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-159">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-159">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-160"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="cb120-160"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-161">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-161">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-162"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="cb120-162"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-163">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-163">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="cb120-164"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-165">Toujours <strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="cb120-165">always <strong>adUseServer</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-166"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="cb120-166"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-167">Toujours <strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="cb120-167">always <strong>adOpenStatic</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-168"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="cb120-168"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-169">Toujours <strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="cb120-169">always <strong>adEditNone</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-170"><a href="bof-eof-properties-ado.md">EOF</a></span><span class="sxs-lookup"><span data-stu-id="cb120-170"><a href="bof-eof-properties-ado.md">EOF</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-171">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-171">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-172"><a href="filter-property-ado.md">Filtre</a></span><span class="sxs-lookup"><span data-stu-id="cb120-172"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-173">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-173">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-174"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="cb120-174"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-175">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-175">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="cb120-176"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-177">Non disponible</span><span class="sxs-lookup"><span data-stu-id="cb120-177">not available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="cb120-178"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-179">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-179">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-180"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="cb120-180"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-181">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-181">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-182"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="cb120-182"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-183">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-183">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-184"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="cb120-184"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-185">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-185">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-186"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="cb120-186"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-187">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb120-187">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-188"><a href="state-property-ado.md">État</a></span><span class="sxs-lookup"><span data-stu-id="cb120-188"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-189">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-189">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-190"><a href="status-property-ado-recordset.md">État</a></span><span class="sxs-lookup"><span data-stu-id="cb120-190"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-191">lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb120-191">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb120-192">Disponibilité des méthodes ADO standard d'un **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="cb120-192">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb120-193">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb120-193">Method</span></span></p></th>
<th><p><span data-ttu-id="cb120-194">Disponible ?</span><span class="sxs-lookup"><span data-stu-id="cb120-194">Available?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb120-195"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="cb120-195"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-196">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-196">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-197"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="cb120-197"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-198">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-198">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="cb120-199"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-200">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-200">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="cb120-201"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-202">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-202">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-203"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="cb120-203"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-204">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-205"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="cb120-205"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-206">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-206">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-207"><a href="delete-method-ado-recordset.md">Supprimer</a></span><span class="sxs-lookup"><span data-stu-id="cb120-207"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-208">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-209"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="cb120-209"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-210">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-210">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-211"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="cb120-211"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-212">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-212">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="cb120-213"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-214">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-214">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="cb120-215"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-216">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-216">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="cb120-217"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-218">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-218">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="cb120-219"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-220">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-220">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="cb120-221"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-222">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-222">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-223"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="cb120-223"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-224">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-224">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-225"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="cb120-225"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-226">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-226">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-227"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="cb120-227"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-228">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-228">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-229"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="cb120-229"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-230">Oui</span><span class="sxs-lookup"><span data-stu-id="cb120-230">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb120-231"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="cb120-231"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-232">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-232">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb120-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="cb120-233"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="cb120-234">Non</span><span class="sxs-lookup"><span data-stu-id="cb120-234">No</span></span></p></td>
</tr>
</tbody>
</table>

