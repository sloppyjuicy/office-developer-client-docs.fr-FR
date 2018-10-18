---
title: Fournisseur Microsoft OLE DB pour ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0098e646ea48656f44bd3ccd380ae41efc94ffba
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606937"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="bd7f0-102">Fournisseur Microsoft OLE DB pour ODBC</span><span class="sxs-lookup"><span data-stu-id="bd7f0-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="bd7f0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd7f0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd7f0-p101">Pour un programmeur ADO ou RDS, l'idéal serait que chaque source de données expose une interface OLE DB pour qu'ADO puisse effectuer les appels directement dans la source de données. Même si les fournisseurs de bases de données sont de plus en plus nombreux à implémenter les interfaces OLE DB, certaines sources de données ne sont pas encore exposées de cette façon. Toutefois, tous les systèmes SGBD utilisés aujourd'hui sont en principe accessibles via ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="bd7f0-107">Il existe des pilotes ODBC pour les principaux SGBD utilisés aujourd'hui, dont Microsoft SQL Server, Microsoft Access (moteur de base de données Microsoft Jet) et Microsoft FoxPro, sans oublier les produits de base de données non-Microsoft comme Oracle.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="bd7f0-p102">Le fournisseur Microsoft ODBC permet à ADO de se connecter à n'importe quelle source de données ODBC. Ce fournisseur est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="bd7f0-p103">Le fournisseur prend en charge les transactions bien que les différents moteurs SGBD offrent différents types de prise en charge de ces transactions. Microsoft Access prend par exemple en charge jusqu'à cinq niveaux de transactions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="bd7f0-112">Il s'agit du fournisseur par défaut pour ADO et toutes les propriétés et méthodes ADO spécifiques au fournisseur sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="bd7f0-113">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="bd7f0-113">Connection String Parameters</span></span>

<span data-ttu-id="bd7f0-114">Pour vous connecter à ce fournisseur, définissez l'argument **Provider** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="bd7f0-115">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="bd7f0-116">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="bd7f0-116">Typical Connection String</span></span>

<span data-ttu-id="bd7f0-117">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="bd7f0-118">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd7f0-119">Mot clé</span><span class="sxs-lookup"><span data-stu-id="bd7f0-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-120">Description</span><span class="sxs-lookup"><span data-stu-id="bd7f0-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="bd7f0-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-122">Spécifie le fournisseur OLE DB pour ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="bd7f0-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-124">Spécifie le nom de la source de données.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="bd7f0-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-126">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="bd7f0-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-128">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="bd7f0-129"><strong>URL</strong></span></span></p></td>
<span data-ttu-id="bd7f0-130"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bd7f0-130"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="bd7f0-131">Spécifie l'URL d'un fichier ou d'un répertoire publié dans un dossier Web.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-131">Specifies the URL of a file or directory published in a Web folder.</span></span></p></td>
=======
<td><p><span data-ttu-id="bd7f0-132">Spécifie l’URL d’un fichier ou un répertoire publié dans un dossier web.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-132">Specifies the URL of a file or directory published in a web folder.</span></span></p></td><span data-ttu-id="bd7f0-133">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="bd7f0-133">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="bd7f0-134">Comme il s'agit du fournisseur par défaut pour ADO, si vous omettez de spécifier le paramètre **Provider=** dans la chaîne de connexion, ADO tentera d'établir une connexion vers ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-134">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="bd7f0-p104">Ce fournisseur ne prend pas en charge de paramètre de connexion spécifique en plus des paramètres définis par ADO. Il transmettra toutefois tous les paramètres de connexion non-ADO au gestionnaire de pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="bd7f0-p105">Comme vous n'êtes pas obligé de spécifier le paramètre **Provider**, vous pouvez composer une chaîne de connexion ADO identique à la chaîne de connexion ODBC pour la même source de données. Utilisez les mêmes noms de paramètre (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), les mêmes valeurs et la même syntaxe que pour composer une chaîne ODBC. Vous pouvez vous connecter avec ou sans nom de source de données (DSN) ou DSN de fichier (FileDSN).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="bd7f0-140">**Syntaxe avec un DSN ou un FileDSN :**</span><span class="sxs-lookup"><span data-stu-id="bd7f0-140">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="bd7f0-141">**Syntaxe sans DSN (connexion sans DSN) :**</span><span class="sxs-lookup"><span data-stu-id="bd7f0-141">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="bd7f0-p106">Si vous utilisez un **DSN** ou un **FileDSN**, il doit être défini à travers l'administrateur de source de données ODBC dans le Panneau de configuration de Windows. Dans Microsoft Windows 2000, l'administrateur ODBC se trouve sous Outils d'administration. Dans les versions précédentes de Windows, l'icône de l'administrateur ODBC est appelée **ODBC 32 bits** ou simplement **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="bd7f0-145">Plutôt que de définir un **DSN**, vous pouvez choisir de spécifier le pilote ODBC (**DRIVER=**), SQL Server par exemple, le nom du serveur (**SERVER=**) et le nom de la base de données (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-145">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="bd7f0-146">Vous pouvez aussi spécifier un nom de compte utilisateur (**UID=**) et le mot de passe de ce compte (**PWD=**) dans les paramètres spécifiques à ODBC ou dans les paramètres ADO standard *utilisateur* et *mot de passe*.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-146">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="bd7f0-147">Bien que la définition d’un **DSN** déjà spécifie une base de données, vous pouvez spécifier *un* paramètre de *base de données* en plus un **DSN** pour se connecter à une autre base de données.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-147">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="bd7f0-148">Il est conseillé de toujours inclure *le* paramètre de la *base de données* lorsque vous utilisez un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-148">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="bd7f0-149">Vous serez ainsi certain de vous connecter à la bonne base de données même si un autre utilisateur a modifié le paramètre de base de données par défaut depuis votre dernière vérification de la définition du **DSN**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-149">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="bd7f0-150">Propriétés de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="bd7f0-150">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="bd7f0-p108">Le fournisseur OLE DB pour ODBC ajoute plusieurs propriétés à la collection [Properties](properties-collection-ado.md) de l'objet **Connection**. Le tableau suivant répertorie chaque propriété en indiquant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd7f0-153">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="bd7f0-153">Property Name</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-154">Description</span><span class="sxs-lookup"><span data-stu-id="bd7f0-154">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-155">Procédures accessibles</span><span class="sxs-lookup"><span data-stu-id="bd7f0-155">Accessible Procedures</span></span><br />
<span data-ttu-id="bd7f0-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-156">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-157">Indique si l'utilisateur a accès aux procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-157">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-158">Table accessible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-158">Accessible Tables</span></span><br />
<span data-ttu-id="bd7f0-159">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-159">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-160">Indique si l'utilisateur a l'autorisation d'exécuter les instructions SELECT sur les tables de base de données.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-160">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-161">Instructions actives</span><span class="sxs-lookup"><span data-stu-id="bd7f0-161">Active Statements</span></span><br />
<span data-ttu-id="bd7f0-162">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-162">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-163">Indique le nombre de descripteurs qu'un pilote ODBC peut prendre en charge dans une connexion.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-163">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-164">Nom du pilote</span><span class="sxs-lookup"><span data-stu-id="bd7f0-164">Driver Name</span></span><br />
<span data-ttu-id="bd7f0-165">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-165">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-166">Indique le nom de fichier du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-166">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-167">Version du pilote ODBC</span><span class="sxs-lookup"><span data-stu-id="bd7f0-167">Driver ODBC Version</span></span><br />
<span data-ttu-id="bd7f0-168">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-168">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-169">Indique la version d'ODBC prise en charge par ce pilote.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-169">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-170">Utilisation des fichiers</span><span class="sxs-lookup"><span data-stu-id="bd7f0-170">File Usage</span></span><br />
<span data-ttu-id="bd7f0-171">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-171">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-172">Indique le mode utilisé par le pilote pour traiter un fichier dans une source de données : table ou catalogue.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-172">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-173">Comme la Clause d’échappement</span><span class="sxs-lookup"><span data-stu-id="bd7f0-173">Like Escape Clause</span></span><br />
<span data-ttu-id="bd7f0-174">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-174">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-175">Indique si le pilote prend en charge la définition et l'utilisation du caractère d'échappement pour le caractère de pourcentage (%) et le caractère de soulignement (_) dans le prédicat LIKE d'une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-175">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-176">Nombre maximal de colonnes dans le groupe de</span><span class="sxs-lookup"><span data-stu-id="bd7f0-176">Max Columns in Group By</span></span><br />
<span data-ttu-id="bd7f0-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-177">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-178">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la clause GROUP BY d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-178">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-179">Nombre maximal de colonnes dans l’Index</span><span class="sxs-lookup"><span data-stu-id="bd7f0-179">Max Columns in Index</span></span><br />
<span data-ttu-id="bd7f0-180">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-180">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-181">Indique le nombre maximal de colonnes qui peuvent être incluses dans un index.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-181">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-182">Nombre maximal de colonnes en les classant par</span><span class="sxs-lookup"><span data-stu-id="bd7f0-182">Max Columns in Order By</span></span><br />
<span data-ttu-id="bd7f0-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-183">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-184">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la clause ORDER BY d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-184">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-185">Nombre maximal de colonnes dans, sélectionnez</span><span class="sxs-lookup"><span data-stu-id="bd7f0-185">Max Columns in Select</span></span><br />
<span data-ttu-id="bd7f0-186">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-186">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-187">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la partie SELECT d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-187">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-188">Nombre maximal de colonnes dans un tableau</span><span class="sxs-lookup"><span data-stu-id="bd7f0-188">Max Columns in Table</span></span><br />
<span data-ttu-id="bd7f0-189">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-189">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-190">Indique le nombre maximal de colonnes autorisé dans une table.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-190">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-191">Fonctions numériques</span><span class="sxs-lookup"><span data-stu-id="bd7f0-191">Numeric Functions</span></span><br />
<span data-ttu-id="bd7f0-192">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-192">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-p109">Indique les fonctions numériques prises en charge par le pilote ODBC.

Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-195">Fonctionnalités de jointure externe</span><span class="sxs-lookup"><span data-stu-id="bd7f0-195">Outer Join Capabilities</span></span><br />
<span data-ttu-id="bd7f0-196">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-196">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-197">Indique les types de jointures externes (OUTER JOIN) prises en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-197">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-198">Jointures externes</span><span class="sxs-lookup"><span data-stu-id="bd7f0-198">Outer Joins</span></span><br />
<span data-ttu-id="bd7f0-199">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-199">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-200">Indique si le fournisseur prend en charge les jointures externes (OUTER JOIN).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-200">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-201">Caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="bd7f0-201">Special Characters</span></span><br />
<span data-ttu-id="bd7f0-202">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-202">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-203">Indique les caractères ayant une signification spéciale pour le pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-203">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-204">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="bd7f0-204">Stored Procedures</span></span><br />
<span data-ttu-id="bd7f0-205">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-205">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-206">Indique si les procédures stockées peuvent être utilisées avec ce pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-206">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-207">Fonctions de chaîne</span><span class="sxs-lookup"><span data-stu-id="bd7f0-207">String Functions</span></span><br />
<span data-ttu-id="bd7f0-208">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-208">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-p110">Indique les fonctions de chaîne prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-211">Fonctions du système</span><span class="sxs-lookup"><span data-stu-id="bd7f0-211">System Functions</span></span><br />
<span data-ttu-id="bd7f0-212">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-212">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-p111">Indique les fonctions système prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-215">Fonctions de Date/heure</span><span class="sxs-lookup"><span data-stu-id="bd7f0-215">Time/Date Functions</span></span><br />
<span data-ttu-id="bd7f0-216">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-216">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-p112">Indique les fonctions de date et heure prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-219">Prise en charge de la grammaire SQL</span><span class="sxs-lookup"><span data-stu-id="bd7f0-219">SQL Grammar Support</span></span><br />
<span data-ttu-id="bd7f0-220">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-220">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-221">Indique la grammaire SQL prise en charge par le pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-221">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="bd7f0-222">Propriétés spécifiques au fournisseur pour le jeu d'enregistrement et la commande</span><span class="sxs-lookup"><span data-stu-id="bd7f0-222">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="bd7f0-p113">Le fournisseur OLE DB pour ODBC ajoute plusieurs propriétés à la collection **Properties** des objets **Recordset** et **Command**. Le tableau suivant répertorie chaque propriété en indiquant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd7f0-225">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="bd7f0-225">Property Name</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-226">Description</span><span class="sxs-lookup"><span data-stu-id="bd7f0-226">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-227">Mises à jour/suppression/insère fondés sur une requête</span><span class="sxs-lookup"><span data-stu-id="bd7f0-227">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="bd7f0-228">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-228">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-229">Indique s'il est possible d'utiliser des requêtes SQL pour effectuer des mises à jour, des suppressions ou des insertions.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-229">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-230">Type d’accès concurrentiel ODBC</span><span class="sxs-lookup"><span data-stu-id="bd7f0-230">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="bd7f0-231">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-231">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-232">Indique la méthode utilisée pour réduire les problèmes susceptibles de se produire si deux utilisateurs tentent d'accéder simultanément aux mêmes données de la source de données.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-232">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-233">Accessibilité des objets BLOB sur curseur avant uniquement</span><span class="sxs-lookup"><span data-stu-id="bd7f0-233">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="bd7f0-234">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-234">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-235">Indique si les <strong>champs</strong> BLOB sont accessibles avec un curseur de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-235">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-236">Inclure les valeurs SQL_FLOAT, SQL_DOUBLE et SQL_REAL dans QBU WHERE clauses</span><span class="sxs-lookup"><span data-stu-id="bd7f0-236">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="bd7f0-237">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-237">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-238">Indique si les valeurs SQL_FLOAT, SQL_DOUBLE et SQL_REAL peuvent être incluses dans une clause QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-238">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-239">Position dans la dernière ligne après insertion</span><span class="sxs-lookup"><span data-stu-id="bd7f0-239">Position on the last row after insert</span></span><br />
<span data-ttu-id="bd7f0-240">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-240">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-241">Indique qu'après insertion d'un nouvel enregistrement dans une table, la dernière ligne de la table est activée.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-241">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-242">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-242">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="bd7f0-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-243">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-244">Indique si l'interface <strong>IRowsetChange</strong> fournit la prise en charge des informations étendues.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-244">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-245">Type de curseur ODBC</span><span class="sxs-lookup"><span data-stu-id="bd7f0-245">ODBC Cursor Type</span></span><br />
<span data-ttu-id="bd7f0-246">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-246">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-247">Indique le type de curseur utilisé par le <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-247">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-248">Générer un jeu de lignes qui peut être marshalé.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-248">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="bd7f0-249">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="bd7f0-249">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-250">Indique que le pilote ODBC génère un jeu d'enregistrements qui peut être marshalé.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-250">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="bd7f0-251">Texte de la commande</span><span class="sxs-lookup"><span data-stu-id="bd7f0-251">Command Text</span></span>

<span data-ttu-id="bd7f0-252">La façon dont vous utilisez l'objet [Command](command-object-ado.md) dépend en grande partie de la source de données et du type de requête ou de commande qu'elle accepte.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-252">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="bd7f0-253">ODBC fournit une syntaxe spécifique pour appeler les procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-253">ODBC provides a specific syntax for calling stored procedures.</span></span> <span data-ttu-id="bd7f0-254">Pour la propriété [CommandText](commandtext-property-ado.md) d’un objet **Command** , l’argument *CommandText* de la méthode **Execute** sur un objet [Connection](connection-object-ado.md) ou l’argument *Source* à la méthode **Open** sur un [objet Recordset](recordset-object-ado.md) objet, il passe dans une chaîne avec la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-254">For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="bd7f0-p115">Chaque **?** fait référence à un objet de la collection [Parameters](parameters-collection-ado.md). Le premier **?** fait référence à l’objet **Parameters** (0), le **?** suivant fait référence à l’objet **Parameters** (1) et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="bd7f0-p116">Les références aux paramètres sont facultatives et dépendent de la structure de la procédure stockée. Si vous voulez appeler une procédure stockée qui ne définisse aucun paramètre, votre chaîne doit présenter la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="bd7f0-262">Si vous avez deux paramètres de requête, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-262">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="bd7f0-p117">Si la procédure stockée renvoie une valeur, cette valeur sera traitée comme un paramètre supplémentaire. Si vous n'avez pas de paramètre de requête mais que vous avez une valeur de renvoi, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="bd7f0-265">Enfin, si vous avez une valeur de renvoi et deux paramètres de requête, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="bd7f0-265">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="bd7f0-266">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="bd7f0-266">Recordset Behavior</span></span>

<span data-ttu-id="bd7f0-267">Les tableaux suivants répertorient les méthodes et propriétés ADO standard disponibles pour un objet **Recordset** ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-267">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="bd7f0-268">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection **Properties** du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-268">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="bd7f0-269">Disponibilité des propriétés ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="bd7f0-269">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="bd7f0-270">Propriété</span><span class="sxs-lookup"><span data-stu-id="bd7f0-270">Property</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-271">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="bd7f0-271">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-272">Dynamic</span><span class="sxs-lookup"><span data-stu-id="bd7f0-272">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-273">Keyset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-273">Keyset</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-274">Static</span><span class="sxs-lookup"><span data-stu-id="bd7f0-274">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-275"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-276">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-276">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-277">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-277">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-278">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-278">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-279">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-279">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-280"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-281">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-281">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-282">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-282">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-283">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-284">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-284">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-285"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-286">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-286">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-287">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-287">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-288">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-288">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-289">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-289">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-290"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-290"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-291">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-291">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-292">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-292">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-293">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-293">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-294">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-294">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-295"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-295"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-296">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-296">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-297">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-297">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-298">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-299">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-299">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-300"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-300"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-301">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-301">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-302">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-302">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-303">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-304">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-304">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-305"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-306">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-306">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-307">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-307">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-308">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-309">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-309">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-310"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-310"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-311">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-311">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-312">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-312">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-313">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-313">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-314">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-314">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-315"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-315"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-316">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-316">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-317">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-317">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-318">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-318">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-319">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-319">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-320"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-320"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-321">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-321">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-322">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-322">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-323">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-324">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-324">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-325"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-325"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-326">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-326">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-327">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-327">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-328">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-329">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-329">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-330"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-331">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-331">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-332">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-332">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-333">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-334">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-334">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-335"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-336">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-336">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-337">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-337">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-338">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-339">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-339">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-340"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-340"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-341">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-341">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-342">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-342">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-343">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-343">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-344">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-344">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-345"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-345"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-346">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-346">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-347">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-347">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-348">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-349">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-349">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-350"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-350"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-351">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-351">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-352">Non disponible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-352">not available</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-353">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-353">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-354">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-354">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-355"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-355"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-356">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-356">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-357">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-357">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-358">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-358">read/write</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-359">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd7f0-359">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-360"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-360"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-361">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-361">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-362">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-362">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-363">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-364">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-364">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-365"><a href="status-property-ado-recordset.md">Status</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-365"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-366">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-366">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-367">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-367">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-368">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-368">read-only</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-369">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd7f0-369">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd7f0-370">Les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [AbsolutePage](absolutepage-property-ado.md) sont en écriture seule lorsqu'ADO est utilisé avec la version 1.0 du fournisseur Microsoft OLE DB pour ODBC.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-370">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="bd7f0-371">Disponibilité des méthodes ADO standard d'un **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="bd7f0-371">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="bd7f0-372">Méthode</span><span class="sxs-lookup"><span data-stu-id="bd7f0-372">Method</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-373">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="bd7f0-373">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-374">Dynamic</span><span class="sxs-lookup"><span data-stu-id="bd7f0-374">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-375">Keyset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-375">Keyset</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-376">Static</span><span class="sxs-lookup"><span data-stu-id="bd7f0-376">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-377"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-377"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-378">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-378">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-379">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-379">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-380">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-381">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-382"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-382"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-383">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-383">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-384">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-384">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-385">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-386">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-386">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-387"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-388">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-388">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-389">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-389">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-390">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-391">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-391">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-392"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-393">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-393">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-394">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-394">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-395">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-395">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-396">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-396">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-397"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-397"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-398">Non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-398">No</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-399">Non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-399">No</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-400">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-401">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-401">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-402"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-402"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-403">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-403">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-404">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-404">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-405">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-406">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-406">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-407"><a href="delete-method-ado-recordset.md">Delete</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-407"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-408">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-408">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-409">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-409">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-410">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-411">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-411">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-412"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-412"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-413">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-413">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-414">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-414">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-415">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-416">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-416">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-417"><a href="move-method-ado.md">Déplacer</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-417"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-418">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-418">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-419">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-419">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-420">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-421">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-421">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-422"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-423">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-423">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-424">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-424">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-425">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-425">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-426">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-426">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-427"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-428">Non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-428">No</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-429">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-429">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-430">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-431">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-431">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-432"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-433">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-433">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-434">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-434">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-435">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-435">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-436">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-436">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-437"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-438">Non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-438">No</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-439">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-439">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-440">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-441">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="bd7f0-442"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-443">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-443">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-444">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-444">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-445">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-446">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-446">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-447"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-447"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-448">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-448">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-449">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-449">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-450">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-451">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-451">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-452"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-452"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-453">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-453">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-454">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-454">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-455">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-455">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-456">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-456">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-457"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-457"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-458">Non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-458">No</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-459">Non</span><span class="sxs-lookup"><span data-stu-id="bd7f0-459">No</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-460">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-461">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-461">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-462"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-462"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-463">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-463">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-464">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-464">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-465">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-466">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-466">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-467"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-467"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-468">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-468">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-469">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-469">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-470">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-471">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-471">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="bd7f0-472"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="bd7f0-473">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-473">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-474">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-474">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-475">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-475">Yes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-476">Oui</span><span class="sxs-lookup"><span data-stu-id="bd7f0-476">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd7f0-477">\*Non prise en charge avec les bases de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-477">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="bd7f0-478">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="bd7f0-478">Dynamic Properties</span></span>

<span data-ttu-id="bd7f0-479">Le fournisseur OLE DB pour ODBC insère plusieurs propriétés dynamiques dans la collection **Properties** des objets [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) et [Command](command-object-ado.md) non ouverts.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-479">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="bd7f0-p118">Les tableaux suivants forment un index croisé des noms ADO et OLE DB de chaque propriété dynamique. Le guide OLE DB Programmer's Reference (en anglais) référence les noms de propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés. Recherchez le nom de la propriété OLE DB dans l'Index ou consultez la rubrique « Appendix C: OLE DB Properties ».</span><span class="sxs-lookup"><span data-stu-id="bd7f0-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="bd7f0-484">Propriétés dynamiques de connexion</span><span class="sxs-lookup"><span data-stu-id="bd7f0-484">Connection Dynamic Properties</span></span>

<span data-ttu-id="bd7f0-485">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-485">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd7f0-486">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="bd7f0-486">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-487">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="bd7f0-487">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-488">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="bd7f0-488">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-489">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-489">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-490">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="bd7f0-490">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-491">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-491">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-492">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="bd7f0-492">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-493">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-493">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-494">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="bd7f0-494">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-495">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-496">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="bd7f0-496">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-497">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="bd7f0-497">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-498">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="bd7f0-498">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-499">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="bd7f0-499">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-500">Column Definition</span><span class="sxs-lookup"><span data-stu-id="bd7f0-500">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-501">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="bd7f0-501">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-502">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="bd7f0-502">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-503">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-503">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-504">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="bd7f0-504">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-505">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="bd7f0-505">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-506">Data Source</span><span class="sxs-lookup"><span data-stu-id="bd7f0-506">Data Source</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-507">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-507">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-508">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="bd7f0-508">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-509">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="bd7f0-509">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-510">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="bd7f0-510">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-511">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="bd7f0-511">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-512">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="bd7f0-512">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-513">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="bd7f0-513">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-514">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="bd7f0-514">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-515">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="bd7f0-515">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-516">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="bd7f0-516">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-517">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="bd7f0-517">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-518">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="bd7f0-518">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-519">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-519">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-520">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="bd7f0-520">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-521">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-521">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-522">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-522">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-523">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-523">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-524">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="bd7f0-524">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-525">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="bd7f0-525">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-526">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="bd7f0-526">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-527">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-527">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-528">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="bd7f0-528">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-529">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="bd7f0-529">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-530">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="bd7f0-530">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-531">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="bd7f0-531">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-532">Location</span><span class="sxs-lookup"><span data-stu-id="bd7f0-532">Location</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-533">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="bd7f0-533">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-534">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="bd7f0-534">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-535">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-535">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-536">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="bd7f0-536">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-537">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-537">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-538">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="bd7f0-538">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="bd7f0-539">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-540">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-540">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-541">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-541">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-542">Mode</span><span class="sxs-lookup"><span data-stu-id="bd7f0-542">Mode</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-543">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-543">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-544">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="bd7f0-544">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-545">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-545">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-546">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="bd7f0-546">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-547">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-547">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-548">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="bd7f0-548">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-549">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-549">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-550">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="bd7f0-550">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-551">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-551">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-552">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="bd7f0-552">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-553">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="bd7f0-553">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-554">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="bd7f0-554">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-555">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="bd7f0-555">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-556">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="bd7f0-556">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-557">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-557">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-558">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="bd7f0-558">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-559">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="bd7f0-559">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-560">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="bd7f0-560">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-561">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-561">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-562">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="bd7f0-562">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-563">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-563">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-564">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="bd7f0-564">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-565">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-565">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-566">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="bd7f0-566">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-567">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-568">Password</span><span class="sxs-lookup"><span data-stu-id="bd7f0-568">Password</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-569">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="bd7f0-569">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-570">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="bd7f0-570">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-571">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-571">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-572">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="bd7f0-572">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="bd7f0-573">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-574">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="bd7f0-574">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-575">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-575">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-576">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="bd7f0-576">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-577">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="bd7f0-577">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-578">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="bd7f0-578">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-579">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="bd7f0-579">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-580">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="bd7f0-580">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-581">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="bd7f0-581">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-582">Prompt</span><span class="sxs-lookup"><span data-stu-id="bd7f0-582">Prompt</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-583">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-583">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-584">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="bd7f0-584">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-585">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="bd7f0-585">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-586">Provider Name</span><span class="sxs-lookup"><span data-stu-id="bd7f0-586">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-587">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="bd7f0-587">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-588">Provider Version</span><span class="sxs-lookup"><span data-stu-id="bd7f0-588">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-589">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="bd7f0-589">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-590">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="bd7f0-590">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-591">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-591">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-592">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="bd7f0-592">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="bd7f0-593">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-594">Schema Term</span><span class="sxs-lookup"><span data-stu-id="bd7f0-594">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-595">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="bd7f0-595">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-596">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="bd7f0-596">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-597">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-597">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-598">SQL Support</span><span class="sxs-lookup"><span data-stu-id="bd7f0-598">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-599">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-599">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-600">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="bd7f0-600">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-601">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-601">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-602">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="bd7f0-602">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-603">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-603">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-604">Table Term</span><span class="sxs-lookup"><span data-stu-id="bd7f0-604">Table Term</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-605">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="bd7f0-605">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-606">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="bd7f0-606">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-607">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="bd7f0-607">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-608">User ID</span><span class="sxs-lookup"><span data-stu-id="bd7f0-608">User ID</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-609">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="bd7f0-609">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-610">User Name</span><span class="sxs-lookup"><span data-stu-id="bd7f0-610">User Name</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-611">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="bd7f0-611">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-612">Window Handle</span><span class="sxs-lookup"><span data-stu-id="bd7f0-612">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-613">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="bd7f0-613">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="bd7f0-614">Propriétés dynamiques du jeu d'enregitrements</span><span class="sxs-lookup"><span data-stu-id="bd7f0-614">Recordset Dynamic Properties</span></span>

<span data-ttu-id="bd7f0-615">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-615">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd7f0-616">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="bd7f0-616">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-617">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="bd7f0-617">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-618">Access Order</span><span class="sxs-lookup"><span data-stu-id="bd7f0-618">Access Order</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-619">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="bd7f0-619">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-620">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="bd7f0-620">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-621">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-622">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="bd7f0-622">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-623">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-623">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-624">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="bd7f0-624">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-625">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-625">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-626">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-626">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-627">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-627">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-628">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="bd7f0-628">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-629">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-629">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-630">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-630">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-631">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="bd7f0-631">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-632">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="bd7f0-632">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-633">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-633">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-634">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="bd7f0-634">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-635">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-635">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-636">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-636">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-637">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-637">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-638">IAccessor</span><span class="sxs-lookup"><span data-stu-id="bd7f0-638">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-639">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="bd7f0-639">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-640">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-640">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-641">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-641">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-642">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-642">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-643">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-643">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-644">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bd7f0-644">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-645">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bd7f0-645">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-646">IConvertType</span><span class="sxs-lookup"><span data-stu-id="bd7f0-646">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-647">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="bd7f0-647">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-648">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-648">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-649">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-649">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-650">IRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-650">IRowset</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-651">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-651">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-652">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bd7f0-652">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-653">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bd7f0-653">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-654">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-654">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-655">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-655">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-656">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-656">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-657">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-657">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-658">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-658">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-659">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-659">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-660">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="bd7f0-660">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-661">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-661">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-662">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-662">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-663">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bd7f0-663">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-664">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bd7f0-664">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-665">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-665">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-666">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-666">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-667">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bd7f0-667">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-668">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-668">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-669">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-669">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-670">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-670">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-671">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-671">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-672">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-672">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-673">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-673">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-674">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-674">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-675">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-675">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-676">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-676">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-677">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-677">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-678">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-678">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-679">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="bd7f0-679">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-680">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-680">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-681">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="bd7f0-681">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-682">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-682">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-683">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-683">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-684">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-684">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-685">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-685">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-686">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-686">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-687">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="bd7f0-687">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-688">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-688">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-689">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="bd7f0-689">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-690">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-690">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-691">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="bd7f0-691">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-692">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="bd7f0-692">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-693">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="bd7f0-693">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-694">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-694">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-695">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-695">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-696">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="bd7f0-696">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-697">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="bd7f0-697">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-698">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-698">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-699">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="bd7f0-699">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-700">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-700">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-701">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-701">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-702">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-702">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-703">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-703">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-704">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-704">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-705">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-705">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-706">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-706">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-707">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="bd7f0-707">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-708">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-708">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-709">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-709">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-710">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="bd7f0-710">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-711">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="bd7f0-711">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-712">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="bd7f0-712">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-713">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-713">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-714">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-714">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-715">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-715">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-716">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-716">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-717">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-717">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-718">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-718">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-719">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-719">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-720">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-720">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-721">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-721">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-722">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-723">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-723">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-724">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-724">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-725">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="bd7f0-725">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-726">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-726">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-727">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bd7f0-727">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-728">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="bd7f0-728">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-729">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-729">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-730">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-730">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-731">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-731">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-732">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-732">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-733">Updatability</span><span class="sxs-lookup"><span data-stu-id="bd7f0-733">Updatability</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-734">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-734">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-735">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bd7f0-735">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-736">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-736">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="bd7f0-737">Propriétés dynamiques de la commande</span><span class="sxs-lookup"><span data-stu-id="bd7f0-737">Command Dynamic Properties</span></span>

<span data-ttu-id="bd7f0-738">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="bd7f0-738">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd7f0-739">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="bd7f0-739">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="bd7f0-740">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="bd7f0-740">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-741">Access Order</span><span class="sxs-lookup"><span data-stu-id="bd7f0-741">Access Order</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-742">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="bd7f0-742">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-743">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="bd7f0-743">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-744">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-745">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="bd7f0-745">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-746">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-746">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-747">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="bd7f0-747">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-748">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-748">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-749">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-749">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-750">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-750">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-751">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="bd7f0-751">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-752">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-752">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-753">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-753">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-754">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="bd7f0-754">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-755">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="bd7f0-755">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-756">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-756">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-757">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="bd7f0-757">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-758">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-758">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-759">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-759">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-760">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-760">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-761">IAccessor</span><span class="sxs-lookup"><span data-stu-id="bd7f0-761">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-762">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="bd7f0-762">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-763">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-763">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-764">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-764">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-765">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-765">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-766">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-766">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-767">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bd7f0-767">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-768">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="bd7f0-768">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-769">IConvertType</span><span class="sxs-lookup"><span data-stu-id="bd7f0-769">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-770">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="bd7f0-770">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-771">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-771">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-772">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-772">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-773">IRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-773">IRowset</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-774">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="bd7f0-774">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-775">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bd7f0-775">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-776">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="bd7f0-776">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-777">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-777">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-778">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-778">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-779">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-779">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-780">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-780">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-781">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-781">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-782">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-782">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-783">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="bd7f0-783">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-784">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-784">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-785">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="bd7f0-785">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-786">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bd7f0-786">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-787">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="bd7f0-787">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-788">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-788">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-789">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="bd7f0-789">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-790">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bd7f0-790">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-791">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-791">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-792">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-792">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-793">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-793">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-794">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-794">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-795">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-795">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-796">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-796">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-797">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-797">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-798">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-798">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-799">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-799">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-800">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-800">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-801">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-801">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-802">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="bd7f0-802">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-803">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-803">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-804">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="bd7f0-804">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-805">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-805">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-806">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-806">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-807">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-807">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-808">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="bd7f0-808">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-809">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-809">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-810">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="bd7f0-810">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-811">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-811">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-812">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="bd7f0-812">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-813">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-813">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-814">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="bd7f0-814">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-815">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="bd7f0-815">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-816">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="bd7f0-816">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-817">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-817">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-818">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="bd7f0-818">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-819">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="bd7f0-819">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-820">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="bd7f0-820">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-821">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="bd7f0-821">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-822">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="bd7f0-822">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-823">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-823">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-824">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-824">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-825">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-825">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-826">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-826">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-827">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-827">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-828">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-828">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-829">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-829">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-830">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="bd7f0-830">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-831">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-831">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-832">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-832">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-833">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="bd7f0-833">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-834">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="bd7f0-834">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-835">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="bd7f0-835">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-836">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-836">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-837">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-837">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-838">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-838">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-839">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-839">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-840">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-840">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-841">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="bd7f0-841">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-842">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-842">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-843">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-843">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-844">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-844">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-845">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-846">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f0-846">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-847">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="bd7f0-847">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-848">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="bd7f0-848">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-849">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-849">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-850">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bd7f0-850">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-851">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="bd7f0-851">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-852">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="bd7f0-852">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-853">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-853">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd7f0-854">Updatability</span><span class="sxs-lookup"><span data-stu-id="bd7f0-854">Updatability</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-855">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="bd7f0-855">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd7f0-856">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="bd7f0-856">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="bd7f0-857">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="bd7f0-857">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="bd7f0-858">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd7f0-858">See also</span></span>

<span data-ttu-id="bd7f0-859">Pour plus d’informations concernant l’implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour ODBC, consultez le [Guide du programmeur OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) ou visitez le [Centre de développement de plateforme de données](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span><span class="sxs-lookup"><span data-stu-id="bd7f0-859">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

