---
title: Open, méthode (connexion ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288426"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="fab16-102">Open, méthode (connexion ADO)</span><span class="sxs-lookup"><span data-stu-id="fab16-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="fab16-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fab16-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="fab16-104">Ouvre une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="fab16-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab16-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fab16-105">Syntax</span></span>

<span data-ttu-id="fab16-106">*connexion*. Open*ConnectionString*, *userid*, *Password*, *options*</span><span class="sxs-lookup"><span data-stu-id="fab16-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="fab16-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fab16-107">Parameters</span></span>

|<span data-ttu-id="fab16-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fab16-108">Parameter</span></span>|<span data-ttu-id="fab16-109">Description</span><span class="sxs-lookup"><span data-stu-id="fab16-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fab16-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="fab16-110">*ConnectionString*</span></span> |<span data-ttu-id="fab16-p101">Facultatif. Valeur de type **String** contenant des informations de connexion. Consultez la propriété [ConnectionString](connectionstring-property-ado.md) pour en savoir plus sur les paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="fab16-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="fab16-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="fab16-114">*UserID*</span></span> |<span data-ttu-id="fab16-p102">Facultatif. Valeur de type **String** contenant le nom d'utilisateur à employer lors de l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="fab16-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="fab16-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="fab16-117">*Password*</span></span> |<span data-ttu-id="fab16-p103">Facultatif. Valeur de type **String** contenant le mot de passe à employer lors de l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="fab16-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="fab16-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="fab16-120">*Options*</span></span> |<span data-ttu-id="fab16-p104">Facultatif. Valeur [ConnectOptionEnum](connectoptionenum.md) qui détermine si cette méthode doit être exécutée après l'établissement de la connexion (de façon synchrone) ou avant (de façon asynchrone).</span><span class="sxs-lookup"><span data-stu-id="fab16-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fab16-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="fab16-123">Remarks</span></span>

<span data-ttu-id="fab16-p105">L’utilisation de la méthode **Open** sur un objet [Connection](connection-object-ado.md) établit la connexion physique à une source de données. Une fois l’exécution de la méthode terminée, la connexion est active et vous pouvez exécuter des commandes sur cette connexion et traiter les résultats.</span><span class="sxs-lookup"><span data-stu-id="fab16-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="fab16-126">Utilisez l'argument facultatif *ConnectionString* pour spécifier une chaîne de connexion contenant une série d'instructions *argument* *= valeur* séparées par des points-virgules ou une ressource de fichier ou de répertoire identifiée par une URL.</span><span class="sxs-lookup"><span data-stu-id="fab16-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="fab16-127">La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l'argument *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="fab16-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="fab16-128">Par conséquent, vous pouvez soit définir la propriété **ConnectionString** de l'objet **Connection** avant d'ouvrir celui-ci, soit utiliser l'argument *ConnectionString* pour définir ou substituer les paramètres de connexion actifs lors de l'appel de la méthode **Open**.</span><span class="sxs-lookup"><span data-stu-id="fab16-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="fab16-129">Si vous passez des données de mot de passe et d'utilisateur dans l'argument *ConnectionString* et dans les arguments facultatifs *UserID* et *Password*, les arguments *UserID* et *Password* se substituent aux valeurs spécifiées dans l'argument *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="fab16-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="fab16-p107">Une fois vos opérations sur l’objet **Connection** ouvert terminées, utilisez la méthode [Close](close-method-ado.md) pour libérer les ressources système associées. La fermeture d’un objet ne le supprime pas de la mémoire  ; vous pouvez modifier ses paramètres de propriétés et utiliser la méthode **Open** pour le rouvrir ultérieurement. Pour éliminer complètement un objet de la mémoire, vous devez définir la variable objet à *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="fab16-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="fab16-133">**Utilisation des services de données à distance** Lorsqu'elle est utilisée sur un objet **Connection** côté client, la méthode **Open** n'établit pas de connexion au serveur tant qu' [](recordset-object-ado.md) un objet Recordset n'est pas ouvert sur l'objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="fab16-133">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="fab16-134">Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="fab16-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="fab16-135">Pour plus d'informations, consultez la rubrique [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="fab16-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


