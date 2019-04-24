---
title: ConnectionString, propriété (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295708"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="13cbe-102">ConnectionString, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="13cbe-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="13cbe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13cbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13cbe-104">Indique les informations utilisées pour se connecter à une source de données.</span><span class="sxs-lookup"><span data-stu-id="13cbe-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="13cbe-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="13cbe-105">Settings and return values</span></span>

<span data-ttu-id="13cbe-106">Définit ou renvoie une valeur de type **String**.</span><span class="sxs-lookup"><span data-stu-id="13cbe-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13cbe-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="13cbe-107">Remarks</span></span>

<span data-ttu-id="13cbe-108">Utilisez la propriété **ConnectionString** pour spécifier une source de données en passant une chaîne de connexion détaillée contenant une série d'instructions *argument* *= valeur* séparées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="13cbe-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="13cbe-p101">ADO prend en charge cinq arguments pour la propriété **ConnectionString**. Tous les autres arguments sont transmis directement au fournisseur sans aucun traitement par ADO. Les arguments pris en charge par ADO sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="13cbe-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13cbe-111">Argument</span><span class="sxs-lookup"><span data-stu-id="13cbe-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="13cbe-112">Description</span><span class="sxs-lookup"><span data-stu-id="13cbe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13cbe-113"><em>Provider =</em></span><span class="sxs-lookup"><span data-stu-id="13cbe-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="13cbe-114">Spécifie le nom d'un fournisseur à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="13cbe-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cbe-115"><em>File Name=</em></span><span class="sxs-lookup"><span data-stu-id="13cbe-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="13cbe-116">Spécifie le nom d'un fichier spécifique au fournisseur (par exemple, un objet de source de données persistant) contenant des informations de connexion prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="13cbe-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cbe-117"><em>Remote Provider=</em></span><span class="sxs-lookup"><span data-stu-id="13cbe-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="13cbe-118">Spécifie le nom d'un fournisseur à utiliser pour les connexions côté client.</span><span class="sxs-lookup"><span data-stu-id="13cbe-118">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="13cbe-119">(Remote Data Service uniquement.)</span><span class="sxs-lookup"><span data-stu-id="13cbe-119">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cbe-120"><em>Remote Server=</em></span><span class="sxs-lookup"><span data-stu-id="13cbe-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="13cbe-p103">Spécifie le nom du chemin d'accès du serveur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</span><span class="sxs-lookup"><span data-stu-id="13cbe-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cbe-123"><em>URL =</em></span><span class="sxs-lookup"><span data-stu-id="13cbe-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="13cbe-124">Spécifie la chaîne de connexion sous la forme d'une URL absolue identifiant une ressource, comme un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="13cbe-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="13cbe-125">Une fois que vous avez défini la propriété **ConnectionString** et ouvert l’objet [Connection](connection-object-ado.md), le fournisseur peut modifier le contenu de la propriété, par exemple, en mappant les noms d’arguments définis par ADO aux équivalents du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="13cbe-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="13cbe-126">La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md) afin que vous puissiez remplacer la propriété **ConnectionString** actuelle lors de l’appel de la méthode **Open**.</span><span class="sxs-lookup"><span data-stu-id="13cbe-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="13cbe-127">Si vous spécifiez l'argument *File Name*, ADO charge le fournisseur associé. Dès lors, vous ne pouvez pas passer en même temps les arguments *Provider* et *File Name*.</span><span class="sxs-lookup"><span data-stu-id="13cbe-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="13cbe-128">La propriété **ConnectionString** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="13cbe-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="13cbe-p104">Les doublons d'un argument dans la propriété **ConnectionString** ne sont pas pris en compte. C'est la dernière instance de l'argument qui est utilisée.</span><span class="sxs-lookup"><span data-stu-id="13cbe-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="13cbe-131">**Utilisation des services de données à distance** Lorsqu'elle est utilisée sur un objet **Connection** côté client, la propriété **ConnectionString** peut inclure uniquement les paramètres Remote *Provider* et *Remote Server* .</span><span class="sxs-lookup"><span data-stu-id="13cbe-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

