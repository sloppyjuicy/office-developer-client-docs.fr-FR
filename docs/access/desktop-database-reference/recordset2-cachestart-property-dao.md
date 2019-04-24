---
title: Recordset2. CacheStart, propriété (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307419"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="59ade-102">Recordset2. CacheStart, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="59ade-102">Recordset2.CacheStart property (DAO)</span></span>


<span data-ttu-id="59ade-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59ade-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59ade-104">Définit ou renvoie une valeur spécifiant le signet du premier enregistrement d’un objet Recordset de type feuille de réponse dynamique qui contient des données d’une source de données ODBC à placer dans le cache local (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="59ade-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="59ade-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59ade-105">Syntax</span></span>

<span data-ttu-id="59ade-106">*expression* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="59ade-106">*expression* .CacheStart</span></span>

<span data-ttu-id="59ade-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="59ade-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ade-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="59ade-108">Remarks</span></span>

<span data-ttu-id="59ade-p101">La mise en cache des données améliore les performances si vous utilisez des objets **Recordset** pour extraire des données d'un serveur distant. Un cache est un espace de la mémoire locale qui conserve les données récemment extraites du serveur. La mise en cache est utile si les utilisateurs demandent à nouveau les données au cours de la même session d'application. En cas de demande des données, le moteur de base de données Microsoft Access vérifie si les données demandées figurent dans le cache avant de tenter de les récupérer auprès du serveur, ce qui prend plus longtemps. Le cache enregistre uniquement des données issues d'une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="59ade-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="59ade-p102">N'importe quelle source de données ODBC connectée au moteur de base de données Microsoft Access, telle qu'une table liée, peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante, définissez les propriétés **CacheSize** et **[CacheStart](recordset2-cachestart-property-dao.md)** puis utilisez la méthode **[FillCache](recordset2-fillcache-method-dao.md)** ou parcourez les enregistrements à l'aide des méthodes **Move**.</span><span class="sxs-lookup"><span data-stu-id="59ade-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="59ade-p103">Le paramètre de la propriété **CacheStart** est le signet du premier enregistrement de l'objet **Recordset** à mettre en cache. Vous pouvez utiliser le signet d'un enregistrement quelconque pour définir la propriété **CacheStart**. Définissez en tant qu'enregistrement actif le premier enregistrement à mettre en cache et affectez à la propriété **CacheStart** la même valeur que la propriété **[Bookmark](recordset2-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="59ade-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="59ade-118">Le moteur de base de données Microsoft Access demande au cache les enregistrements compris dans la plage du cache et demande au serveur les enregistrements hors cache.</span><span class="sxs-lookup"><span data-stu-id="59ade-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="59ade-119">Les enregistrements extraits du cache ne reflètent pas les modifications apportées simultanément par d'autres utilisateurs à la source de données.</span><span class="sxs-lookup"><span data-stu-id="59ade-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="59ade-120">Pour forcer une mise à jour de toutes les données mises en cache, affectez à la propriété **CacheSize** de l'objet **Recordset** la valeur 0, réaffectez-lui une valeur correspondant à la taille du cache initialement demandé puis utilisez la méthode **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="59ade-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

