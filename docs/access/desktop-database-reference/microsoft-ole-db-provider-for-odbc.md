---
title: Fournisseur Microsoft OLE DB pour ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288910"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="848c4-102">Fournisseur Microsoft OLE DB pour ODBC</span><span class="sxs-lookup"><span data-stu-id="848c4-102">Microsoft OLE DB Provider for ODBC</span></span>

<span data-ttu-id="848c4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="848c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="848c4-p101">Pour un programmeur ADO ou RDS, l'idéal serait que chaque source de données expose une interface OLE DB pour qu'ADO puisse effectuer les appels directement dans la source de données. Même si les fournisseurs de bases de données sont de plus en plus nombreux à implémenter les interfaces OLE DB, certaines sources de données ne sont pas encore exposées de cette façon. Toutefois, tous les systèmes SGBD utilisés aujourd'hui sont en principe accessibles via ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-p101">To an ADO or RDS programmer, an ideal world would be one in which every data source exposes an OLE DB interface, so that ADO could call directly into the data source. Although increasingly more database vendors are implementing OLE DB interfaces, some data sources are not yet exposed this way. However, virtually all DBMS systems in use today can be accessed through ODBC.</span></span>

<span data-ttu-id="848c4-107">Il existe des pilotes ODBC pour les principaux SGBD utilisés aujourd'hui, dont Microsoft SQL Server, Microsoft Access (moteur de base de données Microsoft Jet) et Microsoft FoxPro, sans oublier les produits de base de données non-Microsoft comme Oracle.</span><span class="sxs-lookup"><span data-stu-id="848c4-107">ODBC drivers are available for every major DBMS in use today, including Microsoft SQL Server, Microsoft Access (Microsoft Jet database engine), and Microsoft FoxPro, in addition to non-Microsoft database products such as Oracle.</span></span>

<span data-ttu-id="848c4-p102">Le fournisseur Microsoft ODBC permet à ADO de se connecter à n'importe quelle source de données ODBC. Ce fournisseur est libre de thread et utilise Unicode.</span><span class="sxs-lookup"><span data-stu-id="848c4-p102">The Microsoft ODBC Provider, however, allows ADO to connect to any ODBC data source. The provider is free-threaded and Unicode enabled.</span></span>

<span data-ttu-id="848c4-p103">Le fournisseur prend en charge les transactions bien que les différents moteurs SGBD offrent différents types de prise en charge de ces transactions. Microsoft Access prend par exemple en charge jusqu'à cinq niveaux de transactions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="848c4-p103">The provider supports transactions, although different DBMS engines offer different types of transaction support. For example, Microsoft Access supports nested transactions up to five levels deep.</span></span>

<span data-ttu-id="848c4-112">Il s'agit du fournisseur par défaut pour ADO et toutes les propriétés et méthodes ADO spécifiques au fournisseur sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="848c4-112">This is the default provider for ADO, and all provider-dependent ADO properties and methods are supported.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="848c4-113">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="848c4-113">Connection String Parameters</span></span>

<span data-ttu-id="848c4-114">Pour vous connecter à ce fournisseur, définissez l’argument **Provider** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="848c4-114">To connect to this provider, set the **Provider=** argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```sql 
 
MSDASQL 
```

<span data-ttu-id="848c4-115">La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="848c4-115">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="848c4-116">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="848c4-116">Typical Connection String</span></span>

<span data-ttu-id="848c4-117">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="848c4-117">A typical connection string for this provider is:</span></span>

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

<span data-ttu-id="848c4-118">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="848c4-118">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="848c4-119">Mot clé</span><span class="sxs-lookup"><span data-stu-id="848c4-119">Keyword</span></span></p></th>
<th><p><span data-ttu-id="848c4-120">Description</span><span class="sxs-lookup"><span data-stu-id="848c4-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-121"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="848c4-121"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="848c4-122">Spécifie le fournisseur OLE DB pour ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-122">Specifies the OLE DB Provider for ODBC.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-123"><strong>DSN</strong></span><span class="sxs-lookup"><span data-stu-id="848c4-123"><strong>DSN</strong></span></span></p></td>
<td><p><span data-ttu-id="848c4-124">Spécifie le nom de la source de données.</span><span class="sxs-lookup"><span data-stu-id="848c4-124">Specifies the data source name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-125"><strong>UID</strong></span><span class="sxs-lookup"><span data-stu-id="848c4-125"><strong>UID</strong></span></span></p></td>
<td><p><span data-ttu-id="848c4-126">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="848c4-126">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-127"><strong>PWD</strong></span><span class="sxs-lookup"><span data-stu-id="848c4-127"><strong>PWD</strong></span></span></p></td>
<td><p><span data-ttu-id="848c4-128">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="848c4-128">Specifies the user password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-129"><strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="848c4-129"><strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="848c4-130">Spécifie l’URL d’un fichier ou d’un répertoire publié dans un dossier web.</span><span class="sxs-lookup"><span data-stu-id="848c4-130">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="848c4-131">Comme il s'agit du fournisseur par défaut pour ADO, si vous omettez de spécifier le paramètre **Provider=** dans la chaîne de connexion, ADO tentera d'établir une connexion vers ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="848c4-131">Because this is the default provider for ADO, if you omit the **Provider=** parameter from the connection string, ADO will attempt to establish a connection to this provider.</span></span>

<span data-ttu-id="848c4-p104">Ce fournisseur ne prend pas en charge de paramètre de connexion spécifique en plus des paramètres définis par ADO. Il transmettra toutefois tous les paramètres de connexion non-ADO au gestionnaire de pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-p104">The provider does not support any specific connection parameters in addition to those defined by ADO. However, the provider will pass any non-ADO connection parameters to the ODBC driver manager.</span></span>

<span data-ttu-id="848c4-p105">Comme vous n'êtes pas obligé de spécifier le paramètre **Provider**, vous pouvez composer une chaîne de connexion ADO identique à la chaîne de connexion ODBC pour la même source de données. Utilisez les mêmes noms de paramètre (**DRIVER=**, **DATABASE=**, **DSN=**, etc.), les mêmes valeurs et la même syntaxe que pour composer une chaîne ODBC. Vous pouvez vous connecter avec ou sans nom de source de données (DSN) ou DSN de fichier (FileDSN).</span><span class="sxs-lookup"><span data-stu-id="848c4-p105">Because you can omit the **Provider** parameter, you can therefore compose an ADO connection string that is identical to an ODBC connection string for the same data source. Use the same parameter names (**DRIVER=**, **DATABASE=**, **DSN=**, and so on), values, and syntax as you would when composing an ODBC connection string. You can connect with or without a predefined data source name (DSN) or FileDSN.</span></span>

<span data-ttu-id="848c4-137">**Syntaxe avec un DSN ou un FileDSN :**</span><span class="sxs-lookup"><span data-stu-id="848c4-137">**Syntax with a DSN or FileDSN:**</span></span>

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

<span data-ttu-id="848c4-138">**Syntaxe sans DSN (connexion sans DSN) :**</span><span class="sxs-lookup"><span data-stu-id="848c4-138">**Syntax without a DSN (DSN-less connection):**</span></span>

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

<span data-ttu-id="848c4-p106">Si vous utilisez un **DSN** ou un **FileDSN**, il doit être défini à travers l'administrateur de source de données ODBC dans le Panneau de configuration de Windows. Dans Microsoft Windows 2000, l'administrateur ODBC se trouve sous Outils d'administration. Dans les versions précédentes de Windows, l'icône de l'administrateur ODBC est appelée **ODBC 32 bits** ou simplement **ODBC**.</span><span class="sxs-lookup"><span data-stu-id="848c4-p106">If you use a **DSN** or **FileDSN**, it must be defined through the ODBC Data Source Administrator in the Windows Control Panel. In Microsoft Windows 2000, the ODBC Administrator is located under Administrative Tools. In previous versions of Windows, the ODBC Administrator icon is named **32-bit ODBC** or simply **ODBC**.</span></span>

<span data-ttu-id="848c4-142">Plutôt que de définir un **DSN**, vous pouvez choisir de spécifier le pilote ODBC (**DRIVER=**), SQL Server par exemple, le nom du serveur (**SERVER=**) et le nom de la base de données (**DATABASE=**).</span><span class="sxs-lookup"><span data-stu-id="848c4-142">As an alternative to setting a **DSN**, you can specify the ODBC driver (**DRIVER=**), such as "SQL Server;" the server name (**SERVER=**); and the database name (**DATABASE=**).</span></span>

<span data-ttu-id="848c4-143">Vous pouvez aussi spécifier un nom de compte utilisateur (**UID=**) et le mot de passe de ce compte (**PWD=**) dans les paramètres spécifiques à ODBC ou dans les paramètres ADO standard *utilisateur* et *mot de passe*.</span><span class="sxs-lookup"><span data-stu-id="848c4-143">You can also specify a user account name (**UID=**), and the password for the user account (**PWD=**) in the ODBC-specific parameters or in the standard ADO-defined *user* and *password* parameters.</span></span>

<span data-ttu-id="848c4-144">Bien **qu’une définition de DSN** spécifie   déjà une base de données, vous pouvez spécifier un paramètre de base de données en plus d’un **DSN** pour se connecter à une autre base de données.</span><span class="sxs-lookup"><span data-stu-id="848c4-144">Although a **DSN** definition already specifies a database, you can specify *a* *database* parameter in addition to a **DSN** to connect to a different database.</span></span> <span data-ttu-id="848c4-145">Il est bon de toujours inclure le *paramètre* de base *de* données lorsque vous utilisez un **DSN**.</span><span class="sxs-lookup"><span data-stu-id="848c4-145">It is a good idea to always include *the* *database* parameter when you use a **DSN**.</span></span> <span data-ttu-id="848c4-146">Vous serez ainsi certain de vous connecter à la bonne base de données même si un autre utilisateur a modifié le paramètre de base de données par défaut depuis votre dernière vérification de la définition du **DSN**.</span><span class="sxs-lookup"><span data-stu-id="848c4-146">This will ensure that you connect to the proper database in the event that another user changed the default database parameter since you last checked the **DSN** definition.</span></span>

## <a name="provider-specific-connection-properties"></a><span data-ttu-id="848c4-147">Propriétés de connexion spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="848c4-147">Provider-Specific Connection Properties</span></span>

<span data-ttu-id="848c4-p108">Le fournisseur OLE DB pour ODBC ajoute plusieurs propriétés à la collection [Properties](properties-collection-ado.md) de l’objet **Connection**. Le tableau suivant répertorie chaque propriété en indiquant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="848c4-p108">The OLE DB provider for ODBC adds several properties to the [Properties](properties-collection-ado.md) collection of the **Connection** object. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="848c4-150">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="848c4-150">Property Name</span></span></p></th>
<th><p><span data-ttu-id="848c4-151">Description</span><span class="sxs-lookup"><span data-stu-id="848c4-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-152">Procédures accessibles</span><span class="sxs-lookup"><span data-stu-id="848c4-152">Accessible Procedures</span></span><br />
<span data-ttu-id="848c4-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="848c4-153">(KAGPROP_ACCESSIBLEPROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="848c4-154">Indique si l'utilisateur a accès aux procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="848c4-154">Indicates whether the user has access to stored procedures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-155">Tables accessibles</span><span class="sxs-lookup"><span data-stu-id="848c4-155">Accessible Tables</span></span><br />
<span data-ttu-id="848c4-156">(KAGPROP_ACCESSIBLETABLES)</span><span class="sxs-lookup"><span data-stu-id="848c4-156">(KAGPROP_ACCESSIBLETABLES)</span></span></p></td>
<td><p><span data-ttu-id="848c4-157">Indique si l'utilisateur a l'autorisation d'exécuter les instructions SELECT sur les tables de base de données.</span><span class="sxs-lookup"><span data-stu-id="848c4-157">Indicates whether the user has permission to execute SELECT statements against the database tables.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-158">Instructions actives</span><span class="sxs-lookup"><span data-stu-id="848c4-158">Active Statements</span></span><br />
<span data-ttu-id="848c4-159">(KAGPROP_ACTIVESTATEMENTS)</span><span class="sxs-lookup"><span data-stu-id="848c4-159">(KAGPROP_ACTIVESTATEMENTS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-160">Indique le nombre de descripteurs qu'un pilote ODBC peut prendre en charge dans une connexion.</span><span class="sxs-lookup"><span data-stu-id="848c4-160">Indicates the number of handles an ODBC driver can support on a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-161">Nom du pilote</span><span class="sxs-lookup"><span data-stu-id="848c4-161">Driver Name</span></span><br />
<span data-ttu-id="848c4-162">(KAGPROP_DRIVERNAME)</span><span class="sxs-lookup"><span data-stu-id="848c4-162">(KAGPROP_DRIVERNAME)</span></span></p></td>
<td><p><span data-ttu-id="848c4-163">Indique le nom de fichier du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-163">Indicates the file name of the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-164">Version ODBC du pilote</span><span class="sxs-lookup"><span data-stu-id="848c4-164">Driver ODBC Version</span></span><br />
<span data-ttu-id="848c4-165">(KAGPROP_DRIVERODBCVER)</span><span class="sxs-lookup"><span data-stu-id="848c4-165">(KAGPROP_DRIVERODBCVER)</span></span></p></td>
<td><p><span data-ttu-id="848c4-166">Indique la version d'ODBC prise en charge par ce pilote.</span><span class="sxs-lookup"><span data-stu-id="848c4-166">Indicates the version of ODBC that this driver supports.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-167">Utilisation des fichiers</span><span class="sxs-lookup"><span data-stu-id="848c4-167">File Usage</span></span><br />
<span data-ttu-id="848c4-168">(KAGPROP_FILEUSAGE)</span><span class="sxs-lookup"><span data-stu-id="848c4-168">(KAGPROP_FILEUSAGE)</span></span></p></td>
<td><p><span data-ttu-id="848c4-169">Indique le mode utilisé par le pilote pour traiter un fichier dans une source de données : table ou catalogue.</span><span class="sxs-lookup"><span data-stu-id="848c4-169">Indicates how the driver treats a file in a data source; as a table or as a catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-170">Like Escape, clause</span><span class="sxs-lookup"><span data-stu-id="848c4-170">Like Escape Clause</span></span><br />
<span data-ttu-id="848c4-171">(KAGPROP_LIKEESCAPECLAUSE)</span><span class="sxs-lookup"><span data-stu-id="848c4-171">(KAGPROP_LIKEESCAPECLAUSE)</span></span></p></td>
<td><p><span data-ttu-id="848c4-172">Indique si le pilote prend en charge la définition et l'utilisation du caractère d'échappement pour le caractère de pourcentage (%) et le caractère de soulignement (_) dans le prédicat LIKE d'une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="848c4-172">Indicates whether the driver supports the definition and use of an escape character for the percent character (%) and underline character (_) in the LIKE predicate of a WHERE clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-173">Colonnes max dans Group By</span><span class="sxs-lookup"><span data-stu-id="848c4-173">Max Columns in Group By</span></span><br />
<span data-ttu-id="848c4-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span><span class="sxs-lookup"><span data-stu-id="848c4-174">(KAGPROP_MAXCOLUMNSINGROUPBY)</span></span></p></td>
<td><p><span data-ttu-id="848c4-175">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la clause GROUP BY d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="848c4-175">Indicates the maximum number of columns that can be listed in the GROUP BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-176">Nombre maximum de colonnes dans l’index</span><span class="sxs-lookup"><span data-stu-id="848c4-176">Max Columns in Index</span></span><br />
<span data-ttu-id="848c4-177">(KAGPROP_MAXCOLUMNSININDEX)</span><span class="sxs-lookup"><span data-stu-id="848c4-177">(KAGPROP_MAXCOLUMNSININDEX)</span></span></p></td>
<td><p><span data-ttu-id="848c4-178">Indique le nombre maximal de colonnes qui peuvent être incluses dans un index.</span><span class="sxs-lookup"><span data-stu-id="848c4-178">Indicates the maximum number of columns that can be included in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-179">Colonnes max dans l’ordre par</span><span class="sxs-lookup"><span data-stu-id="848c4-179">Max Columns in Order By</span></span><br />
<span data-ttu-id="848c4-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span><span class="sxs-lookup"><span data-stu-id="848c4-180">(KAGPROP_MAXCOLUMNSINORDERBY)</span></span></p></td>
<td><p><span data-ttu-id="848c4-181">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la clause ORDER BY d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="848c4-181">Indicates the maximum number of columns that can be listed in the ORDER BY clause of a SELECT statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-182">Nombre de colonnes max dans Select</span><span class="sxs-lookup"><span data-stu-id="848c4-182">Max Columns in Select</span></span><br />
<span data-ttu-id="848c4-183">(KAGPROP_MAXCOLUMNSINSELECT)</span><span class="sxs-lookup"><span data-stu-id="848c4-183">(KAGPROP_MAXCOLUMNSINSELECT)</span></span></p></td>
<td><p><span data-ttu-id="848c4-184">Indique le nombre maximal de colonnes qui peuvent être répertoriées dans la partie SELECT d'une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="848c4-184">Indicates the maximum number of columns that can be listed in the SELECT portion of a SELECT statement.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-185">Nombre de colonnes max dans le tableau</span><span class="sxs-lookup"><span data-stu-id="848c4-185">Max Columns in Table</span></span><br />
<span data-ttu-id="848c4-186">(KAGPROP_MAXCOLUMNSINTABLE)</span><span class="sxs-lookup"><span data-stu-id="848c4-186">(KAGPROP_MAXCOLUMNSINTABLE)</span></span></p></td>
<td><p><span data-ttu-id="848c4-187">Indique le nombre maximal de colonnes autorisé dans une table.</span><span class="sxs-lookup"><span data-stu-id="848c4-187">Indicates the maximum number of columns allowed in a table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-188">Fonctions numériques</span><span class="sxs-lookup"><span data-stu-id="848c4-188">Numeric Functions</span></span><br />
<span data-ttu-id="848c4-189">(KAGPROP_NUMERICFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="848c4-189">(KAGPROP_NUMERICFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-p109">Indique les fonctions numériques prises en charge par le pilote ODBC.

Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-p109">Indicates which numeric functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-192">Fonctionnalités de joints externes</span><span class="sxs-lookup"><span data-stu-id="848c4-192">Outer Join Capabilities</span></span><br />
<span data-ttu-id="848c4-193">(KAGPROP_OJCAPABILITY)</span><span class="sxs-lookup"><span data-stu-id="848c4-193">(KAGPROP_OJCAPABILITY)</span></span></p></td>
<td><p><span data-ttu-id="848c4-194">Indique les types de jointures externes (OUTER JOIN) prises en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="848c4-194">Indicates the types of OUTER JOINs supported by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-195">Jointeurs externes</span><span class="sxs-lookup"><span data-stu-id="848c4-195">Outer Joins</span></span><br />
<span data-ttu-id="848c4-196">(KAGPROP_OUTERJOINS)</span><span class="sxs-lookup"><span data-stu-id="848c4-196">(KAGPROP_OUTERJOINS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-197">Indique si le fournisseur prend en charge les jointures externes (OUTER JOIN).</span><span class="sxs-lookup"><span data-stu-id="848c4-197">Indicates whether the provider supports OUTER JOINs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-198">Caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="848c4-198">Special Characters</span></span><br />
<span data-ttu-id="848c4-199">(KAGPROP_SPECIALCHARACTERS)</span><span class="sxs-lookup"><span data-stu-id="848c4-199">(KAGPROP_SPECIALCHARACTERS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-200">Indique les caractères ayant une signification spéciale pour le pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-200">Indicates which characters have special meaning for the ODBC driver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-201">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="848c4-201">Stored Procedures</span></span><br />
<span data-ttu-id="848c4-202">(KAGPROP_PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="848c4-202">(KAGPROP_PROCEDURES)</span></span></p></td>
<td><p><span data-ttu-id="848c4-203">Indique si les procédures stockées peuvent être utilisées avec ce pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-203">Indicates whether stored procedures are available for use with this ODBC driver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-204">Fonctions de chaîne</span><span class="sxs-lookup"><span data-stu-id="848c4-204">String Functions</span></span><br />
<span data-ttu-id="848c4-205">(KAGPROP_STRINGFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="848c4-205">(KAGPROP_STRINGFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-p110">Indique les fonctions de chaîne prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-p110">Indicates which string functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-208">Fonctions système</span><span class="sxs-lookup"><span data-stu-id="848c4-208">System Functions</span></span><br />
<span data-ttu-id="848c4-209">(KAGPROP_SYSTEMFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="848c4-209">(KAGPROP_SYSTEMFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-p111">Indique les fonctions système prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-p111">Indicates which system functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-212">Fonctions Heure/Date</span><span class="sxs-lookup"><span data-stu-id="848c4-212">Time/Date Functions</span></span><br />
<span data-ttu-id="848c4-213">(KAGPROP_TIMEDATEFUNCTIONS)</span><span class="sxs-lookup"><span data-stu-id="848c4-213">(KAGPROP_TIMEDATEFUNCTIONS)</span></span></p></td>
<td><p><span data-ttu-id="848c4-p112">Indique les fonctions de date et heure prises en charge par le pilote ODBC. Pour obtenir le listing des noms de fonctions et des valeurs associées utilisés dans ce masque de bits, consultez la rubrique sur les fonctions scalaires dans l'Annexe E de la documentation ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-p112">Indicates which time and date functions are supported by the ODBC driver. For a listing of function names and the associated values used in this bitmask, see Appendix E: Scalar Functions in the ODBC documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-216">SQL Prise en charge de la grammaire</span><span class="sxs-lookup"><span data-stu-id="848c4-216">SQL Grammar Support</span></span><br />
<span data-ttu-id="848c4-217">(KAGPROP_ODBCSQLCONFORMANCE)</span><span class="sxs-lookup"><span data-stu-id="848c4-217">(KAGPROP_ODBCSQLCONFORMANCE)</span></span></p></td>
<td><p><span data-ttu-id="848c4-218">Indique la grammaire SQL prise en charge par le pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-218">Indicates the SQL grammar that the ODBC driver supports.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a><span data-ttu-id="848c4-219">Propriétés spécifiques au fournisseur pour le jeu d'enregistrement et la commande</span><span class="sxs-lookup"><span data-stu-id="848c4-219">Provider-Specific Recordset and Command Properties</span></span>

<span data-ttu-id="848c4-p113">Le fournisseur OLE DB pour ODBC ajoute plusieurs propriétés à la collection **Properties** des objets **Recordset** et **Command**. Le tableau suivant répertorie chaque propriété en indiquant entre parenthèses le nom de propriété OLE DB correspondant.</span><span class="sxs-lookup"><span data-stu-id="848c4-p113">The OLE DB provider for ODBC adds several properties to the **Properties** collection of the **Recordset** and **Command** objects. The following table lists these properties with the corresponding OLE DB property name in parentheses.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="848c4-222">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="848c4-222">Property Name</span></span></p></th>
<th><p><span data-ttu-id="848c4-223">Description</span><span class="sxs-lookup"><span data-stu-id="848c4-223">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-224">Mises à jour/suppressions/insertions basées sur des requêtes</span><span class="sxs-lookup"><span data-stu-id="848c4-224">Query Based Updates/Deletes/Inserts</span></span><br />
<span data-ttu-id="848c4-225">(KAGPROP_QUERYBASEDUPDATES)</span><span class="sxs-lookup"><span data-stu-id="848c4-225">(KAGPROP_QUERYBASEDUPDATES)</span></span></p></td>
<td><p><span data-ttu-id="848c4-226">Indique s'il est possible d'utiliser des requêtes SQL pour effectuer des mises à jour, des suppressions ou des insertions.</span><span class="sxs-lookup"><span data-stu-id="848c4-226">Indicates whether updates, deletions, and insertions can be performed using SQL queries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-227">Type de récurrence ODBC</span><span class="sxs-lookup"><span data-stu-id="848c4-227">ODBC Concurrency Type</span></span><br />
<span data-ttu-id="848c4-228">(KAGPROP_CONCURRENCY)</span><span class="sxs-lookup"><span data-stu-id="848c4-228">(KAGPROP_CONCURRENCY)</span></span></p></td>
<td><p><span data-ttu-id="848c4-229">Indique la méthode utilisée pour réduire les problèmes susceptibles de se produire si deux utilisateurs tentent d'accéder simultanément aux mêmes données de la source de données.</span><span class="sxs-lookup"><span data-stu-id="848c4-229">Indicates the method used to reduce potential problems caused by two users attempting to access the same data from the data source simultaneously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-230">Accessibilité BLOB sur Forward-Only curseur</span><span class="sxs-lookup"><span data-stu-id="848c4-230">BLOB accessibility on Forward-Only cursor</span></span><br />
<span data-ttu-id="848c4-231">(KAGPROP_BLOBSONFOCURSOR)</span><span class="sxs-lookup"><span data-stu-id="848c4-231">(KAGPROP_BLOBSONFOCURSOR)</span></span></p></td>
<td><p><span data-ttu-id="848c4-232">Indique si les <strong>champs</strong> BLOB sont accessibles avec un curseur de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="848c4-232">Indicates whether BLOB <strong>Fields</strong> can be accessed when using a forward-only cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-233">Inclure SQL_FLOAT, SQL_DOUBLE et SQL_REAL dans les clauses WHERE QBU</span><span class="sxs-lookup"><span data-stu-id="848c4-233">Include SQL_FLOAT, SQL_DOUBLE, and SQL_REAL in QBU WHERE clauses</span></span><br />
<span data-ttu-id="848c4-234">(KAGPROP_INCLUDENONEXACT)</span><span class="sxs-lookup"><span data-stu-id="848c4-234">(KAGPROP_INCLUDENONEXACT)</span></span></p></td>
<td><p><span data-ttu-id="848c4-235">Indique si les valeurs SQL_FLOAT, SQL_DOUBLE et SQL_REAL peuvent être incluses dans une clause QBU WHERE.</span><span class="sxs-lookup"><span data-stu-id="848c4-235">Indicates whether SQL_FLOAT, SQL_DOUBLE, and SQL_REAL values can be included in a QBU WHERE clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-236">Position sur la dernière ligne après insertion</span><span class="sxs-lookup"><span data-stu-id="848c4-236">Position on the last row after insert</span></span><br />
<span data-ttu-id="848c4-237">(KAGPROP_POSITIONONNEWROW)</span><span class="sxs-lookup"><span data-stu-id="848c4-237">(KAGPROP_POSITIONONNEWROW)</span></span></p></td>
<td><p><span data-ttu-id="848c4-238">Indique qu'après insertion d'un nouvel enregistrement dans une table, la dernière ligne de la table est activée.</span><span class="sxs-lookup"><span data-stu-id="848c4-238">Indicates that after a new record has been inserted in a table, the last row in the table will be come the current row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-239">IRowsetChangeExtInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-239">IRowsetChangeExtInfo</span></span><br />
<span data-ttu-id="848c4-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span><span class="sxs-lookup"><span data-stu-id="848c4-240">(KAGPROP_IROWSETCHANGEEXTINFO)</span></span></p></td>
<td><p><span data-ttu-id="848c4-241">Indique si l'interface <strong>IRowsetChange</strong> fournit la prise en charge des informations étendues.</span><span class="sxs-lookup"><span data-stu-id="848c4-241">Indicates whether the <strong>IRowsetChange</strong> interface provides extended information support.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-242">Type de curseur ODBC</span><span class="sxs-lookup"><span data-stu-id="848c4-242">ODBC Cursor Type</span></span><br />
<span data-ttu-id="848c4-243">(KAGPROP_CURSOR)</span><span class="sxs-lookup"><span data-stu-id="848c4-243">(KAGPROP_CURSOR)</span></span></p></td>
<td><p><span data-ttu-id="848c4-244">Indique le type de curseur utilisé par le <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="848c4-244">Indicates the type of cursor used by the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-245">Générer un rowset qui peut être marshalé</span><span class="sxs-lookup"><span data-stu-id="848c4-245">Generate a Rowset that can be marshaled</span></span><br />
<span data-ttu-id="848c4-246">(KAGPROP_MARSHALLABLE)</span><span class="sxs-lookup"><span data-stu-id="848c4-246">(KAGPROP_MARSHALLABLE)</span></span></p></td>
<td><p><span data-ttu-id="848c4-247">Indique que le pilote ODBC génère un jeu d'enregistrements qui peut être marshalé.</span><span class="sxs-lookup"><span data-stu-id="848c4-247">Indicates that the ODBC driver generates a recordset that can be marshaled</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a><span data-ttu-id="848c4-248">Texte de la commande</span><span class="sxs-lookup"><span data-stu-id="848c4-248">Command Text</span></span>

<span data-ttu-id="848c4-249">La façon dont vous utilisez l’objet [Command](command-object-ado.md) dépend en grande partie de la source de données et du type de requête ou de commande qu’elle accepte.</span><span class="sxs-lookup"><span data-stu-id="848c4-249">How you use the [Command](command-object-ado.md) object largely depends on the data source, and what type of query or command statement it will accept.</span></span>

<span data-ttu-id="848c4-p114">ODBC fournit une syntaxe spécifique pour appeler les procédures stockées. Pour la propriété [CommandText](commandtext-property-ado.md) d’un objet **Command**, l’argument *CommandText* de la méthode **Execute** sur un objet [Connection](connection-object-ado.md) ou l’argument *Source* de la méthode **Open** sur un objet [Recordset](recordset-object-ado.md) transmet une chaîne présentant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="848c4-p114">ODBC provides a specific syntax for calling stored procedures. For the [CommandText](commandtext-property-ado.md) property of a **Command** object, the *CommandText* argument to the **Execute** method on a [Connection](connection-object-ado.md) object, or the *Source* argument to the **Open** method on a [Recordset](recordset-object-ado.md) object, passes in a string with this syntax:</span></span>

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

<span data-ttu-id="848c4-p115">Chaque **?** fait référence à un objet de la collection [Parameters](parameters-collection-ado.md). Le premier **?** fait référence à l’objet **Parameters** (0), le **?** suivant fait référence à l’objet **Parameters** (1) et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="848c4-p115">Each **?** references an object in the [Parameters](parameters-collection-ado.md) collection. The first **?** references **Parameters**(0), the next **?** references **Parameters**(1), and so on.</span></span>

<span data-ttu-id="848c4-p116">Les références aux paramètres sont facultatives et dépendent de la structure de la procédure stockée. Si vous voulez appeler une procédure stockée qui ne définisse aucun paramètre, votre chaîne doit présenter la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="848c4-p116">The parameter references are optional and depend on the structure of the stored procedure. If you want to call a stored procedure that defines no parameters, your string would look like this:</span></span>

`"{ call procedure }"`

<span data-ttu-id="848c4-259">Si vous avez deux paramètres de requête, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="848c4-259">If you have two query parameters, your string would look like this:</span></span>

`"{ call procedure ( ?, ? ) }"`

<span data-ttu-id="848c4-p117">Si la procédure stockée renvoie une valeur, cette valeur sera traitée comme un paramètre supplémentaire. Si vous n'avez pas de paramètre de requête mais que vous avez une valeur de renvoi, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="848c4-p117">If the stored procedure will return a value, the return value is treated as another parameter. If you have no query parameters but you do have a return value, your string would look like this:</span></span>

`"{ ? = call procedure }"`

<span data-ttu-id="848c4-262">Enfin, si vous avez une valeur de renvoi et deux paramètres de requête, votre chaîne aura la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="848c4-262">Finally, if you have a return value and two query parameters, your string would look like this:</span></span>

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a><span data-ttu-id="848c4-263">Comportement des jeux d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="848c4-263">Recordset Behavior</span></span>

<span data-ttu-id="848c4-264">Les tableaux suivants répertorient les méthodes et propriétés ADO standard disponibles pour un objet **Recordset** ouvert avec ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="848c4-264">The following tables list the standard ADO methods and properties available on a **Recordset** object opened with this provider.</span></span>

<span data-ttu-id="848c4-265">Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection **Properties** du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="848c4-265">For more detailed information about **Recordset** behavior for your provider configuration, run the [Supports](supports-method-ado.md) method and enumerate the **Properties** collection of the **Recordset** to determine whether provider-specific dynamic properties are present.</span></span>

<span data-ttu-id="848c4-266">Disponibilité des propriétés ADO standard d'un **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="848c4-266">Availability of standard ADO **Recordset** properties:</span></span>

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
<th><p><span data-ttu-id="848c4-267">Propriété</span><span class="sxs-lookup"><span data-stu-id="848c4-267">Property</span></span></p></th>
<th><p><span data-ttu-id="848c4-268">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="848c4-268">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="848c4-269">Dynamique</span><span class="sxs-lookup"><span data-stu-id="848c4-269">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="848c4-270">Keyset</span><span class="sxs-lookup"><span data-stu-id="848c4-270">Keyset</span></span></p></th>
<th><p><span data-ttu-id="848c4-271">Statique</span><span class="sxs-lookup"><span data-stu-id="848c4-271">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="848c4-272"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-273">non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-273">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-274">non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-274">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-275">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-275">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-276">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-276">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="848c4-277"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-278">non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-278">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-279">non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-279">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-280">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-280">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-281">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-281">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="848c4-282"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-283">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-283">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-284">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-284">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-285">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-285">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-286">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-286">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-287"><a href="bof-eof-properties-ado.md">BOF</a></span><span class="sxs-lookup"><span data-stu-id="848c4-287"><a href="bof-eof-properties-ado.md">BOF</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-288">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-288">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-289">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-289">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-290">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-290">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-291">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-291">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-292"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="848c4-292"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-293">non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-293">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-294">non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-294">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-295">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-295">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-296">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-296">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-297"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="848c4-297"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-298">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-298">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-299">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-299">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-300">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-300">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-301">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-301">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="848c4-302"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-303">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-303">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-304">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-304">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-305">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-305">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-306">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-306">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-307"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="848c4-307"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-308">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-308">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-309">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-309">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-310">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-310">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-311">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-311">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-312"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="848c4-312"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-313">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-313">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-314">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-314">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-315">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-315">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-316">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-316">read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-317"><a href="filter-property-ado.md">Filtre</a></span><span class="sxs-lookup"><span data-stu-id="848c4-317"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-318">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-318">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-319">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-319">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-320">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-320">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-321">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-321">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-322"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="848c4-322"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-323">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-323">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-324">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-324">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-325">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-325">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-326">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-326">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span><span class="sxs-lookup"><span data-stu-id="848c4-327"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-328">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-328">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-329">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-329">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-330">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-330">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-331">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-331">read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="848c4-332"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-333">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-333">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-334">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-334">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-335">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-335">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-336">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-336">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-337"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="848c4-337"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-338">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-338">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-339">Non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-339">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-340">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-340">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-341">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-341">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-342"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="848c4-342"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-343">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-343">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-344">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-344">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-345">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-345">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-346">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-346">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-347"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="848c4-347"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-348">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-348">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-349">Non disponible</span><span class="sxs-lookup"><span data-stu-id="848c4-349">not available</span></span></p></td>
<td><p><span data-ttu-id="848c4-350">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-350">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-351">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-351">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-352"><a href="source-property-ado-recordset.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="848c4-352"><a href="source-property-ado-recordset.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-353">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-353">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-354">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-354">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-355">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-355">read/write</span></span></p></td>
<td><p><span data-ttu-id="848c4-356">lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="848c4-356">read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-357"><a href="state-property-ado.md">État</a></span><span class="sxs-lookup"><span data-stu-id="848c4-357"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-358">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-358">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-359">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-359">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-360">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-360">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-361">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-361">read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-362"><a href="status-property-ado-recordset.md">État</a></span><span class="sxs-lookup"><span data-stu-id="848c4-362"><a href="status-property-ado-recordset.md">Status</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-363">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-363">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-364">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-364">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-365">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-365">read-only</span></span></p></td>
<td><p><span data-ttu-id="848c4-366">lecture seule</span><span class="sxs-lookup"><span data-stu-id="848c4-366">read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="848c4-367">Les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [AbsolutePage](absolutepage-property-ado.md) sont en écriture seule lorsqu’ADO est utilisé avec la version 1.0 du fournisseur Microsoft OLE DB pour ODBC.</span><span class="sxs-lookup"><span data-stu-id="848c4-367">The [AbsolutePosition](absoluteposition-property-ado.md) and [AbsolutePage](absolutepage-property-ado.md) properties are write-only when ADO is used with version 1.0 of the Microsoft OLE DB Provider for ODBC.</span></span>

<span data-ttu-id="848c4-368">Disponibilité des méthodes ADO standard d'un **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="848c4-368">Availability of standard ADO **Recordset** methods:</span></span>

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
<th><p><span data-ttu-id="848c4-369">Méthode</span><span class="sxs-lookup"><span data-stu-id="848c4-369">Method</span></span></p></th>
<th><p><span data-ttu-id="848c4-370">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="848c4-370">ForwardOnly</span></span></p></th>
<th><p><span data-ttu-id="848c4-371">Dynamique</span><span class="sxs-lookup"><span data-stu-id="848c4-371">Dynamic</span></span></p></th>
<th><p><span data-ttu-id="848c4-372">Keyset</span><span class="sxs-lookup"><span data-stu-id="848c4-372">Keyset</span></span></p></th>
<th><p><span data-ttu-id="848c4-373">Statique</span><span class="sxs-lookup"><span data-stu-id="848c4-373">Static</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-374"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="848c4-374"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-375">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-375">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-376">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-376">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-377">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-377">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-378">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-378">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-379"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="848c4-379"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-380">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-380">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-381">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-381">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-382">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-382">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-383">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="848c4-384"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-385">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-385">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-386">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-386">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-387">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-387">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-388">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-388">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="848c4-389"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-390">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-390">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-391">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-391">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-392">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-392">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-393">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-393">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-394"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="848c4-394"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-395">Non</span><span class="sxs-lookup"><span data-stu-id="848c4-395">No</span></span></p></td>
<td><p><span data-ttu-id="848c4-396">Non</span><span class="sxs-lookup"><span data-stu-id="848c4-396">No</span></span></p></td>
<td><p><span data-ttu-id="848c4-397">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-397">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-398">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-398">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-399"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="848c4-399"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-400">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-400">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-401">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-401">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-402">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-402">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-403">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-403">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-404"><a href="delete-method-ado-recordset.md">Supprimer</a></span><span class="sxs-lookup"><span data-stu-id="848c4-404"><a href="delete-method-ado-recordset.md">Delete</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-405">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-405">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-406">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-406">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-407">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-407">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-408">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-409"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="848c4-409"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-410">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-410">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-411">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-411">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-412">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-412">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-413">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-413">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-414"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="848c4-414"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-415">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-415">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-416">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-416">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-417">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-417">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-418">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-418">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="848c4-419"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-420">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-420">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-421">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-421">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-422">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-422">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-423">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-423">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span><span class="sxs-lookup"><span data-stu-id="848c4-424"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-425">Non</span><span class="sxs-lookup"><span data-stu-id="848c4-425">No</span></span></p></td>
<td><p><span data-ttu-id="848c4-426">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-426">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-427">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-427">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-428">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span><span class="sxs-lookup"><span data-stu-id="848c4-429"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-430">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-430">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-431">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-431">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-432">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-432">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-433">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-433">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="848c4-434"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-435">Non</span><span class="sxs-lookup"><span data-stu-id="848c4-435">No</span></span></p></td>
<td><p><span data-ttu-id="848c4-436">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-436">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-437">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-437">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-438">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-438">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span><span class="sxs-lookup"><span data-stu-id="848c4-439"><a href="nextrecordset-method-ado.md">NextRecordset</a>\*</span></span></p></td>
<td><p><span data-ttu-id="848c4-440">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-440">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-441">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-441">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-442">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-442">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-443">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-444"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="848c4-444"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-445">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-445">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-446">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-446">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-447">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-447">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-448">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-448">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-449"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="848c4-449"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-450">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-450">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-451">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-451">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-452">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-452">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-453">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-453">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-454"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="848c4-454"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-455">Non</span><span class="sxs-lookup"><span data-stu-id="848c4-455">No</span></span></p></td>
<td><p><span data-ttu-id="848c4-456">Non</span><span class="sxs-lookup"><span data-stu-id="848c4-456">No</span></span></p></td>
<td><p><span data-ttu-id="848c4-457">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-457">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-458">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-459"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="848c4-459"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-460">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-460">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-461">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-461">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-462">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-462">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-463">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-463">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-464"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="848c4-464"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-465">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-465">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-466">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-466">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-467">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-467">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-468">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-468">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="848c4-469"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="848c4-470">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-470">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-471">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-471">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-472">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-472">Yes</span></span></p></td>
<td><p><span data-ttu-id="848c4-473">Oui</span><span class="sxs-lookup"><span data-stu-id="848c4-473">Yes</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="848c4-474">\*Non prise en charge avec les bases de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="848c4-474">\*Not supported for Microsoft Access databases.</span></span>

## <a name="dynamic-properties"></a><span data-ttu-id="848c4-475">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="848c4-475">Dynamic Properties</span></span>

<span data-ttu-id="848c4-476">Le fournisseur OLE DB pour ODBC insère plusieurs propriétés dynamiques dans la collection **Properties** des objets [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) et [Command](command-object-ado.md) non ouverts.</span><span class="sxs-lookup"><span data-stu-id="848c4-476">The Microsoft OLE DB Provider for ODBC inserts several dynamic properties into the **Properties** collection of the unopened [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md), and [Command](command-object-ado.md) objects.</span></span>

<span data-ttu-id="848c4-p118">Les tableaux suivants forment un index croisé des noms ADO et OLE DB de chaque propriété dynamique. Le guide OLE DB Programmer's Reference (en anglais) référence les noms de propriétés ADO sous le terme « Description ». Vous trouverez dans ce guide d'autres informations sur ces propriétés. Recherchez le nom de la propriété OLE DB dans l'Index ou consultez la rubrique « Appendix C: OLE DB Properties ».</span><span class="sxs-lookup"><span data-stu-id="848c4-p118">The tables below are a cross-index of the ADO and OLE DB names for each dynamic property. The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see Appendix C: OLE DB Properties.</span></span>

## <a name="connection-dynamic-properties"></a><span data-ttu-id="848c4-481">Propriétés dynamiques de connexion</span><span class="sxs-lookup"><span data-stu-id="848c4-481">Connection Dynamic Properties</span></span>

<span data-ttu-id="848c4-482">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="848c4-482">The following properties are added to the **Connection** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="848c4-483">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="848c4-483">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="848c4-484">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="848c4-484">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-485">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="848c4-485">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="848c4-486">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="848c4-486">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-487">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="848c4-487">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="848c4-488">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="848c4-488">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-489">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="848c4-489">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="848c4-490">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="848c4-490">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-491">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="848c4-491">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="848c4-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="848c4-492">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-493">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="848c4-493">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="848c4-494">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="848c4-494">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-495">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="848c4-495">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="848c4-496">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="848c4-496">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-497">Column Definition</span><span class="sxs-lookup"><span data-stu-id="848c4-497">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="848c4-498">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="848c4-498">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-499">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="848c4-499">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="848c4-500">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="848c4-500">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-501">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="848c4-501">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="848c4-502">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="848c4-502">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-503">Data Source</span><span class="sxs-lookup"><span data-stu-id="848c4-503">Data Source</span></span></p></td>
<td><p><span data-ttu-id="848c4-504">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="848c4-504">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-505">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="848c4-505">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="848c4-506">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="848c4-506">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-507">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="848c4-507">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="848c4-508">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="848c4-508">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-509">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="848c4-509">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="848c4-510">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="848c4-510">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-511">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="848c4-511">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="848c4-512">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="848c4-512">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-513">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="848c4-513">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="848c4-514">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="848c4-514">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-515">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="848c4-515">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="848c4-516">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="848c4-516">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-517">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="848c4-517">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="848c4-518">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="848c4-518">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-519">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="848c4-519">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="848c4-520">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="848c4-520">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-521">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="848c4-521">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="848c4-522">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="848c4-522">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-523">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="848c4-523">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="848c4-524">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="848c4-524">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-525">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="848c4-525">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="848c4-526">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="848c4-526">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-527">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="848c4-527">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="848c4-528">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="848c4-528">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-529">Emplacement</span><span class="sxs-lookup"><span data-stu-id="848c4-529">Location</span></span></p></td>
<td><p><span data-ttu-id="848c4-530">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="848c4-530">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-531">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="848c4-531">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="848c4-532">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="848c4-532">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-533">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="848c4-533">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="848c4-534">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="848c4-534">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-535">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="848c4-535">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="848c4-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="848c4-536">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-537">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="848c4-537">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="848c4-538">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="848c4-538">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-539">Mode</span><span class="sxs-lookup"><span data-stu-id="848c4-539">Mode</span></span></p></td>
<td><p><span data-ttu-id="848c4-540">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="848c4-540">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-541">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="848c4-541">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="848c4-542">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="848c4-542">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-543">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="848c4-543">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="848c4-544">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="848c4-544">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-545">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="848c4-545">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="848c4-546">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="848c4-546">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-547">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="848c4-547">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="848c4-548">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="848c4-548">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-549">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="848c4-549">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="848c4-550">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="848c4-550">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-551">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="848c4-551">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="848c4-552">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="848c4-552">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-553">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="848c4-553">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="848c4-554">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="848c4-554">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-555">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="848c4-555">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="848c4-556">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="848c4-556">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-557">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="848c4-557">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="848c4-558">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="848c4-558">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-559">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="848c4-559">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="848c4-560">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="848c4-560">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-561">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="848c4-561">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="848c4-562">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="848c4-562">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-563">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="848c4-563">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="848c4-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="848c4-564">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-565">Password</span><span class="sxs-lookup"><span data-stu-id="848c4-565">Password</span></span></p></td>
<td><p><span data-ttu-id="848c4-566">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="848c4-566">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-567">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="848c4-567">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="848c4-568">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="848c4-568">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-569">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="848c4-569">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="848c4-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="848c4-570">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-571">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="848c4-571">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="848c4-572">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="848c4-572">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-573">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="848c4-573">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="848c4-574">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="848c4-574">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-575">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="848c4-575">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="848c4-576">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="848c4-576">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-577">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="848c4-577">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="848c4-578">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="848c4-578">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-579">Prompt</span><span class="sxs-lookup"><span data-stu-id="848c4-579">Prompt</span></span></p></td>
<td><p><span data-ttu-id="848c4-580">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="848c4-580">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-581">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="848c4-581">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="848c4-582">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="848c4-582">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-583">Provider Name</span><span class="sxs-lookup"><span data-stu-id="848c4-583">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="848c4-584">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="848c4-584">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-585">Provider Version</span><span class="sxs-lookup"><span data-stu-id="848c4-585">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="848c4-586">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="848c4-586">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-587">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="848c4-587">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="848c4-588">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="848c4-588">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-589">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="848c4-589">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="848c4-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="848c4-590">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-591">Schema Term</span><span class="sxs-lookup"><span data-stu-id="848c4-591">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="848c4-592">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="848c4-592">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-593">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="848c4-593">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="848c4-594">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="848c4-594">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-595">SQL Support</span><span class="sxs-lookup"><span data-stu-id="848c4-595">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="848c4-596">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="848c4-596">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-597">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="848c4-597">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="848c4-598">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="848c4-598">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-599">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="848c4-599">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="848c4-600">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="848c4-600">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-601">Table Term</span><span class="sxs-lookup"><span data-stu-id="848c4-601">Table Term</span></span></p></td>
<td><p><span data-ttu-id="848c4-602">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="848c4-602">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-603">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="848c4-603">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="848c4-604">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="848c4-604">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-605">User ID</span><span class="sxs-lookup"><span data-stu-id="848c4-605">User ID</span></span></p></td>
<td><p><span data-ttu-id="848c4-606">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="848c4-606">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-607">User Name</span><span class="sxs-lookup"><span data-stu-id="848c4-607">User Name</span></span></p></td>
<td><p><span data-ttu-id="848c4-608">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="848c4-608">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-609">Window Handle</span><span class="sxs-lookup"><span data-stu-id="848c4-609">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="848c4-610">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="848c4-610">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a><span data-ttu-id="848c4-611">Propriétés dynamiques du jeu d'enregitrements</span><span class="sxs-lookup"><span data-stu-id="848c4-611">Recordset Dynamic Properties</span></span>

<span data-ttu-id="848c4-612">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="848c4-612">The following properties are added to the **Recordset** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="848c4-613">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="848c4-613">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="848c4-614">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="848c4-614">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-615">Access Order</span><span class="sxs-lookup"><span data-stu-id="848c4-615">Access Order</span></span></p></td>
<td><p><span data-ttu-id="848c4-616">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="848c4-616">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-617">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="848c4-617">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="848c4-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="848c4-618">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-619">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="848c4-619">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="848c4-620">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="848c4-620">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-621">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="848c4-621">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="848c4-622">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="848c4-622">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-623">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-623">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-624">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-624">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-625">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="848c4-625">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="848c4-626">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="848c4-626">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-627">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-627">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-628">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="848c4-628">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-629">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="848c4-629">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="848c4-630">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="848c4-630">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-631">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="848c4-631">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="848c4-632">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="848c4-632">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-633">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-633">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-634">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-634">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-635">IAccessor</span><span class="sxs-lookup"><span data-stu-id="848c4-635">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="848c4-636">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="848c4-636">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-637">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-637">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="848c4-638">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-638">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-639">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-639">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="848c4-640">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-640">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-641">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="848c4-641">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="848c4-642">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="848c4-642">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-643">IConvertType</span><span class="sxs-lookup"><span data-stu-id="848c4-643">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="848c4-644">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="848c4-644">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-645">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-645">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-646">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-646">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-647">IRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-647">IRowset</span></span></p></td>
<td><p><span data-ttu-id="848c4-648">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-648">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-649">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="848c4-649">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="848c4-650">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="848c4-650">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-651">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="848c4-651">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="848c4-652">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="848c4-652">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-653">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-653">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="848c4-654">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-654">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-655">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="848c4-655">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="848c4-656">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="848c4-656">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-657">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="848c4-657">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-658">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="848c4-658">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="848c4-659">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="848c4-659">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-660">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="848c4-660">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="848c4-661">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="848c4-661">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-662">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-662">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="848c4-663">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-663">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-664">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="848c4-664">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="848c4-665">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="848c4-665">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-666">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="848c4-666">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="848c4-667">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="848c4-667">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-668">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-668">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-669">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-669">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-670">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-670">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-671">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-671">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-672">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-672">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-673">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-673">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-674">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="848c4-674">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="848c4-675">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="848c4-675">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-676">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="848c4-676">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="848c4-677">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="848c4-677">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-678">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="848c4-678">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="848c4-679">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="848c4-679">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-680">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="848c4-680">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="848c4-681">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="848c4-681">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-682">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="848c4-682">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="848c4-683">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="848c4-683">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-684">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="848c4-684">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="848c4-685">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="848c4-685">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-686">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="848c4-686">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="848c4-687">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="848c4-687">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-688">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="848c4-688">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="848c4-689">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="848c4-689">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-690">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="848c4-690">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="848c4-691">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="848c4-691">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-692">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-692">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-693">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="848c4-693">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-694">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="848c4-694">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="848c4-695">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="848c4-695">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-696">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="848c4-696">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="848c4-697">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="848c4-697">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-698">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-698">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-699">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="848c4-699">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-700">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-700">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-701">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="848c4-701">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-702">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-702">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-703">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="848c4-703">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-704">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="848c4-704">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="848c4-705">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="848c4-705">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-706">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-706">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-707">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="848c4-707">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-708">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="848c4-708">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="848c4-709">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="848c4-709">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-710">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-710">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-711">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="848c4-711">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-712">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-712">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-713">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="848c4-713">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-714">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-714">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-715">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="848c4-715">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-716">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-716">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-717">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="848c4-717">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-718">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-718">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="848c4-719">DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-720">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-720">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-721">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="848c4-721">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-722">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="848c4-722">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="848c4-723">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="848c4-723">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-724">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="848c4-724">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="848c4-725">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="848c4-725">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-726">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="848c4-726">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="848c4-727">DBPROP_STRONGITDENTITY</span><span class="sxs-lookup"><span data-stu-id="848c4-727">DBPROP_STRONGITDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-728">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-728">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-729">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-729">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-730">Updatability</span><span class="sxs-lookup"><span data-stu-id="848c4-730">Updatability</span></span></p></td>
<td><p><span data-ttu-id="848c4-731">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="848c4-731">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-732">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="848c4-732">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="848c4-733">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="848c4-733">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a><span data-ttu-id="848c4-734">Propriétés dynamiques de la commande</span><span class="sxs-lookup"><span data-stu-id="848c4-734">Command Dynamic Properties</span></span>

<span data-ttu-id="848c4-735">Les propriétés suivantes sont ajoutées à la collection **Properties** de l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="848c4-735">The following properties are added to the **Command** object's **Properties** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="848c4-736">Nom de la propriété ADO</span><span class="sxs-lookup"><span data-stu-id="848c4-736">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="848c4-737">Nom de la propriété OLE DB</span><span class="sxs-lookup"><span data-stu-id="848c4-737">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="848c4-738">Access Order</span><span class="sxs-lookup"><span data-stu-id="848c4-738">Access Order</span></span></p></td>
<td><p><span data-ttu-id="848c4-739">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="848c4-739">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-740">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="848c4-740">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="848c4-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="848c4-741">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-742">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="848c4-742">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="848c4-743">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="848c4-743">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-744">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="848c4-744">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="848c4-745">DBPROP_IROWSETLOCATE</span><span class="sxs-lookup"><span data-stu-id="848c4-745">DBPROP_IROWSETLOCATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-746">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-746">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-747">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-747">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-748">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="848c4-748">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="848c4-749">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="848c4-749">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-750">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-750">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-751">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="848c4-751">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-752">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="848c4-752">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="848c4-753">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="848c4-753">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-754">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="848c4-754">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="848c4-755">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="848c4-755">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-756">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-756">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-757">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-757">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-758">IAccessor</span><span class="sxs-lookup"><span data-stu-id="848c4-758">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="848c4-759">DBPROP_IAccessor</span><span class="sxs-lookup"><span data-stu-id="848c4-759">DBPROP_IAccessor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-760">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-760">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="848c4-761">DBPROP_IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-761">DBPROP_IColumnsInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-762">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-762">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="848c4-763">DBPROP_IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-763">DBPROP_IColumnsRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-764">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="848c4-764">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="848c4-765">DBPROP_IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="848c4-765">DBPROP_IConnectionPointContainer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-766">IConvertType</span><span class="sxs-lookup"><span data-stu-id="848c4-766">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="848c4-767">DBPROP_IConvertType</span><span class="sxs-lookup"><span data-stu-id="848c4-767">DBPROP_IConvertType</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-768">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-768">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-769">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-769">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-770">IRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-770">IRowset</span></span></p></td>
<td><p><span data-ttu-id="848c4-771">DBPROP_IRowset</span><span class="sxs-lookup"><span data-stu-id="848c4-771">DBPROP_IRowset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-772">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="848c4-772">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="848c4-773">DBPROP_IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="848c4-773">DBPROP_IRowsetChange</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-774">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="848c4-774">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="848c4-775">DBPROP_IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="848c4-775">DBPROP_IRowsetIdentity</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-776">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-776">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="848c4-777">DBPROP_IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-777">DBPROP_IRowsetInfo</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-778">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="848c4-778">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="848c4-779">DBPROP_IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="848c4-779">DBPROP_IRowsetLocate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-780">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="848c4-780">IRowsetResynch</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-781">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="848c4-781">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="848c4-782">DBPROP_IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="848c4-782">DBPROP_IRowsetUpdate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-783">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="848c4-783">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="848c4-784">DBPROP_ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="848c4-784">DBPROP_ISequentialStream</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-785">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-785">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="848c4-786">DBPROP_ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="848c4-786">DBPROP_ISupportErrorInfo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-787">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="848c4-787">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="848c4-788">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="848c4-788">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-789">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="848c4-789">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="848c4-790">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="848c4-790">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-791">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-791">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-792">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-792">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-793">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-793">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-794">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-794">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-795">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-795">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-796">DBPROP_MAXROWS</span><span class="sxs-lookup"><span data-stu-id="848c4-796">DBPROP_MAXROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-797">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="848c4-797">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="848c4-798">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="848c4-798">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-799">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="848c4-799">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="848c4-800">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="848c4-800">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-801">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="848c4-801">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="848c4-802">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="848c4-802">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-803">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="848c4-803">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="848c4-804">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="848c4-804">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-805">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="848c4-805">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="848c4-806">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="848c4-806">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-807">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="848c4-807">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="848c4-808">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="848c4-808">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-809">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="848c4-809">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="848c4-810">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="848c4-810">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-811">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="848c4-811">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="848c4-812">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="848c4-812">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-813">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="848c4-813">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="848c4-814">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="848c4-814">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-815">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="848c4-815">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="848c4-816">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="848c4-816">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-817">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="848c4-817">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="848c4-818">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="848c4-818">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-819">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="848c4-819">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="848c4-820">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="848c4-820">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-821">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-821">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-822">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="848c4-822">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-823">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-823">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-824">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="848c4-824">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-825">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-825">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-826">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="848c4-826">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-827">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="848c4-827">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="848c4-828">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="848c4-828">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-829">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-829">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-830">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="848c4-830">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-831">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="848c4-831">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="848c4-832">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="848c4-832">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-833">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-833">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-834">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="848c4-834">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-835">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-835">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-836">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="848c4-836">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-837">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-837">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-838">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="848c4-838">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-839">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-839">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-840">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="848c4-840">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-841">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-841">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="848c4-842">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-843">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="848c4-843">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="848c4-844">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="848c4-844">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-845">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="848c4-845">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="848c4-846">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="848c4-846">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-847">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="848c4-847">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="848c4-848">DBPROP_BOOKMARKSKIP</span><span class="sxs-lookup"><span data-stu-id="848c4-848">DBPROP_BOOKMARKSKIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-849">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="848c4-849">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="848c4-850">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="848c4-850">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="848c4-851">Updatability</span><span class="sxs-lookup"><span data-stu-id="848c4-851">Updatability</span></span></p></td>
<td><p><span data-ttu-id="848c4-852">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="848c4-852">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="848c4-853">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="848c4-853">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="848c4-854">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="848c4-854">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="848c4-855">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="848c4-855">See also</span></span>

<span data-ttu-id="848c4-856">Pour plus [d’informations sur l’implémentation](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) spécifique et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour ODBC, consultez le Guide du programmeur OLE DB ou visitez le Centre de développement de plateforme de [données.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="848c4-856">For details regarding specific implementation and functional information about the Microsoft OLE DB Provider for ODBC, consult the [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).</span></span>

