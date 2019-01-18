---
title: Propriété Recordset2.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718797"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="d0641-102">Propriété Recordset2.CacheStart (DAO)</span><span class="sxs-lookup"><span data-stu-id="d0641-102">Recordset2.CacheStart property (DAO)</span></span>


<span data-ttu-id="d0641-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0641-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0641-104">Définit ou renvoie une valeur qui spécifie le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique contenant des données à mettre en cache local à partir d'une source de données ODBC (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="d0641-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0641-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0641-105">Syntax</span></span>

<span data-ttu-id="d0641-106">*expression* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="d0641-106">*expression* .CacheStart</span></span>

<span data-ttu-id="d0641-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d0641-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0641-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0641-108">Remarks</span></span>

<span data-ttu-id="d0641-p101">La mise en cache des données améliore les performances si vous utilisez des objets **Recordset** pour récupérer des données d'un serveur distant. Le cache est un espace en mémoire locale qui contient les données les plus récentes extraites du serveur. Il s'avère utile lorsque l'utilisateur demande à nouveau des données lors de l'exécution de l'application. En effet, lorsque l'utilisateur demande des données, le moteur de base de données Microsoft Access vérifie d'abord la présence des données demandées dans le cache, au lieu de les extraire du serveur, ce qui est plus long. Le cache n'enregistre que les données issues d'une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="d0641-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="d0641-p102">Toute source de données ODBC reliée à un moteur de base de données Microsoft Access (table liée, par exemple) peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante, définissez les propriétés **CacheSize** et **[CacheStart](recordset2-cachestart-property-dao.md)**, puis utilisez la méthode **[FillCache](recordset2-fillcache-method-dao.md)** ou parcourez les enregistrements à l'aide des méthodes **Move**.</span><span class="sxs-lookup"><span data-stu-id="d0641-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="d0641-p103">La valeur de la propriété **CacheStart** correspond au signet du premier enregistrement dans l'objet **Recordset** à mettre en cache. Vous pouvez utiliser le signet de n'importe quel enregistrement pour définir la propriété **CacheStart**. Définissez l'enregistrement à placer au début du cache comme enregistrement actif et paramétrez la propriété **CacheStart** en fonction de la valeur de la propriété **[Bookmark](recordset2-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d0641-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="d0641-118">Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="d0641-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="d0641-119">Les enregistrements extraits du cache ne répercutent pas les modifications apportées simultanément aux données sources par les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d0641-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="d0641-120">Pour forcer la mise à jour de toutes les données mises en cache, définissez la propriété **CacheSize** de l'objet **Recordset** sur la valeur 0, redéfinissez-la en fonction de la taille du cache demandée à l'origine, puis utilisez la méthode **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="d0641-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

