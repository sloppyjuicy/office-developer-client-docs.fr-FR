---
title: Fournisseur Microsoft OLE DB pour ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 168799b517598211ca9de680730490a0a41d1dde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472460"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="b29d9-102">Fournisseur Microsoft OLE DB pour ODBC</span><span class="sxs-lookup"><span data-stu-id="b29d9-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="b29d9-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b29d9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b29d9-p101">Pour un programmeur ADO ou RDS, l'idéal serait que chaque source de données expose une interface OLE DB pour qu'ADO puisse effectuer les appels directement dans la source de données. Même si les fournisseurs de bases de données sont de plus en plus nombreux à implémenter les interfaces OLE DB, certaines sources de données ne sont pas encore exposées de cette façon. Toutefois, tous les systèmes SGBD utilisés aujourd'hui sont en principe accessibles via ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="b29d9-107">Il existe des pilotes ODBC pour les principaux SGBD utilisés aujourd'hui, dont Microsoft SQL Server, Microsoft Access (moteur de base de données Microsoft Jet) et Microsoft FoxPro, sans oublier les produits de base de données non-Microsoft comme Oracle.</span><span class="sxs-lookup"><span data-stu-id="b29d9-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="b29d9-p102">Le fournisseur Microsoft ODBC permet à ADO de se connecter à n'importe quelle source de données ODBC. Ce fournisseur est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="b29d9-p103">Le fournisseur prend en charge les transactions bien que les différents moteurs SGBD offrent différents types de prise en charge de ces transactions. Microsoft Access prend par exemple en charge jusqu'à cinq niveaux de transactions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="b29d9-112">Il s'agit du fournisseur par défaut pour ADO et toutes les propriétés et méthodes ADO spécifiques au fournisseur sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b29d9-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="b29d9-113">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="b29d9-113">Connection String Parameters</span></span>

<span data-ttu-id="b29d9-114">Pour vous connecter à ce fournisseur, définissez l'argument **Provider** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="b29d9-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="b29d9-115">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="b29d9-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="b29d9-116">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="b29d9-116">Typical Connection String</span></span>

<span data-ttu-id="b29d9-117">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="b29d9-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="b29d9-118">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="b29d9-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-119">Mot clé</span><span class="sxs-lookup"><span data-stu-id="b29d9-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="b29d9-120">Description</span><span class="sxs-lookup"><span data-stu-id="b29d9-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="b29d9-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="b29d9-122">Spécifie le fournisseur OLE DB pour ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="b29d9-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="b29d9-124">Spécifie le nom de la source de données.</span><span class="sxs-lookup"><span data-stu-id="b29d9-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="b29d9-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="b29d9-126">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b29d9-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="b29d9-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="b29d9-128">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b29d9-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="b29d9-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="b29d9-130">Spécifie l'URL d'un fichier ou d'un répertoire publié dans un dossier Web.</span><span class="sxs-lookup"><span data-stu-id="b29d9-130">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b29d9-131">Comme il s'agit du fournisseur par défaut pour ADO, si vous omettez de spécifier le paramètre **Provider=** dans la chaîne de connexion, ADO tentera d'établir une connexion vers ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b29d9-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="b29d9-p104">Ce fournisseur ne prend pas en charge de paramètre de connexion spécifique en plus des paramètres définis par ADO. Il transmettra toutefois tous les paramètres de connexion non-ADO au gestionnaire de pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="b29d9-p105">Comme vous n'êtes pas obligé de spécifier le paramètre **Provider**, vous pouvez composer une chaîne de connexion ADO identique à la chaîne de connexion ODBC pour la même source de données. Utilisez les mêmes noms de paramètre (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), les mêmes valeurs et la même syntaxe que pour composer une chaîne ODBC. Vous pouvez vous connecter avec ou sans nom de source de données (DSN) ou DSN de fichier (FileDSN).</span><span class="sxs-lookup"><span data-stu-id="b29d9-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="b29d9-137">**Syntaxe avec un DSN ou un FileDSN :**</span><span class="sxs-lookup"><span data-stu-id="b29d9-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="b29d9-138">**Syntaxe sans DSN (connexion sans DSN) :**</span><span class="sxs-lookup"><span data-stu-id="b29d9-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="b29d9-p106">Si vous utilisez un **DSN** ou un **FileDSN**, il doit être défini à travers l'administrateur de source de données ODBC dans le Panneau de configuration de Windows. Dans Microsoft Windows 2000, l'administrateur ODBC se trouve sous Outils d'administration. Dans les versions précédentes de Windows, l'icône de l'administrateur ODBC est appelée **ODBC 32 bits** ou simplement **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="b29d9-142">Plutôt que de définir un **DSN**, vous pouvez choisir de spécifier le pilote ODBC (**DRIVER=**), SQL Server par exemple, le nom du serveur (**SERVER=**) et le nom de la base de données (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="b29d9-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="b29d9-143">Vous pouvez aussi spécifier un nom de compte utilisateur (**UID=**) et le mot de passe de ce compte (**PWD=**) dans les paramètres spécifiques à ODBC ou dans les paramètres ADO standard *utilisateur* et *mot de passe*.</span><span class="sxs-lookup"><span data-stu-id="b29d9-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="b29d9-144">Bien que la définition d’un **DSN** déjà spécifie une base de données, vous pouvez spécifier *un* paramètre de *base de données* en plus un **DSN** pour se connecter à une autre base de données.</span><span class="sxs-lookup"><span data-stu-id="b29d9-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="b29d9-145">Il est conseillé de toujours inclure *le* paramètre de la *base de données* lorsque vous utilisez un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="b29d9-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="b29d9-146">Vous serez ainsi certain de vous connecter à la bonne base de données même si un autre utilisateur a modifié le paramètre de base de données par défaut depuis votre dernière vérification de la définition du **DSN**.</span><span class="sxs-lookup"><span data-stu-id="b29d9-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="b29d9-147">Propriétés de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="b29d9-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="b29d9-p108">Le fournisseur OLE DB pour ODBC ajoute plusieurs propriétés à la collection [Properties](properties-collection-ado.md) de l'objet **Connection**. Le tableau suivant répertorie chaque propriété en indiquant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-150">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="b29d9-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="b29d9-151">Description</span><span class="sxs-lookup"><span data-stu-id="b29d9-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-152">Procédures accessibles</span><span class="sxs-lookup"><span data-stu-id="b29d9-152">Accessible Procedures</span></span><br />
<span data-ttu-id="b29d9-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="b29d9-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-154">Indique si l'utilisateur a accès aux procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="b29d9-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-155">Table accessible</span><span class="sxs-lookup"><span data-stu-id="b29d9-155">Accessible Tables</span></span><br />
<span data-ttu-id="b29d9-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="b29d9-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-157">Indique si l'utilisateur a l'autorisation d'exécuter les instructions SELECT sur les tables de base de données.</span><span class="sxs-lookup"><span data-stu-id="b29d9-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-158">Instructions actives</span><span class="sxs-lookup"><span data-stu-id="b29d9-158">Active Statements</span></span><br />
<span data-ttu-id="b29d9-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-160">Indique le nombre de descripteurs qu'un pilote ODBC peut prendre en charge dans une connexion.</span><span class="sxs-lookup"><span data-stu-id="b29d9-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-161">Nom du pilote</span><span class="sxs-lookup"><span data-stu-id="b29d9-161">Driver Name</span></span><br />
<span data-ttu-id="b29d9-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="b29d9-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-163">Indique le nom de fichier du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-164">Version du pilote ODBC</span><span class="sxs-lookup"><span data-stu-id="b29d9-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="b29d9-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="b29d9-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-166">Indique la version d'ODBC prise en charge par ce pilote.</span><span class="sxs-lookup"><span data-stu-id="b29d9-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-167">Utilisation des fichiers</span><span class="sxs-lookup"><span data-stu-id="b29d9-167">File Usage</span></span><br />
<span data-ttu-id="b29d9-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="b29d9-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-169">Indique le mode utilisé par le pilote pour traiter un fichier dans une source de données : table ou catalogue.</span><span class="sxs-lookup"><span data-stu-id="b29d9-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-170">Comme la Clause d’échappement</span><span class="sxs-lookup"><span data-stu-id="b29d9-170">Like Escape Clause</span></span><br />
<span data-ttu-id="b29d9-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="b29d9-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-172">Indique si le pilote prend en charge la définition et l'utilisation du caractère d'échappement pour le caractère de pourcentage (%) et le caractère de soulignement (_) dans le prédicat LIKE d'une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="b29d9-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-173">Nombre maximal de colonnes dans le groupe de</span><span class="sxs-lookup"><span data-stu-id="b29d9-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="b29d9-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="b29d9-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-175">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la clause GROUP BY d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="b29d9-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-176">Nombre maximal de colonnes dans l’Index</span><span class="sxs-lookup"><span data-stu-id="b29d9-176">Max Columns in Index</span></span><br />
<span data-ttu-id="b29d9-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="b29d9-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-178">Indique le nombre maximal de colonnes qui peuvent être incluses dans un index.</span><span class="sxs-lookup"><span data-stu-id="b29d9-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-179">Nombre maximal de colonnes en les classant par</span><span class="sxs-lookup"><span data-stu-id="b29d9-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="b29d9-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="b29d9-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-181">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la clause ORDER BY d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="b29d9-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-182">Nombre maximal de colonnes dans, sélectionnez</span><span class="sxs-lookup"><span data-stu-id="b29d9-182">Max Columns in Select</span></span><br />
<span data-ttu-id="b29d9-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="b29d9-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-184">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la partie SELECT d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="b29d9-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-185">Nombre maximal de colonnes dans un tableau</span><span class="sxs-lookup"><span data-stu-id="b29d9-185">Max Columns in Table</span></span><br />
<span data-ttu-id="b29d9-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="b29d9-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-187">Indique le nombre maximal de colonnes autorisé dans une table.</span><span class="sxs-lookup"><span data-stu-id="b29d9-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-188">Fonctions numériques</span><span class="sxs-lookup"><span data-stu-id="b29d9-188">Numeric Functions</span></span><br />
<span data-ttu-id="b29d9-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-p109">Indique les fonctions numériques prises en charge par le pilote ODBC.

Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-192">Fonctionnalités de jointure externe</span><span class="sxs-lookup"><span data-stu-id="b29d9-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="b29d9-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="b29d9-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-194">Indique les types de jointures externes (OUTER JOIN) prises en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b29d9-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-195">Jointures externes</span><span class="sxs-lookup"><span data-stu-id="b29d9-195">Outer Joins</span></span><br />
<span data-ttu-id="b29d9-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-197">Indique si le fournisseur prend en charge les jointures externes (OUTER JOIN).</span><span class="sxs-lookup"><span data-stu-id="b29d9-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-198">Caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="b29d9-198">Special Characters</span></span><br />
<span data-ttu-id="b29d9-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-200">Indique les caractères ayant une signification spéciale pour le pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-201">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="b29d9-201">Stored Procedures</span></span><br />
<span data-ttu-id="b29d9-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="b29d9-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-203">Indique si les procédures stockées peuvent être utilisées avec ce pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-204">Fonctions de chaîne</span><span class="sxs-lookup"><span data-stu-id="b29d9-204">String Functions</span></span><br />
<span data-ttu-id="b29d9-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-p110">Indique les fonctions de chaîne prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-208">Fonctions du système</span><span class="sxs-lookup"><span data-stu-id="b29d9-208">System Functions</span></span><br />
<span data-ttu-id="b29d9-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-p111">Indique les fonctions système prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-212">Fonctions de Date/heure</span><span class="sxs-lookup"><span data-stu-id="b29d9-212">Time/Date Functions</span></span><br />
<span data-ttu-id="b29d9-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="b29d9-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-p112">Indique les fonctions de date et heure prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-216">Prise en charge de la grammaire SQL</span><span class="sxs-lookup"><span data-stu-id="b29d9-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="b29d9-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="b29d9-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-218">Indique la grammaire SQL prise en charge par le pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="b29d9-219">Propriétés spécifiques au fournisseur pour le jeu d'enregistrement et la commande</span><span class="sxs-lookup"><span data-stu-id="b29d9-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="b29d9-p113">Le fournisseur OLE DB pour ODBC ajoute plusieurs propriétés à la collection **Properties** des objets **Recordset** et **Command**. Le tableau suivant répertorie chaque propriété en indiquant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-222">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="b29d9-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="b29d9-223">Description</span><span class="sxs-lookup"><span data-stu-id="b29d9-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-224">Mises à jour/suppression/insère fondés sur une requête</span><span class="sxs-lookup"><span data-stu-id="b29d9-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="b29d9-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="b29d9-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-226">Indique s'il est possible d'utiliser des requêtes SQL pour effectuer des mises à jour, des suppressions ou des insertions.</span><span class="sxs-lookup"><span data-stu-id="b29d9-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-227">Type d’accès concurrentiel ODBC</span><span class="sxs-lookup"><span data-stu-id="b29d9-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="b29d9-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="b29d9-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-229">Indique la méthode utilisée pour réduire les problèmes susceptibles de se produire si deux utilisateurs tentent d'accéder simultanément aux mêmes données de la source de données.</span><span class="sxs-lookup"><span data-stu-id="b29d9-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-230">Accessibilité des objets BLOB sur curseur avant uniquement</span><span class="sxs-lookup"><span data-stu-id="b29d9-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="b29d9-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="b29d9-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-232">Indique si les <strong>champs</strong> BLOB sont accessibles avec un curseur de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="b29d9-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-233">Inclure les valeurs SQL_FLOAT, SQL_DOUBLE et SQL_REAL dans QBU WHERE clauses</span><span class="sxs-lookup"><span data-stu-id="b29d9-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="b29d9-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="b29d9-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-235">Indique si les valeurs SQL_FLOAT, SQL_DOUBLE et SQL_REAL peuvent être incluses dans une clause QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="b29d9-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-236">Position dans la dernière ligne après insertion</span><span class="sxs-lookup"><span data-stu-id="b29d9-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="b29d9-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="b29d9-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-238">Indique qu'après insertion d'un nouvel enregistrement dans une table, la dernière ligne de la table est activée.</span><span class="sxs-lookup"><span data-stu-id="b29d9-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="b29d9-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="b29d9-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-241">Indique si l'interface <strong>IRowsetChange</strong> fournit la prise en charge des informations étendues.</span><span class="sxs-lookup"><span data-stu-id="b29d9-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-242">Type de curseur ODBC</span><span class="sxs-lookup"><span data-stu-id="b29d9-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="b29d9-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="b29d9-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-244">Indique le type de curseur utilisé par le <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="b29d9-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-245">Générer un jeu de lignes qui peut être marshalé.</span><span class="sxs-lookup"><span data-stu-id="b29d9-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="b29d9-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="b29d9-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="b29d9-247">Indique que le pilote ODBC génère un jeu d'enregistrements qui peut être marshalé.</span><span class="sxs-lookup"><span data-stu-id="b29d9-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="b29d9-248">Texte de la commande</span><span class="sxs-lookup"><span data-stu-id="b29d9-248">Command Text</span></span>

<span data-ttu-id="b29d9-249">La façon dont vous utilisez l'objet [Command](command-object-ado.md) dépend en grande partie de la source de données et du type de requête ou de commande qu'elle accepte.</span><span class="sxs-lookup"><span data-stu-id="b29d9-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="b29d9-250">ODBC fournit une syntaxe spécifique pour appeler les procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="b29d9-250">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="b29d9-251">Pour la propriété [CommandText](commandtext-property-ado.md) d’un objet **Command** , l’argument *CommandText* de la méthode **Execute** sur un objet [Connection](connection-object-ado.md) ou l’argument *Source* à la méthode **Open** sur un [objet Recordset](recordset-object-ado.md) objet, il passe dans une chaîne avec la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b29d9-251">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="b29d9-p115">Chaque **?** fait référence à un objet de la collection [Parameters](parameters-collection-ado.md). Le premier **?** fait référence à l’objet **Parameters** (0), le **?** suivant fait référence à l’objet **Parameters** (1) et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b29d9-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="b29d9-p116">Les références aux paramètres sont facultatives et dépendent de la structure de la procédure stockée. Si vous voulez appeler une procédure stockée qui ne définisse aucun paramètre, votre chaîne doit présenter la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b29d9-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="b29d9-259">Si vous avez deux paramètres de requête, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b29d9-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="b29d9-p117">Si la procédure stockée renvoie une valeur, cette valeur sera traitée comme un paramètre supplémentaire. Si vous n'avez pas de paramètre de requête mais que vous avez une valeur de renvoi, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b29d9-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="b29d9-262">Enfin, si vous avez une valeur de renvoi et deux paramètres de requête, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b29d9-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="b29d9-263">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="b29d9-263">Recordset Behavior</span></span>

<span data-ttu-id="b29d9-264">Les tableaux suivants répertorient les méthodes et propriétés ADO standard disponibles pour un objet **Recordset** ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b29d9-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="b29d9-265">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection **Properties** du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b29d9-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="b29d9-266">Disponibilité des propriétés ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="b29d9-266">Availability of standard ADO **Recordset** properties:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-267">Propriété</span><span class="sxs-lookup"><span data-stu-id="b29d9-267">Property</span></span></p></th>
<th><p><span data-ttu-id="b29d9-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="b29d9-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="b29d9-269">Dynamic</span><span class="sxs-lookup"><span data-stu-id="b29d9-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="b29d9-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="b29d9-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="b29d9-271">Static</span><span class="sxs-lookup"><span data-stu-id="b29d9-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-273">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-273">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-274">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-274">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-275">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-276">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-278">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-278">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-279">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-279">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-280">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-281">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-283">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-284">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-285">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-286">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-288">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-289">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-290">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-291">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-293">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-293">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-294">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-294">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-295">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-296">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-298">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-299">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-300">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-301">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-303">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-304">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-305">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-306">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-308">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-309">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-310">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-311">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-313">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-314">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-315">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-316">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-317"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-318">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-319">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-320">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-321">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-323">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-324">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-325">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-326">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-328">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-329">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-330">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-331">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-333">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-334">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-335">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-336">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-338">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-339">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-339">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-340">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-341">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-343">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-344">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-345">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-346">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-348">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-349">Non disponible</span><span class="sxs-lookup"><span data-stu-id="b29d9-349">not available</span></span></p></td>
<td><p><span data-ttu-id="b29d9-350">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-351">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-353">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-354">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-355">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="b29d9-356">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b29d9-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-357"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-358">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-359">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-360">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-361">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-362"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-363">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-364">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-365">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="b29d9-366">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b29d9-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b29d9-367">Les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [AbsolutePage](absolutepage-property-ado.md) sont en écriture seule lorsqu'ADO est utilisé avec la version 1.0 du fournisseur Microsoft OLE DB pour ODBC.</span><span class="sxs-lookup"><span data-stu-id="b29d9-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="b29d9-368">Disponibilité des méthodes ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="b29d9-368">Availability of standard ADO **Recordset** methods:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-369">Méthode</span><span class="sxs-lookup"><span data-stu-id="b29d9-369">Method</span></span></p></th>
<th><p><span data-ttu-id="b29d9-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="b29d9-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="b29d9-371">Dynamic</span><span class="sxs-lookup"><span data-stu-id="b29d9-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="b29d9-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="b29d9-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="b29d9-373">Static</span><span class="sxs-lookup"><span data-stu-id="b29d9-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-375">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-376">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-377">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-378">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-380">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-381">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-382">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-383">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-385">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-386">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-387">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-388">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-390">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-391">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-392">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-393">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-395">Non</span><span class="sxs-lookup"><span data-stu-id="b29d9-395">No</span></span></p></td>
<td><p><span data-ttu-id="b29d9-396">Non</span><span class="sxs-lookup"><span data-stu-id="b29d9-396">No</span></span></p></td>
<td><p><span data-ttu-id="b29d9-397">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-398">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-400">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-401">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-402">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-403">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-404"><a href="delete-method-ado-recordset.md">Supprimer</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-405">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-406">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-407">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-408">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-410">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-411">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-412">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-413">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-414"><a href="move-method-ado.md">Déplacer</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-415">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-416">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-417">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-418">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-420">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-421">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-422">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-423">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-425">Non</span><span class="sxs-lookup"><span data-stu-id="b29d9-425">No</span></span></p></td>
<td><p><span data-ttu-id="b29d9-426">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-427">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-428">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-430">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-431">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-432">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-433">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-435">Non</span><span class="sxs-lookup"><span data-stu-id="b29d9-435">No</span></span></p></td>
<td><p><span data-ttu-id="b29d9-436">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-437">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-438">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="b29d9-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="b29d9-440">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-441">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-442">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-443">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-445">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-446">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-447">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-448">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-449"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-450">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-451">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-452">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-453">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-455">Non</span><span class="sxs-lookup"><span data-stu-id="b29d9-455">No</span></span></p></td>
<td><p><span data-ttu-id="b29d9-456">Non</span><span class="sxs-lookup"><span data-stu-id="b29d9-456">No</span></span></p></td>
<td><p><span data-ttu-id="b29d9-457">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-458">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-459"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-460">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-461">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-462">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-463">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-464"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-465">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-466">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-467">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-468">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="b29d9-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="b29d9-470">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-471">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-472">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-473">Oui</span><span class="sxs-lookup"><span data-stu-id="b29d9-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b29d9-474">\*Non prise en charge avec les bases de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b29d9-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="b29d9-475">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="b29d9-475">Dynamic Properties</span></span>

<span data-ttu-id="b29d9-476">Le fournisseur OLE DB pour ODBC insère plusieurs propriétés dynamiques dans la collection **Properties** des objets [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) et [Command](command-object-ado.md) non ouverts.</span><span class="sxs-lookup"><span data-stu-id="b29d9-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="b29d9-p118">Les tableaux suivants forment un index croisé des noms ADO et OLE DB de chaque propriété dynamique. Le guide OLE DB Programmer's Reference (en anglais) référence les noms de propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés. Recherchez le nom de la propriété OLE DB dans l'Index ou consultez la rubrique « Appendix C: OLE DB Properties ».</span><span class="sxs-lookup"><span data-stu-id="b29d9-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="b29d9-481">Propriétés dynamiques de connexion</span><span class="sxs-lookup"><span data-stu-id="b29d9-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="b29d9-482">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="b29d9-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-483">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="b29d9-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b29d9-484">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="b29d9-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="b29d9-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="b29d9-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="b29d9-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="b29d9-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="b29d9-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="b29d9-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="b29d9-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="b29d9-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="b29d9-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="b29d9-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="b29d9-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="b29d9-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="b29d9-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="b29d9-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="b29d9-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="b29d9-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="b29d9-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="b29d9-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="b29d9-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="b29d9-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b29d9-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="b29d9-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="b29d9-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b29d9-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="b29d9-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="b29d9-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="b29d9-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="b29d9-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="b29d9-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="b29d9-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="b29d9-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="b29d9-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="b29d9-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="b29d9-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b29d9-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b29d9-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="b29d9-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="b29d9-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="b29d9-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="b29d9-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="b29d9-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="b29d9-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="b29d9-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="b29d9-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="b29d9-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="b29d9-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="b29d9-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="b29d9-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="b29d9-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="b29d9-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="b29d9-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b29d9-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="b29d9-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="b29d9-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="b29d9-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="b29d9-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="b29d9-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="b29d9-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="b29d9-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="b29d9-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="b29d9-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="b29d9-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="b29d9-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="b29d9-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="b29d9-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-529">Location</span><span class="sxs-lookup"><span data-stu-id="b29d9-529">Location</span></span></p></td>
<td><p><span data-ttu-id="b29d9-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="b29d9-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="b29d9-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="b29d9-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="b29d9-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="b29d9-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="b29d9-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="b29d9-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="b29d9-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="b29d9-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="b29d9-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="b29d9-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="b29d9-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="b29d9-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-539">Mode</span><span class="sxs-lookup"><span data-stu-id="b29d9-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="b29d9-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="b29d9-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="b29d9-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="b29d9-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="b29d9-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="b29d9-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="b29d9-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="b29d9-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b29d9-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="b29d9-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="b29d9-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="b29d9-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="b29d9-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="b29d9-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="b29d9-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="b29d9-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="b29d9-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b29d9-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="b29d9-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="b29d9-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="b29d9-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="b29d9-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="b29d9-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="b29d9-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="b29d9-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="b29d9-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="b29d9-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="b29d9-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b29d9-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="b29d9-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="b29d9-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="b29d9-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="b29d9-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="b29d9-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-565">Password</span><span class="sxs-lookup"><span data-stu-id="b29d9-565">Password</span></span></p></td>
<td><p><span data-ttu-id="b29d9-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="b29d9-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="b29d9-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="b29d9-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="b29d9-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="b29d9-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="b29d9-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="b29d9-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="b29d9-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="b29d9-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="b29d9-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="b29d9-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="b29d9-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b29d9-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="b29d9-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="b29d9-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="b29d9-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="b29d9-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="b29d9-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="b29d9-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="b29d9-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="b29d9-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="b29d9-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="b29d9-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="b29d9-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="b29d9-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="b29d9-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="b29d9-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="b29d9-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="b29d9-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="b29d9-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="b29d9-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="b29d9-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="b29d9-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="b29d9-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="b29d9-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="b29d9-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="b29d9-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="b29d9-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="b29d9-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="b29d9-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="b29d9-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="b29d9-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="b29d9-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="b29d9-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b29d9-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="b29d9-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="b29d9-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="b29d9-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="b29d9-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="b29d9-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="b29d9-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="b29d9-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="b29d9-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="b29d9-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="b29d9-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="b29d9-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-605">User ID</span><span class="sxs-lookup"><span data-stu-id="b29d9-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="b29d9-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="b29d9-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-607">User Name</span><span class="sxs-lookup"><span data-stu-id="b29d9-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="b29d9-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="b29d9-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="b29d9-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="b29d9-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="b29d9-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="b29d9-611">Propriétés dynamiques du jeu d'enregitrements</span><span class="sxs-lookup"><span data-stu-id="b29d9-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="b29d9-612">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b29d9-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-613">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="b29d9-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b29d9-614">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="b29d9-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="b29d9-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="b29d9-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="b29d9-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="b29d9-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b29d9-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="b29d9-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="b29d9-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="b29d9-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="b29d9-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="b29d9-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="b29d9-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="b29d9-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="b29d9-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b29d9-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="b29d9-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="b29d9-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="b29d9-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="b29d9-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="b29d9-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b29d9-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="b29d9-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="b29d9-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="b29d9-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="b29d9-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="b29d9-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b29d9-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="b29d9-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b29d9-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="b29d9-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="b29d9-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="b29d9-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="b29d9-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b29d9-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="b29d9-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b29d9-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b29d9-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b29d9-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="b29d9-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b29d9-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="b29d9-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b29d9-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="b29d9-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b29d9-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="b29d9-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b29d9-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b29d9-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="b29d9-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b29d9-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="b29d9-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b29d9-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b29d9-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b29d9-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="b29d9-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="b29d9-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="b29d9-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="b29d9-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="b29d9-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="b29d9-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="b29d9-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="b29d9-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="b29d9-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="b29d9-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="b29d9-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="b29d9-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="b29d9-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="b29d9-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="b29d9-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="b29d9-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b29d9-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="b29d9-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="b29d9-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b29d9-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="b29d9-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="b29d9-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="b29d9-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="b29d9-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="b29d9-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="b29d9-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="b29d9-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="b29d9-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="b29d9-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="b29d9-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="b29d9-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="b29d9-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="b29d9-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="b29d9-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b29d9-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="b29d9-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="b29d9-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b29d9-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b29d9-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b29d9-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="b29d9-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="b29d9-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="b29d9-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="b29d9-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="b29d9-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b29d9-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b29d9-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b29d9-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="b29d9-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="b29d9-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="b29d9-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="b29d9-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b29d9-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b29d9-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b29d9-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="b29d9-734">Propriétés dynamiques de la commande</span><span class="sxs-lookup"><span data-stu-id="b29d9-734">Command Dynamic Properties</span></span>

<span data-ttu-id="b29d9-735">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="b29d9-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b29d9-736">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="b29d9-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="b29d9-737">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="b29d9-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="b29d9-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="b29d9-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="b29d9-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="b29d9-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="b29d9-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="b29d9-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="b29d9-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="b29d9-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="b29d9-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="b29d9-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="b29d9-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="b29d9-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="b29d9-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b29d9-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="b29d9-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="b29d9-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="b29d9-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="b29d9-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="b29d9-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b29d9-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="b29d9-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="b29d9-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="b29d9-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="b29d9-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="b29d9-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b29d9-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="b29d9-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="b29d9-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="b29d9-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="b29d9-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="b29d9-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="b29d9-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="b29d9-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b29d9-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="b29d9-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="b29d9-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b29d9-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="b29d9-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="b29d9-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b29d9-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="b29d9-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="b29d9-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="b29d9-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b29d9-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="b29d9-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="b29d9-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b29d9-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="b29d9-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="b29d9-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="b29d9-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="b29d9-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b29d9-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b29d9-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b29d9-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="b29d9-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="b29d9-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="b29d9-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="b29d9-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="b29d9-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="b29d9-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="b29d9-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="b29d9-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="b29d9-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="b29d9-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="b29d9-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="b29d9-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="b29d9-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="b29d9-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="b29d9-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="b29d9-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="b29d9-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b29d9-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="b29d9-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="b29d9-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b29d9-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="b29d9-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="b29d9-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="b29d9-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="b29d9-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="b29d9-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="b29d9-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="b29d9-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="b29d9-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="b29d9-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="b29d9-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="b29d9-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="b29d9-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="b29d9-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="b29d9-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="b29d9-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="b29d9-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="b29d9-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="b29d9-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="b29d9-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="b29d9-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="b29d9-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="b29d9-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="b29d9-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="b29d9-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="b29d9-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="b29d9-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="b29d9-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="b29d9-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="b29d9-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="b29d9-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="b29d9-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="b29d9-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="b29d9-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b29d9-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b29d9-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="b29d9-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="b29d9-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="b29d9-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b29d9-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="b29d9-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="b29d9-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="b29d9-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b29d9-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="b29d9-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="b29d9-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="b29d9-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b29d9-855">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b29d9-855">See also</span></span>

<span data-ttu-id="b29d9-856">Pour plus d’informations concernant l’implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour ODBC, consultez le [Guide du programmeur OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) ou visitez le [Centre de développement de plateforme de données](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="b29d9-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

