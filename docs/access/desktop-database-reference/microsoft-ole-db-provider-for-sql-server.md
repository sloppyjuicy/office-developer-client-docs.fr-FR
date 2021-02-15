---
title: Fournisseur Microsoft OLE DB pour SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288889"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="d0f1a-102">Fournisseur Microsoft OLE DB pour SQL Server</span><span class="sxs-lookup"><span data-stu-id="d0f1a-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="d0f1a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0f1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0f1a-104">Le fournisseur Microsoft OLE DB pour SQL Server (SQLOLEDB) permet à ADO d'accéder à Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="d0f1a-105">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="d0f1a-105">Connection String Parameters</span></span>

<span data-ttu-id="d0f1a-106">Pour vous connecter à ce fournisseur, définissez l’argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="d0f1a-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="d0f1a-107">Cette valeur peut également être définie ou lue à partire de la propriété [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d0f1a-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="d0f1a-108">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="d0f1a-108">Typical Connection String</span></span>

<span data-ttu-id="d0f1a-109">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="d0f1a-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="d0f1a-110">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="d0f1a-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0f1a-111">Mot clé</span><span class="sxs-lookup"><span data-stu-id="d0f1a-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="d0f1a-112">Description</span><span class="sxs-lookup"><span data-stu-id="d0f1a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="d0f1a-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f1a-114">Spécifie le fournisseur OLE DB pour SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-115"><strong>Data Source</strong> ou <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d0f1a-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f1a-116">Spécifie le nom d'un serveur.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-117"><strong>Initial Catalog</strong> ou <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="d0f1a-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f1a-118">Spécifie le nom d'une base de données sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-119"><strong>User ID</strong> ou <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="d0f1a-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f1a-120">Spécifie le nom de l'utilisateur (pour l'authentification par SQL Server).</span><span class="sxs-lookup"><span data-stu-id="d0f1a-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-121"><strong>Password</strong> ou <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="d0f1a-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f1a-122">Spécifie le mot de passe de l'utilisateur (pour l'authentification par SQL Server).</span><span class="sxs-lookup"><span data-stu-id="d0f1a-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="d0f1a-123">Paramètres de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="d0f1a-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="d0f1a-p101">Le fournisseur prend en charge plusieurs paramètres de connexion qui lui sont spécifiques en plus de ceux définis par ADO. Comme les propriétés de connexion ADO, ces propriétés spécifiques au fournisseur peuvent être définies via la collection [Properties](properties-collection-ado.md) d’un objet [Connection](connection-object-ado.md) ou dans **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0f1a-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d0f1a-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="d0f1a-127">Description</span><span class="sxs-lookup"><span data-stu-id="d0f1a-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="d0f1a-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-p102">Indique le mode d’authentification de l’utilisateur. Peut être défini sur <strong>Oui</strong> ou sur <strong>Non</strong>. La valeur par défaut est <strong>Non</strong>. Si cette propriété est définie sur <strong>Oui </strong>, SQLOLEDB utilise le mode d’authentification Microsoft Windows NT pour autoriser l’accès de l’utilisateur à la base de données SQL Server spécifiée par les valeurs des propriétés <strong>Location</strong> et <a href="datasource-property-ado.md">Datasource</a>. Si cette propriété est définie sur <strong>Non </strong>, SQLOLEDB utilise le mode mixte. Le nom de connexion et le mot de passe SQL Server sont spécifiés dans les propriétés <strong>User Id</strong> et <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="d0f1a-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-p103">Indique le nom de la langue utilisée dans SQL Server.

Identifie la langue choisie pour la sélection et la mise en forme des messages système.

La langue doit être installée sur le serveur SQL ; sinon, la tentative de connexion échouera.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="d0f1a-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-140">Indique l'adresse réseau du serveur SQL spécifiée par la propriété <strong>Location </strong>.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="d0f1a-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-142">Indique le nom de la bibliothèque réseau (bibliothèques de liens dynamiques) utilisée pour communiquer avec le serveur SQL.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="d0f1a-143">Le nom ne doit pas inclure le chemin d’accès ni l’extension de nom de fichier .dll.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="d0f1a-144">La valeur par défaut est fournie par la configuration SQL Server client.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="d0f1a-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-146">Détermine si SQL Server crée des procédures stockées temporaires lors de la préparation de commandes (à l'aide de la propriété <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="d0f1a-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-p105">Indique si les caractères OEM/ANSI sont convertis. Cette propriété peut avoir la valeur <strong>True </strong> ou <strong>False </strong>. La valeur par défaut est <strong>True</strong>. Si cette propriété est définie sur <strong>True </strong>, SQLOLEDB effectue la conversion OEM/ANSI des caractères lorsque des chaînes de caractères multioctets sont extraites du serveur SQL ou sont envoyées vers ce serveur. Si cette propriété est définie sur <strong>False </strong>, SQLOLEDB n'effectue pas de conversion OEM/ANSI des caractères sur les données des chaînes de caractères multioctets.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="d0f1a-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-p106">Indique la taille du paquet réseau en octets.

La valeur de cette propriété doit être comprise entre 512 et 32 767.

Par défaut, la taille du paquet réseau pour SQLOLEDB est de 4096.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="d0f1a-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-158">Indique le nom de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="d0f1a-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-160">Chaîne identifiant la station de travail.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="d0f1a-161">Utilisation de l'objet Command</span><span class="sxs-lookup"><span data-stu-id="d0f1a-161">Command Object Usage</span></span>

<span data-ttu-id="d0f1a-p107">SQLOLEDB accepte comme valide une syntaxe mixte associant ODBC, ANSI et le langage Transact-SQL spécifique à SQL Server. Par exemple, l'instruction SQL suivante utilise une séquence d'échappement SQL ODBC pour spécifier la fonction de chaîne LCASE :</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="d0f1a-p108">LCASE renvoie une chaîne de caractères en convertissant tous les caractères majuscules en leurs équivalents minuscules. Dans le langage SQL ANSI, la fonction de chaîne LOWER effectue la même opération ; l'instruction SQL suivante est donc l'équivalent ANSI de l'instruction ODBC présentée ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="d0f1a-166">SQLOLEDB est capable de traiter cette instruction sous ces deux formes lorsqu'elle apparaît dans le texte d'une commande.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="d0f1a-167">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="d0f1a-167">Stored Procedures</span></span>

<span data-ttu-id="d0f1a-p109">Pour exécuter une procédure stockée SQL Server à l'aide d'une commande SQLOLEDB, utilisez la séquence d'échappement d'appel de procédure ODBC dans le texte de commande. SQLOLEDB utilise alors le mécanisme d'appel de procédure distante (RPC) de SQL Server pour optimiser le traitement de la commande. Par exemple, l'instruction SQL ODBC suivante est préférable dans le texte de commande à la forme Transact-SQL :</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="d0f1a-171">SQL ODBC</span><span class="sxs-lookup"><span data-stu-id="d0f1a-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="d0f1a-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="d0f1a-173">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="d0f1a-173">Recordset Behavior</span></span>

<span data-ttu-id="d0f1a-p110">SQLOLEDB ne peut pas utiliser les curseurs SQL Server pour prendre en charge les multiples résultats générés par plusieurs commandes. Lorsqu'un utilisateur demande un jeu d'enregistrements nécessitant la prise en charge des curseurs SQL Server, une erreur se produit si le texte de commande utilisé génère un résultat contenant plusieurs jeux d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="d0f1a-p111">Les jeux d'enregistrements SQLOLEDB avec fonction de défilement sont pris en charge par les curseurs SQL Server. SQL Server impose des limitations sur les curseurs sensibles aux modifications effectuées par d'autres utilisateurs de la base de données. Par exemple, il est impossible d'ordonner les lignes de certains curseurs et les tentatives de création d'un jeu d'enregistrements à l'aide d'une commande contenant une clause SQL ORDER BY peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="d0f1a-179">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d0f1a-179">Dynamic Properties</span></span>

<span data-ttu-id="d0f1a-180">Le fournisseur Microsoft OLE DB pour SQL Server insère plusieurs propriétés dynamiques dans la collection **Properties** des objets [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) et [Command](command-object-ado.md) non ouverts.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="d0f1a-p112">Les tableaux suivants forment un index croisé des noms ADO et OLE DB de chaque propriété dynamique. Le guide OLE DB Programmer's Reference (en anglais) référence les noms de propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés. Recherchez le nom de la propriété OLE DB dans l'Index ou consultez la rubrique « Appendix C: OLE DB Properties ».</span><span class="sxs-lookup"><span data-stu-id="d0f1a-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="d0f1a-185">Propriétés dynamiques de connexion</span><span class="sxs-lookup"><span data-stu-id="d0f1a-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="d0f1a-186">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0f1a-187">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="d0f1a-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="d0f1a-188">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="d0f1a-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="d0f1a-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="d0f1a-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="d0f1a-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="d0f1a-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="d0f1a-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="d0f1a-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="d0f1a-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="d0f1a-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="d0f1a-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="d0f1a-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="d0f1a-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="d0f1a-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="d0f1a-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="d0f1a-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="d0f1a-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="d0f1a-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="d0f1a-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="d0f1a-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="d0f1a-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="d0f1a-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="d0f1a-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="d0f1a-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="d0f1a-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="d0f1a-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="d0f1a-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="d0f1a-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="d0f1a-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d0f1a-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="d0f1a-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="d0f1a-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="d0f1a-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="d0f1a-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="d0f1a-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="d0f1a-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="d0f1a-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="d0f1a-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="d0f1a-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="d0f1a-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="d0f1a-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="d0f1a-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="d0f1a-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="d0f1a-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="d0f1a-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="d0f1a-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="d0f1a-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="d0f1a-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="d0f1a-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="d0f1a-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="d0f1a-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="d0f1a-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="d0f1a-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="d0f1a-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-265">Password</span><span class="sxs-lookup"><span data-stu-id="d0f1a-265">Password</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="d0f1a-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="d0f1a-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="d0f1a-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="d0f1a-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="d0f1a-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="d0f1a-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="d0f1a-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="d0f1a-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="d0f1a-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="d0f1a-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="d0f1a-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="d0f1a-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="d0f1a-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="d0f1a-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="d0f1a-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="d0f1a-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="d0f1a-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="d0f1a-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="d0f1a-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="d0f1a-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="d0f1a-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="d0f1a-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="d0f1a-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="d0f1a-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="d0f1a-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="d0f1a-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="d0f1a-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="d0f1a-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="d0f1a-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-303">User ID</span><span class="sxs-lookup"><span data-stu-id="d0f1a-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="d0f1a-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-305">User Name</span><span class="sxs-lookup"><span data-stu-id="d0f1a-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="d0f1a-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="d0f1a-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="d0f1a-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="d0f1a-309">Propriétés dynamiques du jeu d'enregitrements</span><span class="sxs-lookup"><span data-stu-id="d0f1a-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="d0f1a-310">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0f1a-311">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="d0f1a-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="d0f1a-312">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="d0f1a-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="d0f1a-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="d0f1a-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="d0f1a-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="d0f1a-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="d0f1a-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="d0f1a-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="d0f1a-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="d0f1a-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="d0f1a-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="d0f1a-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="d0f1a-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="d0f1a-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="d0f1a-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="d0f1a-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d0f1a-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d0f1a-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="d0f1a-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="d0f1a-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d0f1a-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d0f1a-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="d0f1a-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d0f1a-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d0f1a-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d0f1a-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d0f1a-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d0f1a-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="d0f1a-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="d0f1a-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="d0f1a-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="d0f1a-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="d0f1a-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="d0f1a-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="d0f1a-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="d0f1a-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="d0f1a-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="d0f1a-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="d0f1a-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="d0f1a-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="d0f1a-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="d0f1a-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="d0f1a-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="d0f1a-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="d0f1a-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-433">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="d0f1a-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d0f1a-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="d0f1a-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="d0f1a-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d0f1a-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="d0f1a-444">Propriétés dynamiques de la commande</span><span class="sxs-lookup"><span data-stu-id="d0f1a-444">Command Dynamic Properties</span></span>

<span data-ttu-id="d0f1a-445">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0f1a-446">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="d0f1a-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="d0f1a-447">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="d0f1a-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="d0f1a-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="d0f1a-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="d0f1a-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="d0f1a-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="d0f1a-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="d0f1a-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="d0f1a-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="d0f1a-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="d0f1a-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="d0f1a-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="d0f1a-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="d0f1a-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="d0f1a-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="d0f1a-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="d0f1a-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="d0f1a-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="d0f1a-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="d0f1a-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="d0f1a-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d0f1a-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d0f1a-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="d0f1a-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="d0f1a-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="d0f1a-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d0f1a-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="d0f1a-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="d0f1a-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="d0f1a-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d0f1a-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="d0f1a-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="d0f1a-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d0f1a-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="d0f1a-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="d0f1a-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d0f1a-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="d0f1a-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="d0f1a-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="d0f1a-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="d0f1a-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="d0f1a-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="d0f1a-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="d0f1a-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="d0f1a-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="d0f1a-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="d0f1a-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="d0f1a-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="d0f1a-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="d0f1a-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="d0f1a-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="d0f1a-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="d0f1a-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="d0f1a-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="d0f1a-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="d0f1a-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="d0f1a-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="d0f1a-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="d0f1a-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="d0f1a-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="d0f1a-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="d0f1a-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="d0f1a-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-581">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="d0f1a-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="d0f1a-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d0f1a-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="d0f1a-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="d0f1a-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="d0f1a-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="d0f1a-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="d0f1a-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="d0f1a-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f1a-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="d0f1a-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="d0f1a-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f1a-594">XSL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="d0f1a-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="d0f1a-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0f1a-596">Pour obtenir des détails spécifiques d'implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour SQL Server, consultez la documentation de ce produit dans la section OLE DB du kit de développement logiciel (SDK) de MDAC.</span><span class="sxs-lookup"><span data-stu-id="d0f1a-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

