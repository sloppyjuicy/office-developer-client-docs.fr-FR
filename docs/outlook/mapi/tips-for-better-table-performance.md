---
title: Conseils pour améliorer les performances d’une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412512"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="97cc2-103">Conseils pour améliorer les performances d’une table</span><span class="sxs-lookup"><span data-stu-id="97cc2-103">Tips for better table performance</span></span>
  
<span data-ttu-id="97cc2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97cc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97cc2-105">Étant donné que de nombreuses opérations de table peuvent prendre du temps et qu’il n’existe aucun moyen d’indiquer la progression, il est utile d’utiliser les techniques suivantes pour améliorer les performances :</span><span class="sxs-lookup"><span data-stu-id="97cc2-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="97cc2-106">**Effectuer [des appels IMAPITable : IUnknown](imapitableiunknown.md) dans l’ordre correct**</span><span class="sxs-lookup"><span data-stu-id="97cc2-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="97cc2-107">Les clients et les fournisseurs de services peuvent utiliser des tableaux de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="97cc2-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="97cc2-108">Ils peuvent ouvrir la table et récupérer les données de toutes les lignes à l’aide de l’ordre de tri et du jeu de colonnes par défaut.</span><span class="sxs-lookup"><span data-stu-id="97cc2-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="97cc2-109">Ils peuvent également modifier cet affichage par défaut du tableau en modifiant le jeu de colonnes, en modifiant l’ordre de tri ou en établissant une restriction pour affiner l’étendue du tableau.</span><span class="sxs-lookup"><span data-stu-id="97cc2-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="97cc2-110">Les utilisateurs de tableau qui ont l’intention d’effectuer une ou plusieurs de ces opérations avant de récupérer des données doivent les effectuer dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="97cc2-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="97cc2-111">Définissez un ensemble de colonnes [avec IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="97cc2-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="97cc2-112">Établir une restriction avec [IMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="97cc2-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="97cc2-113">Définissez un ordre de tri [avec IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="97cc2-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="97cc2-114">L’exécution de ces tâches dans cet ordre limite le nombre de lignes et de colonnes qui seront triées, améliorant ainsi les performances.</span><span class="sxs-lookup"><span data-stu-id="97cc2-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="97cc2-115">**Retarder une opération à l’aide de l’TBL_BATCH si possible**</span><span class="sxs-lookup"><span data-stu-id="97cc2-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="97cc2-116">La définition de l’indicateur BATCH TBL sur une méthode permet à l’implémenteur de table de collecter plusieurs appels avant d’agir \_ sur l’un d’eux.</span><span class="sxs-lookup"><span data-stu-id="97cc2-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="97cc2-117">Au lieu d’effectuer potentiellement de nombreux appels vers un serveur distant ; un implémenteur de table peut en effectuer une, en effectuer toutes les opérations en même temps.</span><span class="sxs-lookup"><span data-stu-id="97cc2-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="97cc2-118">Les résultats des opérations ne sont pas évalués tant qu’ils ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="97cc2-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="97cc2-119">Par exemple, lorsqu’un client appelle [IMAPITable::Restrict](imapitable-restrict.md) pour spécifier une restriction avec l’indicateur BATCH TBL, la restriction n’a pas besoin d’entrer en vigueur tant que le client n’appelle \_ [pas IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="97cc2-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="97cc2-120">Cela permet à l’implémenteur de table de combiner le travail de deux appels en un seul.</span><span class="sxs-lookup"><span data-stu-id="97cc2-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="97cc2-121">Les utilisateurs de tableau qui tirez parti de l’indicateur BATCH TBL doivent savoir que la gestion des erreurs dans ces \_ conditions peut être plus complexe.</span><span class="sxs-lookup"><span data-stu-id="97cc2-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="97cc2-122">Étant donné que la gestion des erreurs à partir d’une opération différée est similaire à la gestion des erreurs lorsque l’indicateur DEFERRED_ERRORS MAPI est définie, voir Différer les erreurs MAPI pour plus \_ d’informations. [](deferring-mapi-errors.md)</span><span class="sxs-lookup"><span data-stu-id="97cc2-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="97cc2-123">**Conserver un cache des propriétés couramment utilisées**</span><span class="sxs-lookup"><span data-stu-id="97cc2-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="97cc2-124">Les fournisseurs de services qui implémentent des tables peuvent réduire le temps qu’il faut pour créer un affichage en mettant en cache des copies des propriétés d’objet couramment utilisées.</span><span class="sxs-lookup"><span data-stu-id="97cc2-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="97cc2-125">Conserver une copie de ces propriétés en mémoire permet d’éviter de devoir les récupérer à partir de l’objet chaque fois que l’affichage doit être reconstruit.</span><span class="sxs-lookup"><span data-stu-id="97cc2-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97cc2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97cc2-126">See also</span></span>

- [<span data-ttu-id="97cc2-127">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="97cc2-127">MAPI Tables</span></span>](mapi-tables.md)

