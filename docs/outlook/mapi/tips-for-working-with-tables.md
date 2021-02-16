---
title: Conseils pour travailler avec des tableaux
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
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="b1418-103">Conseils pour travailler avec des tableaux</span><span class="sxs-lookup"><span data-stu-id="b1418-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="b1418-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1418-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1418-105">Travailler avec une table MAPI est un peu comme une table de base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="b1418-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="b1418-106">Un utilisateur peut limiter le nombre de lignes et de colonnes dans l’affichage et spécifier son ordre.</span><span class="sxs-lookup"><span data-stu-id="b1418-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="b1418-107">Les lignes peuvent être récupérées une par une ou par groupes.</span><span class="sxs-lookup"><span data-stu-id="b1418-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="b1418-108">Un curseur qui assure le suivi de la position actuelle peut être déplacé vers un endroit spécifique du tableau.</span><span class="sxs-lookup"><span data-stu-id="b1418-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="b1418-109">Pour travailler avec des tables, les clients utilisent l’interface en lecture [seule, IMAPITable : IUnknown](imapitableiunknown.md), tandis que les fournisseurs de services, selon qu’ils possèdent ou non les données sur la table, peuvent utiliser **IMAPITable** ou [ITableData : IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b1418-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="b1418-110">Les opérations définies dans ces interfaces peuvent être classées en tant qu’opérations que tous les utilisateurs de tables font ou peuvent appeler et les opérations qui ne sont pas aussi largement utilisées, car elles sont plus avancées.</span><span class="sxs-lookup"><span data-stu-id="b1418-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="b1418-111">Certaines opérations avancées sont plus complexes à implémenter . d’autres ne sont pas plus complexes, mais sont d’un intérêt pour une petite majorité de composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1418-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="b1418-112">Les opérations les plus courantes sont :</span><span class="sxs-lookup"><span data-stu-id="b1418-112">The more common operations are:</span></span>
  
- <span data-ttu-id="b1418-113">Opérations de colonne, qui affectent des colonnes individuelles.</span><span class="sxs-lookup"><span data-stu-id="b1418-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="b1418-114">Il s’agit notamment de spécifier les propriétés à inclure dans le jeu de colonnes et l’ordre dans lequel elles doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="b1418-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="b1418-115">Opérations de ligne, qui affectent des lignes individuelles.</span><span class="sxs-lookup"><span data-stu-id="b1418-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="b1418-116">Il s’agit notamment de la récupération des données et des opérations de maintenance : ajout, suppression et modification d’une ou plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="b1418-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="b1418-117">Opérations globales, qui affectent la table entière.</span><span class="sxs-lookup"><span data-stu-id="b1418-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="b1418-118">Il s’agit notamment de la notification d’événement, de la recherche et du tri.</span><span class="sxs-lookup"><span data-stu-id="b1418-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1418-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1418-119">See also</span></span>



[<span data-ttu-id="b1418-120">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="b1418-120">MAPI Tables</span></span>](mapi-tables.md)

