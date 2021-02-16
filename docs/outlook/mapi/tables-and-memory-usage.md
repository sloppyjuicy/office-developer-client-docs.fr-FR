---
title: Utilisation de la mémoire et des tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436859"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="a6635-103">Utilisation de la mémoire et des tables</span><span class="sxs-lookup"><span data-stu-id="a6635-103">Tables and memory usage</span></span>

<span data-ttu-id="a6635-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6635-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6635-105">Un problème important lié à la récupération des données d’une table est l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a6635-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="a6635-106">Le manque de mémoire disponible peut entraîner l’échec [d’IMAPITable::QueryRows](imapitable-queryrows.md) et [HrQueryAllRows,](hrqueryallrows.md) en renvoyant moins de lignes que le nombre souhaité.</span><span class="sxs-lookup"><span data-stu-id="a6635-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="a6635-107">Le choix de la méthode ou de la fonction à utiliser pour récupérer les données d’un tableau varie selon que la table doit tenir dans la mémoire et, si elle ne l’est pas, si l’échec est acceptable.</span><span class="sxs-lookup"><span data-stu-id="a6635-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="a6635-108">Étant donné qu’il n’est pas toujours facile de déterminer la quantité de données qui s’intégrera dans la mémoire à la fois, MAPI fournit des instructions de base pour qu’une application cliente ou un fournisseur de services suive.</span><span class="sxs-lookup"><span data-stu-id="a6635-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="a6635-109">N’oubliez pas qu’il existe toujours des exceptions, en fonction de l’implémentation de la table particulière et de la façon dont les données sous-jacentes sont stockées.</span><span class="sxs-lookup"><span data-stu-id="a6635-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="a6635-110">Les instructions suivantes peuvent être utilisées pour évaluer l’utilisation de la mémoire des tableaux :</span><span class="sxs-lookup"><span data-stu-id="a6635-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="a6635-111">Les clients qui peuvent tolérer un travail occasionnel définissent l’utilisation de la mémoire dans la plage de mégaoctets et peuvent supposer qu’ils n’auront aucun problème à lire un tableau entier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a6635-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="a6635-112">Les restrictions ont une incidence sur l’utilisation de la mémoire par une table.</span><span class="sxs-lookup"><span data-stu-id="a6635-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="a6635-113">Une table très restreinte avec un grand nombre de lignes, telles qu’une table des matières, peut être attendue pour tenir dans la mémoire, alors qu’une grande table non restreinte ne le peut généralement pas.</span><span class="sxs-lookup"><span data-stu-id="a6635-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="a6635-114">Plusieurs tables de MAPI, telles que les tables d’état, de profil, de service de message, de fournisseur et de magasin de messages, sont généralement stockées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a6635-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="a6635-115">Il s’agit généralement de petites tables.</span><span class="sxs-lookup"><span data-stu-id="a6635-115">These are generally small tables.</span></span> <span data-ttu-id="a6635-116">Toutefois, il existe des exceptions.</span><span class="sxs-lookup"><span data-stu-id="a6635-116">However, there are exceptions.</span></span> <span data-ttu-id="a6635-117">Par exemple, un fournisseur de profils basé sur un serveur peut générer une table de profils plus grande qui ne pourra pas tenir.</span><span class="sxs-lookup"><span data-stu-id="a6635-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="a6635-118">Pour récupérer toutes les lignes d’un tableau qui s’intègrera dans la mémoire sans problème, appelez [HrQueryAllRows](hrqueryallrows.md), en fixant le nombre maximal de lignes sur zéro.</span><span class="sxs-lookup"><span data-stu-id="a6635-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="a6635-119">Pour récupérer toutes les lignes d’un tableau qui peuvent ou non tenir dans la mémoire, générant une erreur, appelez **HrQueryAllRows** en spécifiant un nombre maximal de lignes.</span><span class="sxs-lookup"><span data-stu-id="a6635-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="a6635-120">Le nombre maximal de lignes doit être supérieur au nombre minimal de lignes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a6635-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="a6635-121">Si un client doit accéder à au moins 50 lignes à partir d’un tableau de 300 lignes, le nombre maximal de lignes doit être d’au moins 51.</span><span class="sxs-lookup"><span data-stu-id="a6635-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="a6635-122">Pour récupérer toutes les lignes d’un tableau qui n’est pas censé tenir dans la mémoire, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) dans une boucle avec un nombre de lignes relativement faible, comme l’illustre l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="a6635-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

<span data-ttu-id="a6635-123">Lorsque cette boucle est terminée et que toutes les lignes du tableau ont été traitées et  _que cRows_ est zéro, la position du curseur est généralement en bas du tableau.</span><span class="sxs-lookup"><span data-stu-id="a6635-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6635-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6635-124">See also</span></span>

- [<span data-ttu-id="a6635-125">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="a6635-125">MAPI Tables</span></span>](mapi-tables.md)

