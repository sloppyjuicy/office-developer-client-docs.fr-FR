---
title: Création de la chaîne de connexion
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295326"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="bc903-102">Création de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="bc903-102">Creating the connection string</span></span>

<span data-ttu-id="bc903-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc903-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc903-p101">ADO prend directement en charge cinq arguments dans une chaîne de connexion. D'autres arguments sont transférés au fournisseur mentionné dans l'argument *Fournisseur* sans aucun traitement de la part d'ADO.</span><span class="sxs-lookup"><span data-stu-id="bc903-p101">ADO directly supports five arguments in a connection string. Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc903-106">Argument</span><span class="sxs-lookup"><span data-stu-id="bc903-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="bc903-107">Description</span><span class="sxs-lookup"><span data-stu-id="bc903-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc903-108"><em>Provider</em></span><span class="sxs-lookup"><span data-stu-id="bc903-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="bc903-109">Spécifie le nom d'un fournisseur à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="bc903-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc903-110"><em>Nom du fichier</em></span><span class="sxs-lookup"><span data-stu-id="bc903-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="bc903-111">Spécifie le nom d'un fichier spécifique au fournisseur (par exemple, un objet de source de données persistant) contenant des informations de connexion prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="bc903-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc903-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="bc903-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="bc903-113">Spécifie la chaîne de connexion sous la forme d'une URL absolue identifiant une ressource, comme un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="bc903-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc903-114"><em>Fournisseur distant</em></span><span class="sxs-lookup"><span data-stu-id="bc903-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="bc903-p102">Spécifie le nom d'un fournisseur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</span><span class="sxs-lookup"><span data-stu-id="bc903-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc903-117"><em>Serveur distant</em></span><span class="sxs-lookup"><span data-stu-id="bc903-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="bc903-p103">Spécifie le nom du chemin d'accès du serveur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</span><span class="sxs-lookup"><span data-stu-id="bc903-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="bc903-120">Dans les exemples suivants et dans le guide du programmeur ADO, l’ID d’utilisateur « MyId » avec le mot de passe « 123aBc » est utilisé pour s’authentifier auprès du serveur.</span><span class="sxs-lookup"><span data-stu-id="bc903-120">In the following examples and throughout the ADO programmer's guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="bc903-121">Remplacez ces valeurs par des informations d'identification valides pour votre serveur.</span><span class="sxs-lookup"><span data-stu-id="bc903-121">You should substitute these values with valid login credentials for your server.</span></span> <span data-ttu-id="bc903-122">Remplacez également le nom de votre serveur par « MySqlServer ».</span><span class="sxs-lookup"><span data-stu-id="bc903-122">Also, substitute the name of your server for "MySqlServer".</span></span>

<span data-ttu-id="bc903-123">Dans le chapitre 1, l'application HelloData a utilisé la chaîne de connexion suivante :</span><span class="sxs-lookup"><span data-stu-id="bc903-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="bc903-p105">Le seul paramètre ADO fourni dans cette chaîne de connexion était « Provider=SQLOLEDB », qui indiquait le fournisseur Microsoft OLE DB pour SQL Server. Reportez-vous à la documentation de chaque fournisseur pour déterminer les autres paramètres valides pouvant être transférés dans la chaîne de connexion. Selon la documentation du fournisseur OLE DB pour SQL Server, vous pouvez remplacer « Server » par le paramètre *Source de données* et « Database » par le paramètre *Catalogue initial*. Ainsi, la chaîne de connexion suivante devrait produire les mêmes résultats que la première :</span><span class="sxs-lookup"><span data-stu-id="bc903-p105">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server. Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation. According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter. Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="bc903-128">Pour ouvrir la connexion, transmettez simplement la chaîne de connexion comme premier argument dans la méthode **Connection** objet **Open**:</span><span class="sxs-lookup"><span data-stu-id="bc903-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="bc903-p106">Il est également possible de fournir la plupart de ces informations en définissant les propriétés de l'objet **Connection** avant d'ouvrir la connexion. Par exemple, vous pourriez obtenir le même résultat que la chaîne de connexion précédente en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bc903-p106">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection. For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

