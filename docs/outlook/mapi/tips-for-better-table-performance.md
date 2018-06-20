---
title: Conseils pour améliorer les performances de table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2b14c4fe8cbbadb2ccdd6a2f7870a07d2f96a3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787353"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="957a8-103">Conseils pour améliorer les performances de table</span><span class="sxs-lookup"><span data-stu-id="957a8-103">Tips for better table performance</span></span>
  
<span data-ttu-id="957a8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="957a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="957a8-105">Étant donné que de nombreuses opérations de table peuvent prendre du temps et il n’existe aucun moyen d’indiquer la progression, il est utile d’utiliser les techniques suivantes pour améliorer les performances :</span><span class="sxs-lookup"><span data-stu-id="957a8-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="957a8-106">**Rendre [IMAPITable : IUnknown](imapitableiunknown.md) appelle dans l’ordre correct**</span><span class="sxs-lookup"><span data-stu-id="957a8-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="957a8-107">Clients et fournisseurs de services peuvent travailler avec des tableaux de diverses façons.</span><span class="sxs-lookup"><span data-stu-id="957a8-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="957a8-108">Ils peuvent ouvrir la table et récupérer les données pour toutes les lignes à l’aide de l’ensemble de colonnes par défaut et l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="957a8-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="957a8-109">Ils peuvent également modifier cet affichage par défaut de la table en modifiant l’ensemble de colonnes, modification de l’ordre de tri ou en établissant une restriction pour limiter l’étendue de la table.</span><span class="sxs-lookup"><span data-stu-id="957a8-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="957a8-110">Les utilisateurs de tableau que vous souhaitez effectuer une ou plusieurs de ces opérations avant de récupérer des données doivent effectuer les dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="957a8-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="957a8-111">Définir une colonne avec [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="957a8-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="957a8-112">Établir une restriction avec [IMAPITable](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="957a8-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="957a8-113">Définir un ordre de tri avec [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="957a8-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="957a8-114">Exécution de ces tâches dans l’ordre suivant limite le nombre de lignes et de colonnes qui seront triées, ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="957a8-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="957a8-115">**Délai d’une opération à l’aide de l’indicateur TBL_BATCH si possible**</span><span class="sxs-lookup"><span data-stu-id="957a8-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="957a8-116">Définition de la table\_indicateur de lot sur une méthode permet à l’implémentation de tableau collecter plusieurs appels avant de traiter sur n’importe lequel d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="957a8-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="957a8-117">Au lieu de passer des appels nombreux à un serveur distant. une implémentation de table, permettent d’effectuer toutes les opérations en même temps.</span><span class="sxs-lookup"><span data-stu-id="957a8-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="957a8-118">Les résultats des opérations ne sont pas évaluées jusqu'à ce qu’ils ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="957a8-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="957a8-119">Par exemple, lorsqu’un client appelle [IMAPITable](imapitable-restrict.md) pour spécifier une restriction avec la TBL\_lot indicateur défini, la restriction n’avez pas à entrent en vigueur jusqu'à ce que le client appelle [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="957a8-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="957a8-120">Ainsi, l’implémentation de table combiner le travail de deux appels en une seule.</span><span class="sxs-lookup"><span data-stu-id="957a8-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="957a8-121">Les utilisateurs qui tirent parti de la table de table\_indicateur lot Sachez que gestion dans ces conditions d’erreur peut être plus complexe.</span><span class="sxs-lookup"><span data-stu-id="957a8-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="957a8-122">Étant donné que la gestion des erreurs à partir d’une opération différée sont similaire à la gestion des erreurs lors de l’interface MAPI\_DEFERRED_ERRORS est défini, voir [Report des erreurs MAPI](deferring-mapi-errors.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="957a8-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="957a8-123">**Conserver un cache des propriétés couramment utilisées**</span><span class="sxs-lookup"><span data-stu-id="957a8-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="957a8-124">Fournisseurs de services de mise en œuvre de tables peuvent réduire le temps que nécessaire pour créer un affichage en mettant en cache les copies des propriétés de l’objet couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="957a8-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="957a8-125">Conserver une copie de ces propriétés en mémoire enregistre avoir à récupérer à partir de l’objet chaque fois que l’affichage doit être reconstruite.</span><span class="sxs-lookup"><span data-stu-id="957a8-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="957a8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="957a8-126">See also</span></span>

- [<span data-ttu-id="957a8-127">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="957a8-127">MAPI Tables</span></span>](mapi-tables.md)

