---
title: Conseils pour utiliser des tableaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439736"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="9d5e9-103">Conseils pour utiliser des tableaux</span><span class="sxs-lookup"><span data-stu-id="9d5e9-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="9d5e9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d5e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d5e9-105">Travailler avec une table MAPI est un peu semblable à travailler avec une table de base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="9d5e9-106">Un utilisateur peut limiter le nombre de lignes et de colonnes dans l'affichage et spécifier son ordre.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="9d5e9-107">Les lignes peuvent être récupérées une par une ou dans des groupes.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="9d5e9-108">Un curseur qui effectue le suivi de la position actuelle peut être déplacé vers un emplacement spécifique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="9d5e9-109">Pour travailler avec des tables, les clients utilisent l'interface en lecture seule, [IMAPITable: IUnknown](imapitableiunknown.md), tandis que les fournisseurs de services, selon qu'ils possèdent ou non les données sur lesquelles la table est basée, peuvent utiliser la fonction **IMAPITable** ou [ITableData: IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9d5e9-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="9d5e9-110">Les opérations définies dans ces interfaces peuvent être catégorisées comme des opérations que tous les utilisateurs de tables effectuent ou peuvent appeler et des opérations qui ne sont pas aussi largement utilisées car elles sont plus avancées.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="9d5e9-111">Certaines des opérations avancées sont plus complexes à mettre en œuvre; d'autres ne sont pas plus complexes, mais présentent un intérêt pour une petite minorité de composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="9d5e9-112">Les opérations les plus courantes sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="9d5e9-112">The more common operations are:</span></span>
  
- <span data-ttu-id="9d5e9-113">Les opérations sur les colonnes, qui affectent des colonnes uniques.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="9d5e9-114">Il s'agit notamment de spécifier les propriétés à inclure dans le jeu de colonnes et l'ordre dans lequel elles doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="9d5e9-115">Les opérations de ligne, qui affectent des lignes uniques.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="9d5e9-116">Il s'agit notamment des opérations de récupération des données et de maintenance: ajout, suppression et modification d'une ou de plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="9d5e9-117">Les opérations globales, qui affectent l'intégralité du tableau.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="9d5e9-118">Cela inclut la notification d'événement, la recherche et le tri.</span><span class="sxs-lookup"><span data-stu-id="9d5e9-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d5e9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d5e9-119">See also</span></span>



[<span data-ttu-id="9d5e9-120">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="9d5e9-120">MAPI Tables</span></span>](mapi-tables.md)

