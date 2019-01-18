---
title: Fournisseur Microsoft OLE DB pour Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712840"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a><span data-ttu-id="d583c-102">Fournisseur Microsoft OLE DB pour Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="d583c-102">Microsoft OLE DB Provider for Microsoft Jet</span></span>

<span data-ttu-id="d583c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d583c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d583c-104">Le fournisseur OLE pour Microsoft Jet permet à ADO d'accéder aux bases de données Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="d583c-104">The OLE DB Provider for Microsoft Jet allows ADO to access Microsoft Jet databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="d583c-105">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="d583c-105">Connection String Parameters</span></span>

<span data-ttu-id="d583c-106">Pour vous connecter à ce fournisseur, définissez l'argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="d583c-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

<span data-ttu-id="d583c-107">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d583c-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="d583c-108">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="d583c-108">Typical Connection String</span></span>

<span data-ttu-id="d583c-109">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="d583c-109">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="d583c-110">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="d583c-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d583c-111">Mot clé</span><span class="sxs-lookup"><span data-stu-id="d583c-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="d583c-112">Description</span><span class="sxs-lookup"><span data-stu-id="d583c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d583c-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="d583c-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d583c-114">Spécifie le fournisseur OLE DB pour Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="d583c-114">Specifies the OLE DB Provider for Microsoft Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="d583c-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="d583c-116">Spécifie le chemin d’accès à la base de données et le nom du fichier (par exemple, c:\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="d583c-116">Specifies the database path and file name (for example, c:\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-117"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="d583c-117"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="d583c-118">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d583c-118">Specifies the user name.</span></span> <span data-ttu-id="d583c-119">Si ce mot clé n’est pas spécifié, la chaîne, &quot;admin&quot;, est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="d583c-119">If this keyword is not specified, the string, &quot;admin&quot;, is used by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-120"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="d583c-120"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="d583c-121">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d583c-121">Specifies the user password.</span></span> <span data-ttu-id="d583c-122">Si ce mot clé n’est pas spécifié, une chaîne vide (&quot;&quot;), est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="d583c-122">If this keyword is not specified, the empty string (&quot;&quot;), is used by default.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="d583c-123">Paramètres de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="d583c-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="d583c-124">Le fournisseur OLE DB pour Microsoft Jet prend en charge plusieurs propriétés dynamiques spécifiques au fournisseur en plus de ceux définis par ADO.</span><span class="sxs-lookup"><span data-stu-id="d583c-124">The OLE DB Provider for Microsoft Jet supports several provider-specific dynamic properties in addition to those defined by ADO.</span></span> <span data-ttu-id="d583c-125">Comme avec tous les autres paramètres de **connexion** , elles peuvent être définies via la collection **Properties** de l’objet **Connection** ou dans le cadre de la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="d583c-125">As with all other **Connection** parameters, they can be set via the **Connection** object's **Properties** collection or as part of the connection string.</span></span>

<span data-ttu-id="d583c-126">Le tableau suivant répertorie ces propriétés en indiquant entre parenthèses le nom de la propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="d583c-126">The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d583c-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d583c-127">Parameter</span></span></p></th>
<th><p><span data-ttu-id="d583c-128">Description</span><span class="sxs-lookup"><span data-stu-id="d583c-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d583c-129">Quantité d’espace récupéré Jet OLEDB:Compact</span><span class="sxs-lookup"><span data-stu-id="d583c-129">Jet OLEDB:Compact Reclaimed Space Amount</span></span><br />
<span data-ttu-id="d583c-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span><span class="sxs-lookup"><span data-stu-id="d583c-130">(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p104">Donne une estimation en octets de l'espace qui peut être récupéré si la base de données est compactée. Cette valeur n'est valide qu'une fois établie la connexion à la base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-p104">Indicates an estimate of the amount of space, in bytes, that can be reclaimed by compacting the database. This value is only valid after a database connection has been established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-133">Contrôle de OLEDB:Connection Jet</span><span class="sxs-lookup"><span data-stu-id="d583c-133">Jet OLEDB:Connection Control</span></span><br />
<span data-ttu-id="d583c-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span><span class="sxs-lookup"><span data-stu-id="d583c-134">(DBPROP_JETOLEDB_CONNECTIONCONTROL)</span></span></p></td>
<td><p><span data-ttu-id="d583c-135">Indique si les utilisateurs peuvent se connecter à la base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-135">Indicates whether users can connect to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-136">Jet OLEDB : créer la base de données système</span><span class="sxs-lookup"><span data-stu-id="d583c-136">Jet OLEDB:Create System Database</span></span><br />
<span data-ttu-id="d583c-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span><span class="sxs-lookup"><span data-stu-id="d583c-137">(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-138">Indique si une base de données système doit être créée lorsqu'une nouvelle source de données est créée.</span><span class="sxs-lookup"><span data-stu-id="d583c-138">Indicates whether a system database should be created when creating a new data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-139">En Mode Verrouillage Jet OLEDB : Database</span><span class="sxs-lookup"><span data-stu-id="d583c-139">Jet OLEDB:Database Locking Mode</span></span><br />
<span data-ttu-id="d583c-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span><span class="sxs-lookup"><span data-stu-id="d583c-140">(DBPROP_JETOLEDB_DATABASELOCKMODE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p105">Indique le mode de verrouillage pour cette base de données. Le premier utilisateur ouvrant la base de données détermine le mode utilisé lorsque la base de données est ouverte.</span><span class="sxs-lookup"><span data-stu-id="d583c-p105">Indicates the locking mode for this database. The first user to open the database determines the mode used while the database is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-143">Jet OLEDB:Database Password</span><span class="sxs-lookup"><span data-stu-id="d583c-143">Jet OLEDB:Database Password</span></span><br />
<span data-ttu-id="d583c-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="d583c-144">(DBPROP_JETOLEDB_DATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="d583c-145">Indique le mot de passe de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-145">Indicates the database password.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-146">Jet OLEDB:Don’t Copy Locale on Compact</span><span class="sxs-lookup"><span data-stu-id="d583c-146">Jet OLEDB:Don't Copy Locale on Compact</span></span><br />
<span data-ttu-id="d583c-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span><span class="sxs-lookup"><span data-stu-id="d583c-147">(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-148">Indique si Jet doit copier les informations relatives aux paramètres régionaux lors du compactage d'une base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-148">Indicates whether Jet should copy locale information when compacting a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-149">Jet OLEDB:Encrypt Database</span><span class="sxs-lookup"><span data-stu-id="d583c-149">Jet OLEDB:Encrypt Database</span></span><br />
<span data-ttu-id="d583c-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span><span class="sxs-lookup"><span data-stu-id="d583c-150">(DBPROP_JETOLEDB_ENCRYPTDATABASE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p106">Indique si une base de données compactée doit être chiffrée. Lorsque cette propriété n'est pas définie, la base de données compactée est chiffrée si la base de données d'origine a également été chiffrée.</span><span class="sxs-lookup"><span data-stu-id="d583c-p106">Indicates whether a compacted database should be encrypted. If this property is not set, the compacted database will be encrypted if the original database was also encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-153">Jet OLEDB:Engine Type</span><span class="sxs-lookup"><span data-stu-id="d583c-153">Jet OLEDB:Engine Type</span></span><br />
<span data-ttu-id="d583c-154">(DBPROP_JETOLEDB_ENGINE)</span><span class="sxs-lookup"><span data-stu-id="d583c-154">(DBPROP_JETOLEDB_ENGINE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-155">Indique le moteur de stockage utilisé pour accéder au magasin de données actuel.</span><span class="sxs-lookup"><span data-stu-id="d583c-155">Indicates the storage engine used to access the current data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-156">Jet OLEDB:Exclusive Async Delay</span><span class="sxs-lookup"><span data-stu-id="d583c-156">Jet OLEDB:Exclusive Async Delay</span></span><br />
<span data-ttu-id="d583c-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="d583c-157">(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p107">Indique le délai maximal en millisecondes dont dispose Jet pour les écritures asynchrones sur le disque lorsque la base de données est ouverte en mode exclusif. Cette propriété est ignorée sauf si <strong>Jet OLEDB:Flush Transaction Timeout</strong> est défini sur 0.  </span><span class="sxs-lookup"><span data-stu-id="d583c-p107">Indicates the maximum length of time, in milliseconds, that Jet can delay asynchronous writes to disk when the database is opened exclusively. This property is ignored unless <strong>Jet OLEDB:Flush Transaction Timeout</strong> is set to 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-160">Jet OLEDB:Flush Transaction Timeout</span><span class="sxs-lookup"><span data-stu-id="d583c-160">Jet OLEDB:Flush Transaction Timeout</span></span><br />
<span data-ttu-id="d583c-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="d583c-161">(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p108">Indique le délai d'attente nécessaire pour que les données stockées en cache en vue d'une écriture asynchrone soient effectivement écrites sur le disque. Ce paramètre remplace les valeurs définies pour <strong>Jet OLEDB:Shared Async Delay</strong> et <strong>Jet OLEDB:Exclusive Async Delay</strong>.  </span><span class="sxs-lookup"><span data-stu-id="d583c-p108">Indicates the amount of time to wait before data stored in a cache for asynchronous writing is actually written to disk. This setting overrides the values for <strong>Jet OLEDB:Shared Async Delay</strong> and <strong>Jet OLEDB:Exclusive Async Delay</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-164">Jet OLEDB : Transactions Global en bloc</span><span class="sxs-lookup"><span data-stu-id="d583c-164">Jet OLEDB:Global Bulk Transactions</span></span><br />
<span data-ttu-id="d583c-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="d583c-165">(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="d583c-166">Indique si les transactions SQL en bloc sont traitées.</span><span class="sxs-lookup"><span data-stu-id="d583c-166">Indicates whether SQL bulk transactions are transacted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-167">Jet OLEDB : les opérations en bloc partiel globale</span><span class="sxs-lookup"><span data-stu-id="d583c-167">Jet OLEDB:Global Partial Bulk Ops</span></span><br />
<span data-ttu-id="d583c-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="d583c-168">(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="d583c-169">Indique le mot de passe utilisé pour ouvrir la base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-169">Indicates the password used to open the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-170">Jet OLEDB:Implicit Commit Sync</span><span class="sxs-lookup"><span data-stu-id="d583c-170">Jet OLEDB:Implicit Commit Sync</span></span><br />
<span data-ttu-id="d583c-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="d583c-171">(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="d583c-172">Indique si les modifications effectuées lors de transactions internes implicites sont écrites en mode synchrone ou en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d583c-172">Indicates whether changes made in internal implicit transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-173">Jet OLEDB:Lock Delay</span><span class="sxs-lookup"><span data-stu-id="d583c-173">Jet OLEDB:Lock Delay</span></span><br />
<span data-ttu-id="d583c-174">(DBPROP_JETOLEDB_LOCKDELAY)</span><span class="sxs-lookup"><span data-stu-id="d583c-174">(DBPROP_JETOLEDB_LOCKDELAY)</span></span></p></td>
<td><p><span data-ttu-id="d583c-175">Indique le délai d'attente nécessaire en millisecondes pour lancer une nouvelle tentative d'acquisition d'un verrou après échec d'une tentative précédente.</span><span class="sxs-lookup"><span data-stu-id="d583c-175">Indicates the number of milliseconds to wait before attempting to acquire a lock after a previous attempt has failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-176">Jet OLEDB:Lock Retry</span><span class="sxs-lookup"><span data-stu-id="d583c-176">Jet OLEDB:Lock Retry</span></span><br />
<span data-ttu-id="d583c-177">(DBPROP_JETOLEDB_LOCKRETRY)</span><span class="sxs-lookup"><span data-stu-id="d583c-177">(DBPROP_JETOLEDB_LOCKRETRY)</span></span></p></td>
<td><p><span data-ttu-id="d583c-178">Indique le nombre de répétitions d'une tentative d'accès à une page verrouillée.</span><span class="sxs-lookup"><span data-stu-id="d583c-178">Indicates how many times an attempt to access a locked page is repeated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-179">Jet OLEDB:Max Buffer Size</span><span class="sxs-lookup"><span data-stu-id="d583c-179">Jet OLEDB:Max Buffer Size</span></span><br />
<span data-ttu-id="d583c-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span><span class="sxs-lookup"><span data-stu-id="d583c-180">(DBPROP_JETOLEDB_MAXBUFFERSIZE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-181">Indique la quantité de mémoire maximum en kilo-octets que Jet peut utiliser avant de lancer une purge des modifications sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d583c-181">Indicates the maximum amount of memory, in kilobytes, Jet can use before it starts flushing changes to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-182">Jet OLEDB:Max Locks Per File</span><span class="sxs-lookup"><span data-stu-id="d583c-182">Jet OLEDB:Max Locks Per File</span></span><br />
<span data-ttu-id="d583c-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span><span class="sxs-lookup"><span data-stu-id="d583c-183">(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p109">Indique le nombre maximum de verrous que Jet peut placer sur une base de données. La valeur par défaut est 9500.</span><span class="sxs-lookup"><span data-stu-id="d583c-p109">Indicates the maximum number of locks Jet can place on a database. The default value is 9500.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-186">Jet OLEDB : nouveau mot de passe de base de données</span><span class="sxs-lookup"><span data-stu-id="d583c-186">Jet OLEDB:New Database Password</span></span><br />
<span data-ttu-id="d583c-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span><span class="sxs-lookup"><span data-stu-id="d583c-187">(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p110">Indique le nouveau mot de passe à définir pour cette base de données. L'ancien mot de passe est enregistré dans <strong>Jet OLEDB:Database Password</strong>.  </span><span class="sxs-lookup"><span data-stu-id="d583c-p110">Indicates the new password to be set for this database. The old password is stored in <strong>Jet OLEDB:Database Password</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-190">Command Time Out du Jet OLEDB : ODBC</span><span class="sxs-lookup"><span data-stu-id="d583c-190">Jet OLEDB:ODBC Command Time Out</span></span><br />
<span data-ttu-id="d583c-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="d583c-191">(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="d583c-192">Indique le délai d'expiration en millisecondes d'une requête ODBC distante en provenance de Jet.</span><span class="sxs-lookup"><span data-stu-id="d583c-192">Indicates the number of milliseconds before a remote ODBC query from Jet will timeout.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-193">Jet OLEDB:Page verrous au verrouillage de Table</span><span class="sxs-lookup"><span data-stu-id="d583c-193">Jet OLEDB:Page Locks to Table Lock</span></span><br />
<span data-ttu-id="d583c-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span><span class="sxs-lookup"><span data-stu-id="d583c-194">(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p111">Indique combien de pages doivent être verrouillées dans une transaction avant que Jet tente de promouvoir le verrouillage d'une table. Si cette valeur est égale à 0, le verrouillage n'est jamais promu.</span><span class="sxs-lookup"><span data-stu-id="d583c-p111">Indicates how many pages need to be locked within a transaction before Jet attempts to promote the lock to a table lock. If this value is 0, then the lock is never promoted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-197">Jet OLEDB:Page Timeout</span><span class="sxs-lookup"><span data-stu-id="d583c-197">Jet OLEDB:Page Timeout</span></span><br />
<span data-ttu-id="d583c-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="d583c-198">(DBPROP_JETOLEDB_PAGETIMEOUT)</span></span></p></td>
<td><p><span data-ttu-id="d583c-199">Indique le délai d'attente en millisecondes avant que Jet vérifie si son cache est obsolète pour le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-199">Indicates the number of milliseconds Jet will wait before checking to see if its cache is out of date with the database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-200">Jet OLEDB:Recycle Long-Valued Pages</span><span class="sxs-lookup"><span data-stu-id="d583c-200">Jet OLEDB:Recycle Long-Valued Pages</span></span><br />
<span data-ttu-id="d583c-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span><span class="sxs-lookup"><span data-stu-id="d583c-201">(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</span></span></p></td>
<td><p><span data-ttu-id="d583c-202">Indique si Jet doit essayer à tout prix de récupérer les pages BLOB lorsqu'elles sont libérées.</span><span class="sxs-lookup"><span data-stu-id="d583c-202">Indicates whether Jet should aggressively try to reclaim BLOB pages when they are freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-203">Jet OLEDB:Registry Path</span><span class="sxs-lookup"><span data-stu-id="d583c-203">Jet OLEDB:Registry Path</span></span><br />
<span data-ttu-id="d583c-204">(DBPROP_JETOLEDB_REGPATH)</span><span class="sxs-lookup"><span data-stu-id="d583c-204">(DBPROP_JETOLEDB_REGPATH)</span></span></p></td>
<td><p><span data-ttu-id="d583c-205">Indique la clé de Registre Windows qui contient des valeurs pour le moteur de base de données Jet.</span><span class="sxs-lookup"><span data-stu-id="d583c-205">Indicates the Windows registry key that contains values for the Jet database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-206">Jet OLEDB:Reset ISAM Stats</span><span class="sxs-lookup"><span data-stu-id="d583c-206">Jet OLEDB:Reset ISAM Stats</span></span><br />
<span data-ttu-id="d583c-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span><span class="sxs-lookup"><span data-stu-id="d583c-207">(DBPROP_JETOLEDB_RESETISAMSTATS)</span></span></p></td>
<td><p><span data-ttu-id="d583c-208">Indique si le schéma <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS doit réinitialiser ses compteurs de performance après le renvoi des informations de performance.</span><span class="sxs-lookup"><span data-stu-id="d583c-208">Indicates whether the schema <strong>Recordset</strong> DBSCHEMA_JETOLEDB_ISAMSTATS should reset its performance counters after returning performance information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-209">Jet OLEDB:Shared Async Delay</span><span class="sxs-lookup"><span data-stu-id="d583c-209">Jet OLEDB:Shared Async Delay</span></span><br />
<span data-ttu-id="d583c-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span><span class="sxs-lookup"><span data-stu-id="d583c-210">(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</span></span></p></td>
<td><p><span data-ttu-id="d583c-211">Indique le délai maximal en millisecondes dont dispose Jet pour les écritures asynchrones sur le disque lorsque la base de données est ouverte en mode multi-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d583c-211">Indicates the maximum amount of time, in milliseconds, Jet can delay asynchronous writes to disk when the database is opened in multi-user mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-212">Jet OLEDB:System Database</span><span class="sxs-lookup"><span data-stu-id="d583c-212">Jet OLEDB:System Database</span></span><br />
<span data-ttu-id="d583c-213">(DBPROP_JETOLEDB_SYSDBPATH)</span><span class="sxs-lookup"><span data-stu-id="d583c-213">(DBPROP_JETOLEDB_SYSDBPATH)</span></span></p></td>
<td><p><span data-ttu-id="d583c-214">Indique le chemin d'accès et le nom de fichier pour le fichier d'information de groupe de travail (base de données système).</span><span class="sxs-lookup"><span data-stu-id="d583c-214">Indicates the path and file name for the workgroup information file (system database).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-215">Mode de validation Jet OLEDB:Transaction</span><span class="sxs-lookup"><span data-stu-id="d583c-215">Jet OLEDB:Transaction Commit Mode</span></span><br />
<span data-ttu-id="d583c-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span><span class="sxs-lookup"><span data-stu-id="d583c-216">(DBPROP_JETOLEDB_TXNCOMMITMODE)</span></span></p></td>
<td><p><span data-ttu-id="d583c-217">Indique si Jet écrit les données sur le disque en mode synchrone ou en mode asynchrone lorsqu'une transaction est validée.</span><span class="sxs-lookup"><span data-stu-id="d583c-217">Indicates whether Jet writes data to disk synchronously or asynchronously when a transaction is committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-218">Jet OLEDB:User Commit Sync</span><span class="sxs-lookup"><span data-stu-id="d583c-218">Jet OLEDB:User Commit Sync</span></span><br />
<span data-ttu-id="d583c-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span><span class="sxs-lookup"><span data-stu-id="d583c-219">(DBPROP_JETOLEDB_USERCOMMITSYNC)</span></span></p></td>
<td><p><span data-ttu-id="d583c-220">Indique si les modifications effectuées dans les transactions sont écrites en mode synchrone ou en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d583c-220">Indicates whether changes made in transactions are written in synchronous or asynchronous mode.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="d583c-221">Propriétés spécifiques au fournisseur pour le jeu d'enregistrements et la commande</span><span class="sxs-lookup"><span data-stu-id="d583c-221">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="d583c-p112">Le fournisseur Jet prend aussi en charge plusieurs propriétés spécifiques au fournisseur pour les objets **Recordset** et **Command**. Il est possible d'accéder à ces propriétés et de les définir au travers de la collection **Properties** de l'objet **Recordset** ou **Command**. La table répertorie le nom de chaque propriété ADO en spécifiant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="d583c-p112">The Jet provider also supports several provider-specific **Recordset** and **Command** properties. These properties are accessed and set through the **Properties** collection of the **Recordset** or **Command** object. The table lists the ADO property name and its corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d583c-225">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="d583c-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="d583c-226">Description</span><span class="sxs-lookup"><span data-stu-id="d583c-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d583c-227">Transactions OLEDB:Bulk Jet</span><span class="sxs-lookup"><span data-stu-id="d583c-227">Jet OLEDB:Bulk Transactions</span></span><br />
<span data-ttu-id="d583c-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span><span class="sxs-lookup"><span data-stu-id="d583c-228">(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p113">Indique si les opérations SQL en bloc sont traitées. Le traitement des opérations en bloc volumineuses peut échouer en raison de retards dans la gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="d583c-p113">Indicates whether SQL bulk operations are transacted. Large bulk operations might fail when transacted, due to resource delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-231">Jet OLEDB : Enable Fat Cursors</span><span class="sxs-lookup"><span data-stu-id="d583c-231">Jet OLEDB:Enable Fat Cursors</span></span><br />
<span data-ttu-id="d583c-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span><span class="sxs-lookup"><span data-stu-id="d583c-232">(DBPROP_JETOLEDB_ENABLEFATCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="d583c-233">Indique si Jet doit mettre en cache plusieurs lignes lors du remplissage d'un jeu d'enregistrements pour une source de lignes distante.</span><span class="sxs-lookup"><span data-stu-id="d583c-233">Indicates whether Jet should cache multiple rows when populating a recordset for remote row sources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-234">Taille du Cache de Jet OLEDB:Fat curseur</span><span class="sxs-lookup"><span data-stu-id="d583c-234">Jet OLEDB:Fat Cursor Cache Size</span></span><br />
<span data-ttu-id="d583c-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span><span class="sxs-lookup"><span data-stu-id="d583c-235">(DBPROP_JETOLEDB_FATCURSORMAXROWS)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p114">Indique le nombre de lignes concernées par la mise en cache des lignes du magasin de données distant. Cette valeur est ignorée sauf si <strong>Jet OLEDB:Enable Fat Cursors</strong> a la valeur True.  </span><span class="sxs-lookup"><span data-stu-id="d583c-p114">Indicates the number of rows to cache when using remote data store row caching. This value is ignored unless <strong>Jet OLEDB:Enable Fat Cursors</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-238">Jet OLEDB : incohérentes</span><span class="sxs-lookup"><span data-stu-id="d583c-238">Jet OLEDB:Inconsistent</span></span><br />
<span data-ttu-id="d583c-239">(DBPROP_JETOLEDB_INCONSISTENT)</span><span class="sxs-lookup"><span data-stu-id="d583c-239">(DBPROP_JETOLEDB_INCONSISTENT)</span></span></p></td>
<td><p><span data-ttu-id="d583c-240">Indique si les résultats des requêtes autorisent les mises à jour incohérentes.</span><span class="sxs-lookup"><span data-stu-id="d583c-240">Indicates whether query results allow inconsistent updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-241">Jet OLEDB : granularité</span><span class="sxs-lookup"><span data-stu-id="d583c-241">Jet OLEDB:Locking Granularity</span></span><br />
<span data-ttu-id="d583c-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span><span class="sxs-lookup"><span data-stu-id="d583c-242">(DBPROP_JETOLEDB_LOCKGRANULARITY)</span></span></p></td>
<td><p><span data-ttu-id="d583c-243">Indique si le verrouillage des lignes est utilisé à l'ouverture d'une table.</span><span class="sxs-lookup"><span data-stu-id="d583c-243">Indicates whether a table is opened using row-level locking.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-244">Jet OLEDB : ODBC Pass-Through Statement</span><span class="sxs-lookup"><span data-stu-id="d583c-244">Jet OLEDB:ODBC Pass-Through Statement</span></span><br />
<span data-ttu-id="d583c-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span><span class="sxs-lookup"><span data-stu-id="d583c-245">(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</span></span></p></td>
<td><p><span data-ttu-id="d583c-246">Indique que Jet doit transmettre à la base de données principale le texte SQL dans un objet <strong>Command</strong> sans le modifier.</span><span class="sxs-lookup"><span data-stu-id="d583c-246">Indicates that Jet should pass the SQL text in a <strong>Command</strong> object to the back end unaltered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-247">Opérations en bloc de Jet OLEDB:Partial</span><span class="sxs-lookup"><span data-stu-id="d583c-247">Jet OLEDB:Partial Bulk Ops</span></span><br />
<span data-ttu-id="d583c-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span><span class="sxs-lookup"><span data-stu-id="d583c-248">(DBPROP_JETOLEDB_BULKPARTIAL)</span></span></p></td>
<td><p><span data-ttu-id="d583c-249">Spécifie le comportement de Jet en cas d'échec des opérations DML SQL.</span><span class="sxs-lookup"><span data-stu-id="d583c-249">Indicates Jet's behavior when SQL DML operations fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-250">Jet OLEDB:Pass par le biais de requête d’opération en bloc</span><span class="sxs-lookup"><span data-stu-id="d583c-250">Jet OLEDB:Pass Through Query Bulk-Op</span></span><br />
<span data-ttu-id="d583c-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span><span class="sxs-lookup"><span data-stu-id="d583c-251">(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</span></span></p></td>
<td><p><span data-ttu-id="d583c-252">Indique si les requêtes qui ne renvoient pas de <strong>Recordset</strong> sont transmises sans modification à la source de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-252">Indicates whether queries that do not return a <strong>Recordset</strong> are passed unaltered to the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-253">Chaîne de connexion Jet OLEDB:Pass par requête</span><span class="sxs-lookup"><span data-stu-id="d583c-253">Jet OLEDB:Pass Through Query Connect String</span></span><br />
<span data-ttu-id="d583c-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span><span class="sxs-lookup"><span data-stu-id="d583c-254">(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</span></span></p></td>
<td><p><span data-ttu-id="d583c-p115">Spécifie la chaîne Jet utilisée pour la connexion à un magasin de données distant. Cette valeur est ignorée sauf si <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> a la valeur True.  </span><span class="sxs-lookup"><span data-stu-id="d583c-p115">Indicates the Jet connect string used to connect to a remote data store. This value is ignored unless <strong>Jet OLEDB:ODBC Pass-Through Statement</strong> is True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-257">Jet OLEDB : stockés de requête</span><span class="sxs-lookup"><span data-stu-id="d583c-257">Jet OLEDB:Stored Query</span></span><br />
<span data-ttu-id="d583c-258">(DBPROP_JETOLEDB_STOREDQUERY)</span><span class="sxs-lookup"><span data-stu-id="d583c-258">(DBPROP_JETOLEDB_STOREDQUERY)</span></span></p></td>
<td><p><span data-ttu-id="d583c-259">Indique si le texte de commande doit être interprété comme une requête stockée au lieu d'une commande SQL.</span><span class="sxs-lookup"><span data-stu-id="d583c-259">Indicates whether the command text should be interpreted as a stored query instead of an SQL command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-260">Jet OLEDB : valider le jeu de règles</span><span class="sxs-lookup"><span data-stu-id="d583c-260">Jet OLEDB:Validate Rules On Set</span></span><br />
<span data-ttu-id="d583c-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span><span class="sxs-lookup"><span data-stu-id="d583c-261">(DBPROP_JETOLEDB_VALIDATEONSET)</span></span></p></td>
<td><p><span data-ttu-id="d583c-262">Indique si les règles de validation Jet sont évaluées lorsque les données des colonnes sont définies ou quand les modifications sont validées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="d583c-262">Indicates whether the Jet validation rules are evaluated when column data is set or when the changes are committed to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d583c-p116">Par défaut, le fournisseur OLE DB pour Microsoft Jet ouvre les bases de données Microsoft Jet en mode lecture/écriture. Pour ouvrir une base de données en mode lecture seule, définissez la propriété [Mode](mode-property-ado.md) de l'objet ADO **Connection** sur **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="d583c-p116">By default, the OLE DB Provider for Microsoft Jet opens Microsoft Jet databases in read/write mode. To open a database in read-only mode, set the [Mode](mode-property-ado.md) property on the ADO **Connection** object to **adModeRead**.</span></span>

## <a name="command-object-usage"></a><span data-ttu-id="d583c-265">Utilisation de l'objet Command</span><span class="sxs-lookup"><span data-stu-id="d583c-265">Command Object Usage</span></span>

<span data-ttu-id="d583c-p117">Le texte de commande de l'objet [Command](command-object-ado.md) utilise le dialecte SQL Microsoft Jet. Dans le texte de commande, vous pouvez spécifier des requêtes de renvoi de lignes, des requêtes d'action et des noms de table ; en revanche, les procédures stockées ne sont pas prises en charge et ne doivent pas être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d583c-p117">Command text in the [Command](command-object-ado.md) object uses the Microsoft Jet SQL dialect. You can specify row-returning queries, action queries, and table names in the command text; however, stored procedures are not supported and should not be specified.</span></span>

## <a name="recordset-behavior"></a><span data-ttu-id="d583c-268">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="d583c-268">Recordset Behavior</span></span>

<span data-ttu-id="d583c-p118">Le moteur de base de données Microsoft Jet ne prend pas en charge les curseurs dynamiques. Par conséquent, le fournisseur OLE DB pour Microsoft Jet ne prend pas en charge le type de curseur **adLockDynamic**. Lorsqu’un curseur dynamique est demandé, le fournisseur renvoie un curseur keyset et réinitialise la propriété [CursorType](cursortype-property-ado.md) pour indiquer le type de [Recordset](recordset-object-ado.md) renvoyé. Ensuite, si un \*\*Recordset \*\* actualisable est demandé ( \*\*LockType \*\* indique **adLockOptimistic**, **adLockBatchOptimistic** ou **adLockPessimistic**), le fournisseur renverra également un curseur keyset et réinitialisera la propriété **CursorType**.</span><span class="sxs-lookup"><span data-stu-id="d583c-p118">The Microsoft Jet database engine does not support dynamic cursors. Therefore, the OLE DB Provider for Microsoft Jet does not support the **adLockDynamic** cursor type. When a dynamic cursor is requested, the provider will return a keyset cursor and reset the [CursorType](cursortype-property-ado.md) property to indicate the type of [Recordset](recordset-object-ado.md) returned. Further, if an updatable **Recordset** is requested (**LockType** is **adLockOptimistic**, **adLockBatchOptimistic**, or **adLockPessimistic**) the provider will also return a keyset cursor and reset the **CursorType** property.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="d583c-273">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d583c-273">Dynamic Properties</span></span>

<span data-ttu-id="d583c-274">Le fournisseur OLE DB pour Microsoft Jet insère plusieurs propriétés dynamiques dans la collection **Properties** des objets [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) et [Command](command-object-ado.md) non ouverts.</span><span class="sxs-lookup"><span data-stu-id="d583c-274">The OLE DB Provider for Microsoft Jet inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="d583c-p119">Les tableaux suivants forment un index croisé des noms ADO et OLE DB de chaque propriété dynamique. Le guide OLE DB Programmer's Reference référence les noms de propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés. Recherchez le nom de la propriété OLE DB dans l'Index ou consultez la rubrique « Appendix C: OLE DB Properties ».</span><span class="sxs-lookup"><span data-stu-id="d583c-p119">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="d583c-279">Propriétés dynamiques de connexion</span><span class="sxs-lookup"><span data-stu-id="d583c-279">Connection Dynamic Properties</span></span>

<span data-ttu-id="d583c-280">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="d583c-280">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d583c-281">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="d583c-281">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="d583c-282">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="d583c-282">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d583c-283">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="d583c-283">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="d583c-284">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="d583c-284">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-285">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="d583c-285">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="d583c-286">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="d583c-286">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-287">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="d583c-287">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="d583c-288">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="d583c-288">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-289">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="d583c-289">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="d583c-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="d583c-290">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-291">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="d583c-291">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="d583c-292">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="d583c-292">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-293">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="d583c-293">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="d583c-294">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="d583c-294">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-295">Column Definition</span><span class="sxs-lookup"><span data-stu-id="d583c-295">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="d583c-296">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="d583c-296">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-297">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="d583c-297">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="d583c-298">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="d583c-298">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-299">Data Source</span><span class="sxs-lookup"><span data-stu-id="d583c-299">Data Source</span></span></p></td>
<td><p><span data-ttu-id="d583c-300">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="d583c-300">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-301">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="d583c-301">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="d583c-302">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="d583c-302">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-303">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="d583c-303">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="d583c-304">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="d583c-304">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-305">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="d583c-305">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="d583c-306">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="d583c-306">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-307">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="d583c-307">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="d583c-308">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="d583c-308">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-309">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="d583c-309">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="d583c-310">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="d583c-310">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-311">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="d583c-311">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="d583c-312">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="d583c-312">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-313">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="d583c-313">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="d583c-314">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="d583c-314">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-315">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="d583c-315">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="d583c-316">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="d583c-316">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-317">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="d583c-317">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="d583c-318">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="d583c-318">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-319">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="d583c-319">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="d583c-320">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="d583c-320">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-321">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="d583c-321">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="d583c-322">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="d583c-322">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-323">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="d583c-323">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="d583c-324">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="d583c-324">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-325">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="d583c-325">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="d583c-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="d583c-326">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-327">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="d583c-327">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="d583c-328">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="d583c-328">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-329">Mode</span><span class="sxs-lookup"><span data-stu-id="d583c-329">Mode</span></span></p></td>
<td><p><span data-ttu-id="d583c-330">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="d583c-330">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-331">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="d583c-331">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="d583c-332">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="d583c-332">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-333">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="d583c-333">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="d583c-334">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="d583c-334">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-335">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="d583c-335">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="d583c-336">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d583c-336">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-337">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="d583c-337">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="d583c-338">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="d583c-338">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-339">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="d583c-339">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="d583c-340">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="d583c-340">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-341">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="d583c-341">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="d583c-342">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="d583c-342">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-343">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="d583c-343">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="d583c-344">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="d583c-344">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-345">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="d583c-345">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="d583c-346">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d583c-346">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-347">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="d583c-347">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="d583c-348">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="d583c-348">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-349">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="d583c-349">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="d583c-350">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="d583c-350">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-351">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="d583c-351">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="d583c-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="d583c-352">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-353">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="d583c-353">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="d583c-354">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="d583c-354">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-355">Password</span><span class="sxs-lookup"><span data-stu-id="d583c-355">Password</span></span></p></td>
<td><p><span data-ttu-id="d583c-356">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="d583c-356">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-357">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="d583c-357">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="d583c-358">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="d583c-358">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-359">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="d583c-359">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="d583c-360">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="d583c-360">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-361">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="d583c-361">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="d583c-362">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="d583c-362">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-363">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="d583c-363">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="d583c-364">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="d583c-364">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-365">Prompt</span><span class="sxs-lookup"><span data-stu-id="d583c-365">Prompt</span></span></p></td>
<td><p><span data-ttu-id="d583c-366">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="d583c-366">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-367">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="d583c-367">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="d583c-368">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="d583c-368">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-369">Provider Name</span><span class="sxs-lookup"><span data-stu-id="d583c-369">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="d583c-370">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="d583c-370">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-371">Provider Version</span><span class="sxs-lookup"><span data-stu-id="d583c-371">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="d583c-372">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="d583c-372">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-373">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="d583c-373">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="d583c-374">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="d583c-374">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-375">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="d583c-375">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="d583c-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="d583c-376">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-377">Schema Term</span><span class="sxs-lookup"><span data-stu-id="d583c-377">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="d583c-378">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="d583c-378">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-379">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="d583c-379">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="d583c-380">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="d583c-380">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-381">SQL Support</span><span class="sxs-lookup"><span data-stu-id="d583c-381">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="d583c-382">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="d583c-382">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-383">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="d583c-383">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="d583c-384">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="d583c-384">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-385">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="d583c-385">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="d583c-386">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="d583c-386">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-387">Table Term</span><span class="sxs-lookup"><span data-stu-id="d583c-387">Table Term</span></span></p></td>
<td><p><span data-ttu-id="d583c-388">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="d583c-388">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-389">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="d583c-389">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="d583c-390">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="d583c-390">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-391">User ID</span><span class="sxs-lookup"><span data-stu-id="d583c-391">User ID</span></span></p></td>
<td><p><span data-ttu-id="d583c-392">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="d583c-392">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-393">User Name</span><span class="sxs-lookup"><span data-stu-id="d583c-393">User Name</span></span></p></td>
<td><p><span data-ttu-id="d583c-394">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="d583c-394">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-395">Window Handle</span><span class="sxs-lookup"><span data-stu-id="d583c-395">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="d583c-396">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="d583c-396">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="d583c-397">Propriétés dynamiques du jeu d'enregitrements</span><span class="sxs-lookup"><span data-stu-id="d583c-397">Recordset Dynamic Properties</span></span>

<span data-ttu-id="d583c-398">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d583c-398">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d583c-399">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="d583c-399">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="d583c-400">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="d583c-400">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d583c-401">Access Order</span><span class="sxs-lookup"><span data-stu-id="d583c-401">Access Order</span></span></p></td>
<td><p><span data-ttu-id="d583c-402">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="d583c-402">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-403">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="d583c-403">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="d583c-404">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="d583c-404">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-405">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="d583c-405">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="d583c-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d583c-406">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-407">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="d583c-407">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="d583c-408">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="d583c-408">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-409">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="d583c-409">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="d583c-410">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="d583c-410">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-411">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="d583c-411">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="d583c-412">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d583c-412">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-413">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="d583c-413">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="d583c-414">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="d583c-414">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-415">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-415">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-416">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-416">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-417">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="d583c-417">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="d583c-418">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d583c-418">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-419">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-419">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-420">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="d583c-420">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-421">Column Writable</span><span class="sxs-lookup"><span data-stu-id="d583c-421">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="d583c-422">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d583c-422">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-423">Defer Column</span><span class="sxs-lookup"><span data-stu-id="d583c-423">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="d583c-424">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="d583c-424">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-425">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="d583c-425">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="d583c-426">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d583c-426">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-427">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="d583c-427">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="d583c-428">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d583c-428">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-429">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-429">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-430">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-430">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-431">IAccessor</span><span class="sxs-lookup"><span data-stu-id="d583c-431">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="d583c-432">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="d583c-432">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-433">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-433">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="d583c-434">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-434">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-435">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-435">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="d583c-436">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-436">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-437">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d583c-437">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="d583c-438">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d583c-438">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-439">IConvertType</span><span class="sxs-lookup"><span data-stu-id="d583c-439">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="d583c-440">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="d583c-440">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-441">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="d583c-441">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="d583c-442">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="d583c-442">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-443">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-443">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-444">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-444">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-445">IRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-445">IRowset</span></span></p></td>
<td><p><span data-ttu-id="d583c-446">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-446">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-447">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d583c-447">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="d583c-448">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d583c-448">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-449">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d583c-449">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="d583c-450">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d583c-450">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-451">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="d583c-451">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="d583c-452">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="d583c-452">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-453">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-453">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="d583c-454">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-454">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-455">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="d583c-455">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="d583c-456">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="d583c-456">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-457">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="d583c-457">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-458">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d583c-458">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="d583c-459">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d583c-459">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-460">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d583c-460">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="d583c-461">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d583c-461">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-462">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d583c-462">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="d583c-463">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d583c-463">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-464">IStorage</span><span class="sxs-lookup"><span data-stu-id="d583c-464">IStorage</span></span></p></td>
<td><p><span data-ttu-id="d583c-465">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="d583c-465">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-466">IStream</span><span class="sxs-lookup"><span data-stu-id="d583c-466">IStream</span></span></p></td>
<td><p><span data-ttu-id="d583c-467">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="d583c-467">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-468">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-468">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="d583c-469">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-469">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-470">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d583c-470">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d583c-471">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d583c-471">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-472">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="d583c-472">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d583c-473">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="d583c-473">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-474">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-474">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-475">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-475">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-476">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-476">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-477">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-477">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-478">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-478">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-479">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-479">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-480">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="d583c-480">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="d583c-481">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="d583c-481">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-482">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="d583c-482">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="d583c-483">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="d583c-483">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-484">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="d583c-484">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="d583c-485">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="d583c-485">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-486">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="d583c-486">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="d583c-487">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="d583c-487">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-488">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-488">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-489">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-489">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-490">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-490">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-491">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-491">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-492">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-492">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-493">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-493">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-494">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-494">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-495">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-495">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-496">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="d583c-496">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="d583c-497">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d583c-497">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-498">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="d583c-498">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="d583c-499">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d583c-499">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-500">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="d583c-500">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="d583c-501">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="d583c-501">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-502">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="d583c-502">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="d583c-503">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="d583c-503">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-504">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-504">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-505">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="d583c-505">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-506">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="d583c-506">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="d583c-507">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="d583c-507">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-508">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="d583c-508">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="d583c-509">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="d583c-509">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-510">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-510">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-511">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-511">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-512">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-512">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-513">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="d583c-513">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-514">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-514">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-515">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-515">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-516">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="d583c-516">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="d583c-517">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d583c-517">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-518">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-518">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-519">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="d583c-519">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-520">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="d583c-520">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="d583c-521">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="d583c-521">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-522">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-522">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-523">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="d583c-523">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-524">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-524">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-525">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-525">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-526">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-526">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-527">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-527">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-528">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-528">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-529">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="d583c-529">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-530">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-530">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="d583c-531">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-532">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-532">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-533">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="d583c-533">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-534">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="d583c-534">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="d583c-535">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d583c-535">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-536">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d583c-536">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d583c-537">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="d583c-537">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-538">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="d583c-538">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d583c-539">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="d583c-539">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-540">Updatability</span><span class="sxs-lookup"><span data-stu-id="d583c-540">Updatability</span></span></p></td>
<td><p><span data-ttu-id="d583c-541">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="d583c-541">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-542">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d583c-542">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d583c-543">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d583c-543">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="d583c-544">Propriétés dynamiques de la commande</span><span class="sxs-lookup"><span data-stu-id="d583c-544">Command Dynamic Properties</span></span>

<span data-ttu-id="d583c-545">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="d583c-545">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d583c-546">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="d583c-546">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="d583c-547">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="d583c-547">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d583c-548">Access Order</span><span class="sxs-lookup"><span data-stu-id="d583c-548">Access Order</span></span></p></td>
<td><p><span data-ttu-id="d583c-549">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="d583c-549">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-550">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="d583c-550">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="d583c-551">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="d583c-551">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-552">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="d583c-552">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="d583c-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d583c-553">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-554">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="d583c-554">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="d583c-555">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="d583c-555">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-556">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="d583c-556">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="d583c-557">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="d583c-557">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-558">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-558">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-559">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-559">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-560">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="d583c-560">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="d583c-561">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d583c-561">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-562">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-562">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-563">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="d583c-563">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-564">Defer Column</span><span class="sxs-lookup"><span data-stu-id="d583c-564">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="d583c-565">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="d583c-565">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-566">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="d583c-566">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="d583c-567">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d583c-567">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-568">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="d583c-568">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="d583c-569">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d583c-569">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-570">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-570">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-571">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-571">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-572">IAccessor</span><span class="sxs-lookup"><span data-stu-id="d583c-572">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="d583c-573">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="d583c-573">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-574">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-574">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="d583c-575">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-575">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-576">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-576">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="d583c-577">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-577">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-578">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d583c-578">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="d583c-579">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d583c-579">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-580">IConvertType</span><span class="sxs-lookup"><span data-stu-id="d583c-580">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="d583c-581">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="d583c-581">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-582">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="d583c-582">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="d583c-583">DBPROP_ILockBytes</span><span class="sxs-lookup"><span data-stu-id="d583c-583">DBPROP_ILockBytes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-584">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-584">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-585">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-585">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-586">IRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-586">IRowset</span></span></p></td>
<td><p><span data-ttu-id="d583c-587">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="d583c-587">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-588">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d583c-588">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="d583c-589">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d583c-589">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-590">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d583c-590">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="d583c-591">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d583c-591">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-592">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="d583c-592">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="d583c-593">DBPROP_IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="d583c-593">DBPROP_IRowsetIndex</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-594">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-594">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="d583c-595">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-595">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-596">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="d583c-596">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="d583c-597">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="d583c-597">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-598">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="d583c-598">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-599">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d583c-599">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="d583c-600">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d583c-600">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-601">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d583c-601">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="d583c-602">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d583c-602">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-603">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d583c-603">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="d583c-604">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d583c-604">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-605">IStorage</span><span class="sxs-lookup"><span data-stu-id="d583c-605">IStorage</span></span></p></td>
<td><p><span data-ttu-id="d583c-606">DBPROP_IStorage</span><span class="sxs-lookup"><span data-stu-id="d583c-606">DBPROP_IStorage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-607">IStream</span><span class="sxs-lookup"><span data-stu-id="d583c-607">IStream</span></span></p></td>
<td><p><span data-ttu-id="d583c-608">DBPROP_IStream</span><span class="sxs-lookup"><span data-stu-id="d583c-608">DBPROP_IStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-609">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-609">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="d583c-610">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d583c-610">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-611">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d583c-611">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d583c-612">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d583c-612">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-613">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="d583c-613">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d583c-614">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="d583c-614">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-615">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="d583c-615">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="d583c-616">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="d583c-616">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-617">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-617">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-618">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-618">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-619">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-619">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-620">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-620">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-621">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-621">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-622">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="d583c-622">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-623">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="d583c-623">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="d583c-624">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="d583c-624">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-625">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="d583c-625">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="d583c-626">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="d583c-626">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-627">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="d583c-627">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="d583c-628">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="d583c-628">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-629">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-629">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-630">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-630">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-631">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-631">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-632">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-632">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-633">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-633">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-634">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-634">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-635">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d583c-635">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d583c-636">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-636">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-637">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="d583c-637">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="d583c-638">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d583c-638">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-639">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="d583c-639">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="d583c-640">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d583c-640">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-641">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="d583c-641">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="d583c-642">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="d583c-642">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-643">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="d583c-643">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="d583c-644">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="d583c-644">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-645">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="d583c-645">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="d583c-646">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="d583c-646">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-647">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="d583c-647">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="d583c-648">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="d583c-648">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-649">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="d583c-649">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="d583c-650">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="d583c-650">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-651">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-651">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-652">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-652">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-653">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-653">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-654">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="d583c-654">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-655">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-655">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-656">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-656">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-657">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="d583c-657">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="d583c-658">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d583c-658">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-659">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-659">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-660">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="d583c-660">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-661">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="d583c-661">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="d583c-662">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="d583c-662">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-663">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-663">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-664">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="d583c-664">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-665">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-665">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-666">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="d583c-666">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-667">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-667">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-668">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-668">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-669">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-669">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-670">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="d583c-670">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-671">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-671">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="d583c-672">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-673">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="d583c-673">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="d583c-674">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="d583c-674">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-675">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="d583c-675">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="d583c-676">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d583c-676">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-677">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="d583c-677">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="d583c-678">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="d583c-678">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-679">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d583c-679">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d583c-680">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="d583c-680">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-681">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="d583c-681">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d583c-682">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="d583c-682">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d583c-683">Updatability</span><span class="sxs-lookup"><span data-stu-id="d583c-683">Updatability</span></span></p></td>
<td><p><span data-ttu-id="d583c-684">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="d583c-684">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d583c-685">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d583c-685">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d583c-686">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d583c-686">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d583c-687">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d583c-687">See also</span></span>

<span data-ttu-id="d583c-688">Pour plus d’informations spécifiques à l’implémentation et des informations fonctionnelles sur le fournisseur OLE DB pour Microsoft Jet, consultez le fournisseur OLE DB pour la documentation Microsoft Jet dans le SDK de MDAC.</span><span class="sxs-lookup"><span data-stu-id="d583c-688">For specific implementation details and functional information about the OLE DB Provider for Microsoft Jet, consult the OLE DB Provider for Microsoft Jet documentation in the MDAC SDK.</span></span>

