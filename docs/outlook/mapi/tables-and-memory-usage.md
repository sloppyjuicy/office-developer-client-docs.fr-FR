---
title: Tables et utilisation de la mémoire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787341"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="97958-103">Tables et utilisation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="97958-103">Tables and memory usage</span></span>

<span data-ttu-id="97958-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97958-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97958-105">Un aspect important connecté à extraire des données d’une table est de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="97958-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="97958-106">Manque de mémoire disponible peut entraîner [IMAPITable::QueryRows](imapitable-queryrows.md) et [HrQueryAllRows](hrqueryallrows.md) échec, retournez moins le nombre de lignes souhaité.</span><span class="sxs-lookup"><span data-stu-id="97958-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="97958-107">Détermination de la méthode ou la fonction à utiliser pour récupérer des données de la table dépend de si la table peut être prévue pour tenir dans la mémoire et, si elle n’est pas le cas, si l’échec est acceptable.</span><span class="sxs-lookup"><span data-stu-id="97958-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="97958-108">Car il n’est pas toujours facile à déterminer la quantité de données adapté en mémoire en même temps, MAPI fournit des instructions de base pour une application cliente ou le fournisseur de services à suivre.</span><span class="sxs-lookup"><span data-stu-id="97958-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="97958-109">N’oubliez pas qu’il n’y a toujours exceptions, en fonction de l’implémentation de la table particulière et comment les données sous-jacentes sont stockées.</span><span class="sxs-lookup"><span data-stu-id="97958-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="97958-110">Les instructions suivantes peuvent servir à évaluer l’utilisation de la mémoire table :</span><span class="sxs-lookup"><span data-stu-id="97958-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="97958-111">Les clients qui tolèrent occasionnellement travailler ensemble de la mémoire dans la plage mégaoctet et peuvent prendre qu’ils n’auront aucun problème de lecture d’un tableau entier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="97958-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="97958-112">Restrictions ont une incidence sur l’utilisation d’une table de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="97958-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="97958-113">Un tableau avec un nombre important de lignes, par exemple une table des matières, strictement limité peut s’attendre à tenir dans la mémoire mais pas les généralement une table de grande taille illimitée.</span><span class="sxs-lookup"><span data-stu-id="97958-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="97958-114">Plusieurs tables appartenant à MAPI, tel que le statut, profils, service de message, fournisseur et tables de banque de messages, généralement contenir en mémoire.</span><span class="sxs-lookup"><span data-stu-id="97958-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="97958-115">Il s’agit généralement de petites tables.</span><span class="sxs-lookup"><span data-stu-id="97958-115">These are generally small tables.</span></span> <span data-ttu-id="97958-116">Toutefois, il existe certaines exceptions.</span><span class="sxs-lookup"><span data-stu-id="97958-116">However, there are exceptions.</span></span> <span data-ttu-id="97958-117">Par exemple, un fournisseur de profil sur le serveur peut générer une plus grande table profil qui ne sera pas en mesure d’adapter.</span><span class="sxs-lookup"><span data-stu-id="97958-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="97958-118">Pour récupérer toutes les lignes d’un tableau qui s’intègre à mémoire sans problème, appelez [HrQueryAllRows](hrqueryallrows.md), définissant le nombre maximal de lignes à zéro.</span><span class="sxs-lookup"><span data-stu-id="97958-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="97958-119">Pour récupérer toutes les lignes d’un tableau qui peut ou ne peut pas tenir dans la mémoire, génère une erreur, appelez **HrQueryAllRows** spécifiant un nombre maximal de lignes.</span><span class="sxs-lookup"><span data-stu-id="97958-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="97958-120">Le nombre maximal de lignes doit être défini à un nombre supérieur au nombre minimal de lignes qui sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="97958-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="97958-121">Si un client doit accéder au moins 50 lignes à partir d’une table de 300 lignes, le nombre maximal de lignes doit être défini au moins 51.</span><span class="sxs-lookup"><span data-stu-id="97958-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="97958-122">Pour récupérer toutes les lignes d’un tableau qui n’est pas prévu pour tenir dans la mémoire, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) dans une boucle avec un nombre de lignes relativement faible, comme l’illustre l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="97958-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="97958-123">Lorsque cette boucle se termine et toutes les lignes de la table ont été traitées et _cRows_ est égale à zéro, la position du curseur sera généralement en bas de la table.</span><span class="sxs-lookup"><span data-stu-id="97958-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97958-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97958-124">See also</span></span>

- [<span data-ttu-id="97958-125">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="97958-125">MAPI Tables</span></span>](mapi-tables.md)

