---
title: Conseils pour l’utilisation des tableaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787345"
---
# <a name="tips-for-working-with-tables"></a><span data-ttu-id="193bd-103">Conseils pour l’utilisation des tableaux</span><span class="sxs-lookup"><span data-stu-id="193bd-103">Tips for Working with Tables</span></span>

  
  
<span data-ttu-id="193bd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="193bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="193bd-105">Utilisation d’une MAPI table est un peu comparable à l’utilisation d’une table de base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="193bd-105">Working with a MAPI table is a little like working with a relational database table.</span></span> <span data-ttu-id="193bd-106">Un utilisateur peut limiter le nombre de lignes et colonnes de la vue et spécifier leur ordre.</span><span class="sxs-lookup"><span data-stu-id="193bd-106">A user can limit the number of rows and columns in the view and specify their order.</span></span> <span data-ttu-id="193bd-107">Lignes peuvent être extraites d’un à la fois ou en groupes.</span><span class="sxs-lookup"><span data-stu-id="193bd-107">Rows can be retrieved one at a time or in groups.</span></span> <span data-ttu-id="193bd-108">Un curseur qui effectue le suivi de la position actuelle peut être déplacé vers un emplacement spécifique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="193bd-108">A cursor that keeps track of the current position can be moved to a specific place in the table.</span></span> 
  
<span data-ttu-id="193bd-109">Pour travailler avec des tableaux, les clients utilisent l’interface en lecture seule, [IMAPITable : IUnknown](imapitableiunknown.md), tandis que les fournisseurs de service, selon qu’ils possèdent les données selon la table, peuvent utiliser soit **IMAPITable** ou [ITableData : IUnknown](itabledataiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="193bd-109">To work with tables, clients use the read-only interface, [IMAPITable : IUnknown](imapitableiunknown.md), whereas service providers, depending on whether they own the data that the table is based on, can use either **IMAPITable** or [ITableData : IUnknown](itabledataiunknown.md).</span></span> <span data-ttu-id="193bd-110">Les opérations définies dans ces interfaces peuvent être classées en tant qu’opérations que tous les utilisateurs de tableaux ou peuvent appeler et qui ne sont pas aussi largement utilisés, car ils sont plus avancés.</span><span class="sxs-lookup"><span data-stu-id="193bd-110">The operations defined in these interfaces can be categorized as operations that all users of tables either do or can invoke and operations that are not as widely used because they are more advanced.</span></span> <span data-ttu-id="193bd-111">Certaines opérations avancées sont plus complexes à implémenter ; d’autres personnes sont ne plus complexes, mais destinées aux petites rarement composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="193bd-111">Some of the advanced operations are more complex to implement; others are no more complex, but are of interest to a small minority of MAPI components.</span></span> 
  
<span data-ttu-id="193bd-112">Opérations les plus courantes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="193bd-112">The more common operations are:</span></span>
  
- <span data-ttu-id="193bd-113">Opérations de colonne, qui affectent les colonnes uniques.</span><span class="sxs-lookup"><span data-stu-id="193bd-113">Column operations, which affect single columns.</span></span> <span data-ttu-id="193bd-114">Cela inclut la spécification des propriétés à inclure dans l’ensemble de colonnes et l’ordre dans lequel ils doivent être inclus.</span><span class="sxs-lookup"><span data-stu-id="193bd-114">These include specifying the properties to be included in the column set and the order in which they should be included.</span></span>
    
- <span data-ttu-id="193bd-115">Opérations de ligne, qui concerne les lignes uniques.</span><span class="sxs-lookup"><span data-stu-id="193bd-115">Row operations, which affect single rows.</span></span> <span data-ttu-id="193bd-116">Cela inclut les opérations de maintenance et de récupération des données : ajout, suppression et la modification d’une seule ligne ou plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="193bd-116">These include data retrieval and the maintenance operations: adding, deleting, and modifying a single row or rows.</span></span>
    
- <span data-ttu-id="193bd-117">Opérations globales, qui affectent l’intégralité du tableau.</span><span class="sxs-lookup"><span data-stu-id="193bd-117">Global operations, which affect the entire table.</span></span> <span data-ttu-id="193bd-118">Cela inclut la notification d’événement, recherche et le tri.</span><span class="sxs-lookup"><span data-stu-id="193bd-118">These include event notification, searching and sorting.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="193bd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="193bd-119">See also</span></span>



[<span data-ttu-id="193bd-120">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="193bd-120">MAPI Tables</span></span>](mapi-tables.md)

