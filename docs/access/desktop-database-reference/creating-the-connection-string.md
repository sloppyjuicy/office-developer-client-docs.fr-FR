---
title: Création de la chaîne de connexion
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8420beb2c6136123c334a55b68bd6601f214faa5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472331"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="8920f-102">Création de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="8920f-102">Creating the Connection String</span></span>


<span data-ttu-id="8920f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8920f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8920f-p101">ADO prend directement en charge cinq arguments dans une chaîne de connexion. D'autres arguments sont transférés au fournisseur mentionné dans l'argument *Fournisseur* sans aucun traitement de la part d'ADO.</span><span class="sxs-lookup"><span data-stu-id="8920f-p101">ADO directly supports five arguments in a connection string. Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8920f-106">Argument</span><span class="sxs-lookup"><span data-stu-id="8920f-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="8920f-107">Description</span><span class="sxs-lookup"><span data-stu-id="8920f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8920f-108"><em>Provider</em></span><span class="sxs-lookup"><span data-stu-id="8920f-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="8920f-109">Spécifie le nom d'un fournisseur à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="8920f-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8920f-110"><em>Nom du fichier</em></span><span class="sxs-lookup"><span data-stu-id="8920f-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="8920f-111">Spécifie le nom d'un fichier spécifique au fournisseur (par exemple, un objet de source de données persistant) contenant des informations de connexion prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="8920f-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8920f-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="8920f-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="8920f-113">Spécifie la chaîne de connexion sous la forme d'une URL absolue identifiant une ressource, comme un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="8920f-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8920f-114"><em>Fournisseur distant</em></span><span class="sxs-lookup"><span data-stu-id="8920f-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="8920f-p102">Spécifie le nom d'un fournisseur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</span><span class="sxs-lookup"><span data-stu-id="8920f-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8920f-117"><em>Serveur distant</em></span><span class="sxs-lookup"><span data-stu-id="8920f-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="8920f-p103">Spécifie le nom de chemin du serveur à utiliser pour les connexions côté client. (Remote Data Service uniquement.)</span><span class="sxs-lookup"><span data-stu-id="8920f-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="8920f-p104">Dans les exemples suivants ainsi que dans l'ensemble du guide du programmeur ADO, l'ID d'utilisateur « MyId » associé au mot de passe « 123aBc » est utilisé pour l'authentification auprès du serveur. Remplacez ces valeurs par des informations d'identification valides pour votre serveur. Remplacez également le nom de votre serveur par « MySqlServer ».</span><span class="sxs-lookup"><span data-stu-id="8920f-p104">In the following examples and throughout the ADO Programmer's Guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid login credentials for your server. Also, substitute the name of your server for "MySqlServer".</span></span></P>



<span data-ttu-id="8920f-123">Dans le chapitre 1, l'application HelloData a utilisé la chaîne de connexion suivante :</span><span class="sxs-lookup"><span data-stu-id="8920f-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="8920f-124">Le seul paramètre ADO fourni dans cette chaîne de connexion était « Provider=SQLOLEDB », qui indiquait le fournisseur Microsoft OLE DB pour SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8920f-124">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server.</span></span> <span data-ttu-id="8920f-125">Reportez-vous à la documentation de chaque fournisseur pour déterminer les autres paramètres valides pouvant être transférés dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="8920f-125">Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation.</span></span> <span data-ttu-id="8920f-126">Selon le fournisseur OLE DB pour la documentation SQL Server, vous pouvez remplacer « Serveur » pour le paramètre *Source de données* et « Database » pour le paramètre *Initial Catalog* .</span><span class="sxs-lookup"><span data-stu-id="8920f-126">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter.</span></span> <span data-ttu-id="8920f-127">Ainsi, la chaîne de connexion suivante devrait produire les mêmes résultats que la première :</span><span class="sxs-lookup"><span data-stu-id="8920f-127">Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="8920f-128">Pour ouvrir la connexion, transmettez simplement la chaîne de connexion comme premier argument dans la méthode **Connection** objet **Open**:</span><span class="sxs-lookup"><span data-stu-id="8920f-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="8920f-p106">Il est également possible de fournir la plupart de ces informations en définissant les propriétés de l'objet **Connection** avant d'ouvrir la connexion. Par exemple, vous pourriez obtenir le même résultat que la chaîne de connexion précédente en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="8920f-p106">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection. For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

