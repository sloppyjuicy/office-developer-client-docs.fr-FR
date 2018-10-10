---
title: Open, méthode (objet Connection ADO)
TOCTitle: Open Method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33d3abd4ebf188534dbaefd9e7668453635a7aaa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471658"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="58a5d-102">Open, méthode (objet Connection ADO)</span><span class="sxs-lookup"><span data-stu-id="58a5d-102">Open Method (ADO Connection)</span></span>


<span data-ttu-id="58a5d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="58a5d-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="58a5d-104">Ouvre une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="58a5d-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58a5d-105">Syntax</span></span>

<span data-ttu-id="58a5d-106">*connexion*. Ouvrez*ConnectionString*, *UserID*, *le mot de passe*, *Options*</span><span class="sxs-lookup"><span data-stu-id="58a5d-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="58a5d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58a5d-107">Parameters</span></span>

  - <span data-ttu-id="58a5d-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="58a5d-108">*ConnectionString*</span></span>

  - <span data-ttu-id="58a5d-p101">Facultatif. Valeur de type **String** contenant des informations de connexion. Consultez la propriété [ConnectionString](connectionstring-property-ado.md) pour en savoir plus sur les paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="58a5d-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>

  - <span data-ttu-id="58a5d-112">*Nom d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="58a5d-112">*UserID*</span></span>

  - <span data-ttu-id="58a5d-p102">Facultatif. Valeur de type **String** contenant le nom d'utilisateur à employer lors de l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="58a5d-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>

  - <span data-ttu-id="58a5d-115">*Password*</span><span class="sxs-lookup"><span data-stu-id="58a5d-115">*Password*</span></span>

  - <span data-ttu-id="58a5d-p103">Facultatif. Valeur de type **String** contenant le mot de passe à employer lors de l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="58a5d-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>

  - <span data-ttu-id="58a5d-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="58a5d-118">*Options*</span></span>

  - <span data-ttu-id="58a5d-p104">Facultatif. Valeur [ConnectOptionEnum](connectoptionenum.md) qui détermine si cette méthode doit être exécutée après l'établissement de la connexion (de façon synchrone) ou avant (de façon asynchrone).</span><span class="sxs-lookup"><span data-stu-id="58a5d-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

## <a name="remarks"></a><span data-ttu-id="58a5d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="58a5d-121">Remarks</span></span>

<span data-ttu-id="58a5d-p105">L'utilisation de la méthode **Open** sur un objet [Connection](connection-object-ado.md) établit la connexion physique à une source de données. Une fois l'exécution de la méthode terminée, la connexion est active et vous pouvez exécuter des commandes sur cette connexion et traiter les résultats.</span><span class="sxs-lookup"><span data-stu-id="58a5d-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="58a5d-124">Utilisez l’argument facultatif *ConnectionString* pour spécifier une chaîne de connexion contenant une série d’instructions *argument* *= valeur* séparées par des points-virgules, ou un fichier ou une ressource de répertoire identifiée par une URL.</span><span class="sxs-lookup"><span data-stu-id="58a5d-124">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="58a5d-125">La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l’argument *ConnectionString* .</span><span class="sxs-lookup"><span data-stu-id="58a5d-125">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="58a5d-126">Par conséquent, vous pouvez définir la propriété **ConnectionString** de l’objet **Connection** avant de l’ouvrir, ou utilisez l’argument *ConnectionString* pour définir ou substituer les paramètres de connexion en cours pendant l’appel de méthode **Open** .</span><span class="sxs-lookup"><span data-stu-id="58a5d-126">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="58a5d-127">Si vous passez des données de mot de passe et d'utilisateur dans l'argument *ConnectionString* et dans les arguments facultatifs *UserID* et *Password*, les arguments *UserID* et *Password* se substituent aux valeurs spécifiées dans l'argument *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="58a5d-127">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="58a5d-p107">Une fois vos opérations sur l’objet **Connection** ouvert terminées, utilisez la méthode [Close](close-method-ado.md) pour libérer les ressources système associées. La fermeture d’un objet ne le supprime pas de la mémoire  ; vous pouvez modifier ses paramètres de propriétés et utiliser la méthode **Open** pour le rouvrir ultérieurement. Pour éliminer complètement un objet de la mémoire, vous devez définir la variable objet à *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="58a5d-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="58a5d-131">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet de **connexion** côté client, la méthode **Open** n’établit pas effective une connexion au serveur jusqu'à ce qu’un [objet Recordset](recordset-object-ado.md) est ouvert sur l’objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="58a5d-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="58a5d-p108">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</span><span class="sxs-lookup"><span data-stu-id="58a5d-p108">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


