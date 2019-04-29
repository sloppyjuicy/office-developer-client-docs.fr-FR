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
# <a name="tables-and-memory-usage"></a><span data-ttu-id="4dea2-103">Utilisation de la mémoire et des tables</span><span class="sxs-lookup"><span data-stu-id="4dea2-103">Tables and memory usage</span></span>

<span data-ttu-id="4dea2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dea2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dea2-105">Un problème important lié à la récupération des données d'une table est l'utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4dea2-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="4dea2-106">L'absence de mémoire disponible peut entraîner l'échec d'une erreur [IMAPITable:: QueryRows](imapitable-queryrows.md) et [HrQueryAllRows](hrqueryallrows.md) , ce qui renvoie moins de lignes que le nombre souhaité.</span><span class="sxs-lookup"><span data-stu-id="4dea2-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="4dea2-107">Le choix de la méthode ou de la fonction à utiliser pour récupérer les données de tableau dépend du fait que la table peut être ajustée en mémoire et, si elle ne l'est pas, si la défaillance est acceptable.</span><span class="sxs-lookup"><span data-stu-id="4dea2-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="4dea2-108">Étant donné qu'il n'est pas toujours facile de déterminer la quantité de données pouvant être insérées dans la mémoire, MAPI fournit quelques instructions de base pour qu'une application client ou un fournisseur de services soit suivi.</span><span class="sxs-lookup"><span data-stu-id="4dea2-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="4dea2-109">N'oubliez pas qu'il existe toujours des exceptions, en fonction de l'implémentation de table particulière et de la façon dont les données sous-jacentes sont stockées.</span><span class="sxs-lookup"><span data-stu-id="4dea2-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="4dea2-110">Les instructions suivantes peuvent être utilisées pour évaluer l'utilisation de la mémoire des tableaux:</span><span class="sxs-lookup"><span data-stu-id="4dea2-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="4dea2-111">Les clients qui peuvent tolérer une utilisation occasionnelle de la mémoire du jeu de travail dans la plage de mégaoctets et peuvent supposer qu'ils n'auront aucun problème à lire une table entière dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4dea2-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="4dea2-112">Les restrictions ont un impact sur l'utilisation de la mémoire d'une table.</span><span class="sxs-lookup"><span data-stu-id="4dea2-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="4dea2-113">Un tableau fortement restreint avec un nombre important de lignes, telles qu'une table des matières, peut être susceptible de s'adapter à la mémoire pendant qu'une table de grande taille non restreinte ne l'est généralement pas.</span><span class="sxs-lookup"><span data-stu-id="4dea2-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="4dea2-114">Plusieurs des tables appartenant à MAPI, telles que l'État, le profil, le service de messagerie, le fournisseur et les tables de banque de messages, sont généralement contenues dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4dea2-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="4dea2-115">Il s'agit généralement de petites tables.</span><span class="sxs-lookup"><span data-stu-id="4dea2-115">These are generally small tables.</span></span> <span data-ttu-id="4dea2-116">Toutefois, il existe des exceptions.</span><span class="sxs-lookup"><span data-stu-id="4dea2-116">However, there are exceptions.</span></span> <span data-ttu-id="4dea2-117">Par exemple, un fournisseur de profils serveur peut générer une table de profil plus grande qui ne pourra pas être ajustée.</span><span class="sxs-lookup"><span data-stu-id="4dea2-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="4dea2-118">Pour récupérer toutes les lignes d'une table qui tiendront dans la mémoire sans problème, appelez [HrQueryAllRows](hrqueryallrows.md), en définissant le nombre maximal de lignes sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4dea2-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="4dea2-119">Pour récupérer toutes les lignes d'une table qui peuvent être dans la mémoire ou non, générant une erreur, appelez **HrQueryAllRows** en spécifiant un nombre maximal de lignes.</span><span class="sxs-lookup"><span data-stu-id="4dea2-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="4dea2-120">Le nombre maximal de lignes doit être défini sur un nombre supérieur au nombre minimal de lignes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4dea2-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="4dea2-121">Si un client doit accéder au moins à 50 lignes à partir d'une table de 300 lignes, le nombre maximal de lignes doit être défini sur au moins 51.</span><span class="sxs-lookup"><span data-stu-id="4dea2-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="4dea2-122">Pour récupérer toutes les lignes d'une table qui ne sont pas censées tenir dans la mémoire, appelez la fonction [IMAPITable:: QueryRows](imapitable-queryrows.md) dans une boucle avec un nombre de lignes relativement faible, comme l'illustre l'exemple de code suivant:</span><span class="sxs-lookup"><span data-stu-id="4dea2-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="4dea2-123">Lorsque cette boucle est terminée et que toutes les lignes de la table ont été traitées __ et que l'argument Crows a la valeur zéro, la position du curseur se trouve généralement en bas du tableau.</span><span class="sxs-lookup"><span data-stu-id="4dea2-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dea2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dea2-124">See also</span></span>

- [<span data-ttu-id="4dea2-125">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="4dea2-125">MAPI Tables</span></span>](mapi-tables.md)

