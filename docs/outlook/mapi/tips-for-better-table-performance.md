---
title: Conseils pour améliorer les performances d’une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327796"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="024fc-103">Conseils pour améliorer les performances d’une table</span><span class="sxs-lookup"><span data-stu-id="024fc-103">Tips for better table performance</span></span>
  
<span data-ttu-id="024fc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="024fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="024fc-105">Étant donné que de nombreuses opérations de table peuvent prendre du temps et qu'il n'existe aucun moyen d'indiquer la progression, il est utile d'utiliser les techniques suivantes pour améliorer les performances:</span><span class="sxs-lookup"><span data-stu-id="024fc-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="024fc-106">**Créer une fonction [IMAPITable: appels IUnknown](imapitableiunknown.md) dans le bon ordre**</span><span class="sxs-lookup"><span data-stu-id="024fc-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="024fc-107">Les clients et les fournisseurs de services peuvent travailler avec des tableaux de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="024fc-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="024fc-108">Ils peuvent ouvrir le tableau et extraire les données de toutes les lignes à l'aide du jeu de colonnes et de l'ordre de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="024fc-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="024fc-109">Ils peuvent également modifier cette vue par défaut du tableau en modifiant le jeu de colonnes, en modifiant l'ordre de tri ou en établissant une restriction pour limiter l'étendue de la table.</span><span class="sxs-lookup"><span data-stu-id="024fc-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="024fc-110">Les utilisateurs de tableau qui envisagent d'effectuer une ou plusieurs de ces opérations avant de récupérer des données doivent les exécuter dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="024fc-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="024fc-111">Définissez un jeu de colonnes avec l'aide de la fonction [IMAPITable:: SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="024fc-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="024fc-112">Établissez une restriction avec la fonction [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="024fc-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="024fc-113">Définissez un ordre de tri à l'aide de la fonction [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="024fc-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="024fc-114">L'exécution de ces tâches dans cet ordre limite le nombre de lignes et de colonnes qui seront triées, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="024fc-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="024fc-115">**ReTarder une opération à l'aide de l'indicateur TBL_BATCH dans la mesure du possible**</span><span class="sxs-lookup"><span data-stu-id="024fc-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="024fc-116">La définition de\_l'indicateur de lot de tbl sur une méthode permet à l'implémenteur de table de collecter plusieurs appels avant d'agir sur l'un d'eux.</span><span class="sxs-lookup"><span data-stu-id="024fc-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="024fc-117">Au lieu de passer un grand nombre d'appels à un serveur distant; un implémenteur de tableau peut en créer un, ce qui effectue toutes les opérations à la fois.</span><span class="sxs-lookup"><span data-stu-id="024fc-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="024fc-118">Les résultats des opérations ne sont pas évalués tant qu'ils ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="024fc-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="024fc-119">Par exemple, lorsqu'un client appelle [IMAPITable:: Restrict](imapitable-restrict.md) pour spécifier une restriction avec l'\_indicateur de lot tbl défini, la restriction n'a pas besoin de prendre effet tant que le client n'appelle pas [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="024fc-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="024fc-120">Cela permet à l'implémenteur de tableau de combiner le travail de deux appels en un seul.</span><span class="sxs-lookup"><span data-stu-id="024fc-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="024fc-121">Les utilisateurs de tableau qui tirent parti\_de l'indicateur de lot tbl doivent savoir que la gestion des erreurs dans ces conditions peut être plus complexe.</span><span class="sxs-lookup"><span data-stu-id="024fc-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="024fc-122">Étant donné que la gestion des erreurs à partir d'une opération différée est similaire à\_la gestion des erreurs lors de la définition de l'indicateur MAPI DEFERRED_ERRORS, reportez-vous à la rubrique [Report des erreurs MAPI](deferring-mapi-errors.md) pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="024fc-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="024fc-123">**Conserver un cache des propriétés couramment utilisées**</span><span class="sxs-lookup"><span data-stu-id="024fc-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="024fc-124">Les fournisseurs de services qui implémentent des tables peuvent réduire le temps nécessaire pour créer une vue en mettant en cache des copies des propriétés d'objets couramment utilisées.</span><span class="sxs-lookup"><span data-stu-id="024fc-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="024fc-125">Conserver une copie de ces propriétés dans la mémoire permet aux utilisateurs de les récupérer à chaque régénération de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="024fc-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="024fc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="024fc-126">See also</span></span>

- [<span data-ttu-id="024fc-127">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="024fc-127">MAPI Tables</span></span>](mapi-tables.md)

