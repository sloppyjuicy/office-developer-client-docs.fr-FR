---
title: Fournisseur Microsoft OLE DB pour SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f999f9268511fd23f1fc6a20c8459d11345ceb4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470104"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="ed1dd-102">Fournisseur Microsoft OLE DB pour SQL Server</span><span class="sxs-lookup"><span data-stu-id="ed1dd-102">Microsoft OLE DB Provider for SQL Server</span></span>


<span data-ttu-id="ed1dd-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed1dd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ed1dd-104">Le fournisseur Microsoft OLE DB pour SQL Server (SQLOLEDB) permet à ADO d'accéder à Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-104">The Microsoft OLE DB Provider for SQL Server, SQLOLEDB, allows ADO to access Microsoft SQL Server.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="ed1dd-105">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="ed1dd-105">Connection String Parameters</span></span>

<span data-ttu-id="ed1dd-106">Pour vous connecter à ce fournisseur, définissez l’argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="ed1dd-106">To connect to this provider, set the *Provider* argument to the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
SQLOLEDB 
```

<span data-ttu-id="ed1dd-107">Cette valeur peut également être définie ou lue à partire de la propriété [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ed1dd-107">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="ed1dd-108">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="ed1dd-108">Typical Connection String</span></span>

<span data-ttu-id="ed1dd-109">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="ed1dd-109">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="ed1dd-110">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="ed1dd-110">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed1dd-111">Mot clé</span><span class="sxs-lookup"><span data-stu-id="ed1dd-111">Keyword</span></span></p></th>
<th><p><span data-ttu-id="ed1dd-112">Description</span><span class="sxs-lookup"><span data-stu-id="ed1dd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-113"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="ed1dd-113"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1dd-114">Spécifie le fournisseur OLE DB pour SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-114">Specifies the OLE DB Provider for SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-115"><strong>Data Source</strong> ou <strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ed1dd-115"><strong>Data Source</strong> or <strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1dd-116">Spécifie le nom d'un serveur.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-116">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-117"><strong>Initial Catalog</strong> ou <strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="ed1dd-117"><strong>Initial Catalog</strong> or <strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1dd-118">Spécifie le nom d'une base de données sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-118">Specifies the name of a database on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-119"><strong>User ID</strong> ou <strong>uid</strong></span><span class="sxs-lookup"><span data-stu-id="ed1dd-119"><strong>User ID</strong> or <strong>uid</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1dd-120">Spécifie le nom de l'utilisateur (pour l'authentification par SQL Server).</span><span class="sxs-lookup"><span data-stu-id="ed1dd-120">Specifies the user name (for SQL Server Authentication).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-121"><strong>Password</strong> ou <strong>pwd</strong></span><span class="sxs-lookup"><span data-stu-id="ed1dd-121"><strong>Password</strong> or <strong>pwd</strong></span></span></p></td>
<td><p><span data-ttu-id="ed1dd-122">Spécifie le mot de passe de l'utilisateur (pour l'authentification par SQL Server).</span><span class="sxs-lookup"><span data-stu-id="ed1dd-122">Specifies the user password (for SQL Server Authentication).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="ed1dd-123">Paramètres de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="ed1dd-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="ed1dd-p101">Le fournisseur prend en charge plusieurs paramètres de connexion qui lui sont spécifiques en plus de ceux définis par ADO. Comme les propriétés de connexion ADO, ces propriétés spécifiques au fournisseur peuvent être définies via la collection [Properties](properties-collection-ado.md) d'un objet [Connection](connection-object-ado.md) ou dans **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p101">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or can be set as part of the **ConnectionString**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed1dd-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ed1dd-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="ed1dd-127">Description</span><span class="sxs-lookup"><span data-stu-id="ed1dd-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-128">Trusted_Connection</span><span class="sxs-lookup"><span data-stu-id="ed1dd-128">Trusted_Connection</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-p102">Indique le mode d’authentification de l’utilisateur. Peut être défini sur <strong>Oui</strong> ou sur <strong>Non</strong>. La valeur par défaut est <strong>Non</strong>. Si cette propriété est définie sur <strong>Oui </strong>, SQLOLEDB utilise le mode d’authentification Microsoft Windows NT pour autoriser l’accès de l’utilisateur à la base de données SQL Server spécifiée par les valeurs des propriétés <strong>Location</strong> et <a href="datasource-property-ado.md">Datasource</a>. Si cette propriété est définie sur <strong>Non </strong>, SQLOLEDB utilise le mode mixte. Le nom de connexion et le mot de passe SQL Server sont spécifiés dans les propriétés <strong>User Id</strong> et <strong>Password</strong>.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p102">Indicates the user authentication mode. This can be set to <strong>Yes</strong> or <strong>No</strong>. The default value is <strong>No</strong>. If this property is set to <strong>Yes</strong>, then SQLOLEDB uses Microsoft Windows NT Authentication Mode to authorize user access to the SQL Server database specified by the <strong>Location</strong> and <a href="datasource-property-ado.md">Datasource</a> property values. If this property is set to <strong>No</strong>, then SQLOLEDB uses Mixed Mode to authorize user access to the SQL Server database. The SQL Server login and password are specified in the <strong>User Id</strong> and <strong>Password</strong> properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-135">Current Language</span><span class="sxs-lookup"><span data-stu-id="ed1dd-135">Current Language</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-p103">Indique le nom de la langue utilisée dans SQL Server.

Identifie la langue choisie pour la sélection et la mise en forme des messages système.

La langue doit être installée sur le serveur SQL ; sinon, la tentative de connexion échouera.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p103">Indicates a SQL Server language name. Identifies the language used for system message selection and formatting. The language must be installed on the SQL Server, otherwise opening the connection will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-139">Network Address</span><span class="sxs-lookup"><span data-stu-id="ed1dd-139">Network Address</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-140">Indique l'adresse réseau du serveur SQL spécifiée par la propriété <strong>Location </strong>.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-140">Indicates the network address of the SQL Server specified by the <strong>Location</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-141">Network Library</span><span class="sxs-lookup"><span data-stu-id="ed1dd-141">Network Library</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-142">Indique le nom de la bibliothèque réseau (bibliothèques de liens dynamiques) utilisé pour communiquer avec le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-142">Indicates the name of the network library (dynamic-link libraries) used to communicate with the SQL Server.</span></span> <span data-ttu-id="ed1dd-143">Le nom ne doit pas inclure le chemin d’accès ou l’extension de nom de fichier .dll.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-143">The name should not include the path or the .dll file name extension.</span></span> <span data-ttu-id="ed1dd-144">La valeur par défaut est fournie par la configuration du client SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-144">The default is provided by the SQL Server client configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-145">Use Procedure for Prepare</span><span class="sxs-lookup"><span data-stu-id="ed1dd-145">Use Procedure for Prepare</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-146">Détermine si SQL Server crée des procédures stockées temporaires lors de la préparation de commandes (à l'aide de la propriété <strong>Prepared</strong>).</span><span class="sxs-lookup"><span data-stu-id="ed1dd-146">Determines whether SQL Server creates temporary stored procedures when Commands are prepared (by the <strong>Prepared</strong> property).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-147">Auto Translate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-147">Auto Translate</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-p105">Indique si les caractères OEM/ANSI sont convertis. Cette propriété peut avoir la valeur <strong>True </strong> ou <strong>False </strong>. La valeur par défaut est <strong>True</strong>. Si cette propriété est définie sur <strong>True </strong>, SQLOLEDB effectue la conversion OEM/ANSI des caractères lorsque des chaînes de caractères multioctets sont extraites du serveur SQL ou sont envoyées vers ce serveur. Si cette propriété est définie sur <strong>False </strong>, SQLOLEDB n'effectue pas de conversion OEM/ANSI des caractères sur les données des chaînes de caractères multioctets.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p105">Indicates whether OEM/ANSI characters are converted. This property can be set to <strong>True</strong> or <strong>False</strong>. The default value is <strong>True</strong>. If this property is set to <strong>True</strong>, then SQLOLEDB performs OEM/ANSI character conversion when multi-byte character strings are retrieved from, or sent to, the SQL Server. If this property is set to <strong>False</strong>, then SQLOLEDB does not perform OEM/ANSI character conversion on multi-byte character string data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-153">Packet Size</span><span class="sxs-lookup"><span data-stu-id="ed1dd-153">Packet Size</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-p106">Indique la taille du paquet réseau en octets.

La valeur de cette propriété doit être comprise entre 512 et 32 767.

Par défaut, la taille du paquet réseau pour SQLOLEDB est de 4096.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p106">Indicates a network packet size in bytes. The packet size property value must be between 512 and 32767. The default SQLOLEDB network packet size is 4096.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-157">Application Name</span><span class="sxs-lookup"><span data-stu-id="ed1dd-157">Application Name</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-158">Indique le nom de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-158">Indicates the client application name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-159">Workstation ID</span><span class="sxs-lookup"><span data-stu-id="ed1dd-159">Workstation ID</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-160">Chaîne identifiant la station de travail.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-160">A string identifying the workstation.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a><span data-ttu-id="ed1dd-161">Utilisation de l'objet Command</span><span class="sxs-lookup"><span data-stu-id="ed1dd-161">Command Object Usage</span></span>

<span data-ttu-id="ed1dd-p107">SQLOLEDB accepte comme valide une syntaxe mixte associant ODBC, ANSI et le langage Transact-SQL spécifique à SQL Server. Par exemple, l'instruction SQL suivante utilise une séquence d'échappement SQL ODBC pour spécifier la fonction de chaîne LCASE :</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p107">SQLOLEDB accepts an amalgam of ODBC, ANSI, and SQL Server-specific Transact-SQL as valid syntax. For example, the following SQL statement uses an ODBC SQL escape sequence to specify the LCASE string function:</span></span>

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

<span data-ttu-id="ed1dd-p108">LCASE renvoie une chaîne de caractères en convertissant tous les caractères majuscules en leurs équivalents minuscules. Dans le langage SQL ANSI, la fonction de chaîne LOWER effectue la même opération ; l'instruction SQL suivante est donc l'équivalent ANSI de l'instruction ODBC présentée ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p108">LCASE returns a character string, converting all uppercase characters to their lowercase equivalents. The ANSI SQL string function LOWER performs the same operation, so the following SQL statement is an ANSI equivalent to the ODBC statement presented above:</span></span>

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

<span data-ttu-id="ed1dd-166">SQLOLEDB est capable de traiter cette instruction sous ces deux formes lorsqu'elle apparaît dans le texte d'une commande.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-166">SQLOLEDB successfully processes either form of the statement when specified as text for a command.</span></span>

## <a name="stored-procedures"></a><span data-ttu-id="ed1dd-167">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="ed1dd-167">Stored Procedures</span></span>

<span data-ttu-id="ed1dd-p109">Pour exécuter une procédure stockée SQL Server à l'aide d'une commande SQLOLEDB, utilisez la séquence d'échappement d'appel de procédure ODBC dans le texte de commande. SQLOLEDB utilise alors le mécanisme d'appel de procédure distante (RPC) de SQL Server pour optimiser le traitement de la commande. Par exemple, l'instruction SQL ODBC suivante est préférable dans le texte de commande à la forme Transact-SQL :</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p109">When executing a SQL Server stored procedure using a SQLOLEDB command, use the ODBC procedure call escape sequence in the command text. SQLOLEDB then uses the remote procedure call mechanism of SQL Server to optimize command processing. For example, the following ODBC SQL statement is the preferred command text over the Transact-SQL form:</span></span>

## <a name="odbc-sql"></a><span data-ttu-id="ed1dd-171">SQL ODBC</span><span class="sxs-lookup"><span data-stu-id="ed1dd-171">ODBC SQL</span></span>

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a><span data-ttu-id="ed1dd-172">Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-172">Transact-SQL</span></span>

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a><span data-ttu-id="ed1dd-173">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="ed1dd-173">Recordset Behavior</span></span>

<span data-ttu-id="ed1dd-p110">SQLOLEDB ne peut pas utiliser les curseurs SQL Server pour prendre en charge les multiples résultats générés par plusieurs commandes. Lorsqu'un utilisateur demande un jeu d'enregistrements nécessitant la prise en charge des curseurs SQL Server, une erreur se produit si le texte de commande utilisé génère un résultat contenant plusieurs jeux d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p110">SQLOLEDB cannot use SQL Server cursors to support the multiple-result generated by many commands. If a consumer requests a recordset requiring SQL Server cursor support, an error occurs if the command text used generates more than a single recordset as its result.</span></span>

<span data-ttu-id="ed1dd-p111">Les jeux d'enregistrements SQLOLEDB avec fonction de défilement sont pris en charge par les curseurs SQL Server. SQL Server impose des limitations sur les curseurs sensibles aux modifications effectuées par d'autres utilisateurs de la base de données. Par exemple, il est impossible d'ordonner les lignes de certains curseurs et les tentatives de création d'un jeu d'enregistrements à l'aide d'une commande contenant une clause SQL ORDER BY peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p111">Scrollable SQLOLEDB recordsets are supported by SQL Server cursors. SQL Server imposes limitations on cursors that are sensitive to changes made by other users of the database. Specifically, the rows in some cursors cannot be ordered, and attempting to create a recordset using a command containing an SQL ORDER BY clause can fail.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="ed1dd-179">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="ed1dd-179">Dynamic Properties</span></span>

<span data-ttu-id="ed1dd-180">Le fournisseur Microsoft OLE DB pour SQL Server insère plusieurs propriétés dynamiques dans la collection **Properties** des objets [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) et [Command](command-object-ado.md) non ouverts.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-180">The Microsoft OLE DB Provider for SQL Server inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="ed1dd-p112">Les tableaux suivants forment un index croisé des noms ADO et OLE DB de chaque propriété dynamique. Le guide OLE DB Programmer's Reference (en anglais) référence les noms de propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés. Recherchez le nom de la propriété OLE DB dans l'Index ou consultez la rubrique « Appendix C: OLE DB Properties ».</span><span class="sxs-lookup"><span data-stu-id="ed1dd-p112">The following tables are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="ed1dd-185">Propriétés dynamiques de connexion</span><span class="sxs-lookup"><span data-stu-id="ed1dd-185">Connection Dynamic Properties</span></span>

<span data-ttu-id="ed1dd-186">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-186">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed1dd-187">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="ed1dd-187">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ed1dd-188">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="ed1dd-188">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-189">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="ed1dd-189">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-190">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-190">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-191">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="ed1dd-191">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-192">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-192">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-193">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="ed1dd-193">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-194">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-194">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-195">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="ed1dd-195">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-196">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-197">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="ed1dd-197">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-198">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="ed1dd-198">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-199">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="ed1dd-199">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-200">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="ed1dd-200">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-201">Column Definition</span><span class="sxs-lookup"><span data-stu-id="ed1dd-201">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-202">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="ed1dd-202">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-203">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="ed1dd-203">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-204">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-204">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-205">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="ed1dd-205">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-206">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="ed1dd-206">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-207">Data Source</span><span class="sxs-lookup"><span data-stu-id="ed1dd-207">Data Source</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-208">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-208">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-209">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="ed1dd-209">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-210">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="ed1dd-210">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-211">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="ed1dd-211">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-212">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-212">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-213">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="ed1dd-213">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-214">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="ed1dd-214">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-215">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="ed1dd-215">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-216">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="ed1dd-216">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-217">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="ed1dd-217">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-218">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="ed1dd-218">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-219">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="ed1dd-219">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-220">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-220">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-221">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="ed1dd-221">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-222">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="ed1dd-222">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-223">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-223">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-224">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-224">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-225">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="ed1dd-225">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-226">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="ed1dd-226">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-227">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="ed1dd-227">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-228">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-228">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-229">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="ed1dd-229">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-230">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="ed1dd-230">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-231">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="ed1dd-231">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-232">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="ed1dd-232">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-233">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="ed1dd-233">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-234">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-234">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-235">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="ed1dd-235">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-236">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-236">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-237">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="ed1dd-237">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="ed1dd-238">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-239">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-239">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-240">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-240">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-241">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="ed1dd-241">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-242">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-242">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-243">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="ed1dd-243">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-244">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-244">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-245">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ed1dd-245">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-246">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-246">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-247">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="ed1dd-247">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-248">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-248">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-249">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="ed1dd-249">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-250">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="ed1dd-250">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-251">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="ed1dd-251">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-252">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ed1dd-252">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-253">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="ed1dd-253">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-254">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="ed1dd-254">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-255">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="ed1dd-255">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-256">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-256">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-257">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="ed1dd-257">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-258">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-258">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-259">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="ed1dd-259">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-260">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-260">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-261">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="ed1dd-261">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-262">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-263">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="ed1dd-263">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-264">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-264">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-265">Password</span><span class="sxs-lookup"><span data-stu-id="ed1dd-265">Password</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-266">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="ed1dd-266">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-267">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="ed1dd-267">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="ed1dd-268">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-269">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="ed1dd-269">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-270">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-270">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-271">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="ed1dd-271">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-272">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ed1dd-272">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-273">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="ed1dd-273">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-274">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="ed1dd-274">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-275">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="ed1dd-275">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-276">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="ed1dd-276">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-277">Prompt</span><span class="sxs-lookup"><span data-stu-id="ed1dd-277">Prompt</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-278">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-278">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-279">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="ed1dd-279">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-280">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="ed1dd-280">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-281">Provider Name</span><span class="sxs-lookup"><span data-stu-id="ed1dd-281">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-282">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="ed1dd-282">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-283">Provider Version</span><span class="sxs-lookup"><span data-stu-id="ed1dd-283">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-284">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="ed1dd-284">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-285">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="ed1dd-285">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-286">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-286">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-287">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="ed1dd-287">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="ed1dd-288">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-289">Schema Term</span><span class="sxs-lookup"><span data-stu-id="ed1dd-289">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-290">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="ed1dd-290">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-291">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="ed1dd-291">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-292">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-292">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-293">SQL Support</span><span class="sxs-lookup"><span data-stu-id="ed1dd-293">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-294">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-294">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-295">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="ed1dd-295">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-296">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-296">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-297">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="ed1dd-297">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-298">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="ed1dd-298">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-299">Table Term</span><span class="sxs-lookup"><span data-stu-id="ed1dd-299">Table Term</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-300">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="ed1dd-300">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-301">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-301">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-302">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-302">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-303">User ID</span><span class="sxs-lookup"><span data-stu-id="ed1dd-303">User ID</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-304">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="ed1dd-304">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-305">User Name</span><span class="sxs-lookup"><span data-stu-id="ed1dd-305">User Name</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-306">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="ed1dd-306">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-307">Window Handle</span><span class="sxs-lookup"><span data-stu-id="ed1dd-307">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-308">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="ed1dd-308">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="ed1dd-309">Propriétés dynamiques du jeu d'enregitrements</span><span class="sxs-lookup"><span data-stu-id="ed1dd-309">Recordset Dynamic Properties</span></span>

<span data-ttu-id="ed1dd-310">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-310">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed1dd-311">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="ed1dd-311">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ed1dd-312">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="ed1dd-312">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-313">Access Order</span><span class="sxs-lookup"><span data-stu-id="ed1dd-313">Access Order</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-314">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="ed1dd-314">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-315">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ed1dd-315">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-316">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-317">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="ed1dd-317">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-318">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-318">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-319">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="ed1dd-319">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-320">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-320">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-321">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-321">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-322">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-322">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-323">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="ed1dd-323">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-324">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-324">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-325">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-325">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-326">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="ed1dd-326">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-327">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="ed1dd-327">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-328">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-328">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-329">Defer Column</span><span class="sxs-lookup"><span data-stu-id="ed1dd-329">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-330">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="ed1dd-330">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-331">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="ed1dd-331">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-332">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-332">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-333">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="ed1dd-333">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-334">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-334">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-335">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-335">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-336">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-336">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-337">IAccessor</span><span class="sxs-lookup"><span data-stu-id="ed1dd-337">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-338">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="ed1dd-338">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-339">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-339">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-340">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-340">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-341">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-341">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-342">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-342">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-343">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ed1dd-343">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-344">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ed1dd-344">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-345">IConvertType</span><span class="sxs-lookup"><span data-stu-id="ed1dd-345">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-346">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="ed1dd-346">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-347">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-347">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-348">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-348">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-349">IRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-349">IRowset</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-350">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-350">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-351">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ed1dd-351">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-352">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ed1dd-352">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-353">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-353">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-354">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-354">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-355">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-355">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-356">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-356">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-357">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-357">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-358">DBPROP_IRowsestLocate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-358">DBPROP_IRowsestLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-359">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="ed1dd-359">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-360">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="ed1dd-360">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-361">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="ed1dd-361">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-362">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-362">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-363">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-363">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-364">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ed1dd-364">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-365">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ed1dd-365">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-366">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-366">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-367">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-367">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-368">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ed1dd-368">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-369">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-369">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-370">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-370">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-371">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-371">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-372">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-372">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-373">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-373">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-374">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-374">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-375">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-375">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-376">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-376">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-377">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-377">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-378">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-378">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-379">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-379">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-380">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="ed1dd-380">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-381">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="ed1dd-381">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-382">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="ed1dd-382">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-383">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-383">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-384">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-384">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-385">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-385">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-386">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-386">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-387">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-387">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-388">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-388">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-389">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-389">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-390">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-390">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-391">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-391">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-392">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="ed1dd-392">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-393">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-393">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-394">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="ed1dd-394">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-395">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-395">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-396">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="ed1dd-396">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-397">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="ed1dd-397">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-398">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="ed1dd-398">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-399">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-399">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-400">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-400">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-401">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="ed1dd-401">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-402">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="ed1dd-402">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-403">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="ed1dd-403">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-404">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="ed1dd-404">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-405">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-405">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-406">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-406">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-407">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-407">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-408">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-408">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-409">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-409">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-410">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-410">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-411">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-411">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-412">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="ed1dd-412">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-413">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-413">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-414">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-414">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-415">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="ed1dd-415">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-416">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="ed1dd-416">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-417">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-417">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-418">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-418">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-419">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-419">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-420">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-420">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-421">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-421">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-422">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-422">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-423">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-423">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-424">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-424">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-425">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-425">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-426">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-426">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-427">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-428">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-428">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-429">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-429">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-430">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="ed1dd-430">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-431">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-431">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-432">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="ed1dd-432">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-433">DONNEZ</span><span class="sxs-lookup"><span data-stu-id="ed1dd-433">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-434">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ed1dd-434">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-435">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="ed1dd-435">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-436">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-436">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-437">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-437">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-438">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-438">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-439">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-439">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-440">Updatability</span><span class="sxs-lookup"><span data-stu-id="ed1dd-440">Updatability</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-441">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-441">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-442">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ed1dd-442">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-443">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-443">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="ed1dd-444">Propriétés dynamiques de la commande</span><span class="sxs-lookup"><span data-stu-id="ed1dd-444">Command Dynamic Properties</span></span>

<span data-ttu-id="ed1dd-445">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-445">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed1dd-446">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="ed1dd-446">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="ed1dd-447">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="ed1dd-447">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-448">Access Order</span><span class="sxs-lookup"><span data-stu-id="ed1dd-448">Access Order</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-449">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="ed1dd-449">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-450">Base Path</span><span class="sxs-lookup"><span data-stu-id="ed1dd-450">Base Path</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-451">SSPROP_STREAM_BASEPATH</span><span class="sxs-lookup"><span data-stu-id="ed1dd-451">SSPROP_STREAM_BASEPATH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-452">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="ed1dd-452">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-453">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-454">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="ed1dd-454">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-455">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-455">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-456">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="ed1dd-456">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-457">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-457">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-458">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-458">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-459">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-459">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-460">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="ed1dd-460">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-461">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-461">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-462">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-462">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-463">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="ed1dd-463">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-464">Content Type</span><span class="sxs-lookup"><span data-stu-id="ed1dd-464">Content Type</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-465">SSPROP_STREAM_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-465">SSPROP_STREAM_CONTENTTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-466">Cursor Auto Fetch</span><span class="sxs-lookup"><span data-stu-id="ed1dd-466">Cursor Auto Fetch</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-467">SSPROP_CURSORAUTOFETCH</span><span class="sxs-lookup"><span data-stu-id="ed1dd-467">SSPROP_CURSORAUTOFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-468">Defer Column</span><span class="sxs-lookup"><span data-stu-id="ed1dd-468">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-469">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="ed1dd-469">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-470">Defer Prepare</span><span class="sxs-lookup"><span data-stu-id="ed1dd-470">Defer Prepare</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-471">SSPROP_DEFERPREPARE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-471">SSPROP_DEFERPREPARE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-472">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="ed1dd-472">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-473">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-473">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-474">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="ed1dd-474">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-475">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-475">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-476">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-476">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-477">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-477">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-478">IAccessor</span><span class="sxs-lookup"><span data-stu-id="ed1dd-478">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-479">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="ed1dd-479">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-480">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-480">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-481">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-481">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-482">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-482">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-483">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-483">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-484">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ed1dd-484">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-485">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="ed1dd-485">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-486">IConvertType</span><span class="sxs-lookup"><span data-stu-id="ed1dd-486">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-487">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="ed1dd-487">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-488">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-488">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-489">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-489">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-490">IRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-490">IRowset</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-491">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="ed1dd-491">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-492">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ed1dd-492">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-493">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="ed1dd-493">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-494">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-494">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-495">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-495">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-496">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-496">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-497">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-497">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-498">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-498">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-499">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-499">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-500">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="ed1dd-500">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-501">DBPROP_IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="ed1dd-501">DBPROP_IRowsetResynch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-502">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="ed1dd-502">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-503">DBPROP_IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="ed1dd-503">DBPROP_IRowsetScroll</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-504">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-504">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-505">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="ed1dd-505">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-506">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ed1dd-506">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-507">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="ed1dd-507">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-508">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-508">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-509">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ed1dd-509">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-510">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ed1dd-510">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-511">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-511">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-512">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-512">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-513">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-513">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-514">Lock Mode</span><span class="sxs-lookup"><span data-stu-id="ed1dd-514">Lock Mode</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-515">DBPROP_LOCKMODE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-515">DBPROP_LOCKMODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-516">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-516">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-517">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-517">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-518">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-518">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-519">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-519">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-520">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-520">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-521">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-521">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-522">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-522">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-523">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-523">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-524">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="ed1dd-524">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-525">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="ed1dd-525">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-526">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="ed1dd-526">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-527">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-527">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-528">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-528">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-529">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-529">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-530">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-530">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-531">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-531">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-532">Output Encoding Property</span><span class="sxs-lookup"><span data-stu-id="ed1dd-532">Output Encoding Property</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-533">DBPROP_OUTPUTENCODING</span><span class="sxs-lookup"><span data-stu-id="ed1dd-533">DBPROP_OUTPUTENCODING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-534">Output Stream Property</span><span class="sxs-lookup"><span data-stu-id="ed1dd-534">Output Stream Property</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-535">DBPROP_OUTPUTSTREAM</span><span class="sxs-lookup"><span data-stu-id="ed1dd-535">DBPROP_OUTPUTSTREAM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-536">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-536">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-537">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-537">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-538">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="ed1dd-538">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-539">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-539">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-540">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="ed1dd-540">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-541">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-541">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-542">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="ed1dd-542">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-543">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-543">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-544">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="ed1dd-544">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-545">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="ed1dd-545">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-546">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="ed1dd-546">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-547">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-547">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-548">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="ed1dd-548">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-549">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="ed1dd-549">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-550">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="ed1dd-550">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-551">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="ed1dd-551">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-552">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="ed1dd-552">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-553">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-553">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-554">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-554">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-555">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-555">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-556">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-556">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-557">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-557">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-558">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-558">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-559">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-559">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-560">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="ed1dd-560">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-561">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-561">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-562">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-562">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-563">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="ed1dd-563">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-564">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="ed1dd-564">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-565">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-565">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-566">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-566">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-567">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-567">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-568">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-568">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-569">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-569">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-570">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-570">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-571">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-571">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-572">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-572">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-573">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-573">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-574">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-574">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-575">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-576">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="ed1dd-576">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-577">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="ed1dd-577">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-578">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="ed1dd-578">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-579">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-579">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-580">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="ed1dd-580">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-581">DONNEZ</span><span class="sxs-lookup"><span data-stu-id="ed1dd-581">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-582">Server Data on Insert</span><span class="sxs-lookup"><span data-stu-id="ed1dd-582">Server Data on Insert</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-583">DBPROP_SERVERDATAONINSERT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-583">DBPROP_SERVERDATAONINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-584">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ed1dd-584">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-585">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="ed1dd-585">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-586">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="ed1dd-586">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-587">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-587">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-588">Updatability</span><span class="sxs-lookup"><span data-stu-id="ed1dd-588">Updatability</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-589">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="ed1dd-589">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-590">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="ed1dd-590">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-591">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="ed1dd-591">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed1dd-592">XML Root</span><span class="sxs-lookup"><span data-stu-id="ed1dd-592">XML Root</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-593">SSPROP_STREAM_XMLROOT</span><span class="sxs-lookup"><span data-stu-id="ed1dd-593">SSPROP_STREAM_XMLROOT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed1dd-594">XSL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-594">XSL</span></span></p></td>
<td><p><span data-ttu-id="ed1dd-595">SSPROP_STREAM_XSL</span><span class="sxs-lookup"><span data-stu-id="ed1dd-595">SSPROP_STREAM_XSL</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed1dd-596">Pour obtenir des détails spécifiques d'implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour SQL Server, consultez la documentation de ce produit dans la section OLE DB du kit de développement logiciel (SDK) de MDAC.</span><span class="sxs-lookup"><span data-stu-id="ed1dd-596">For specific implementation details and functional information about the Microsoft SQL Server OLE DB Provider, consult the OLE DB Provider for SQL Server documentation in the OLE DB section of the MDAC SDK.</span></span>

