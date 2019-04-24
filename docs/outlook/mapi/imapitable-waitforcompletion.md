---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328811"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="85c49-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="85c49-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="85c49-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85c49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85c49-105">Interrompt le traitement jusqu'à ce qu'une ou plusieurs opérations asynchrones en cours sur la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="85c49-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="85c49-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85c49-106">Parameters</span></span>

 <span data-ttu-id="85c49-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85c49-107">_ulFlags_</span></span>
  
> <span data-ttu-id="85c49-108">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="85c49-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="85c49-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="85c49-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="85c49-110">dans Nombre maximal de millisecondes d'attente de l'opération asynchrone ou des opérations à effectuer.</span><span class="sxs-lookup"><span data-stu-id="85c49-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="85c49-111">Pour attendre indéfiniment jusqu'à la fin de l'opération, définissez _ulTimeout_ sur 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="85c49-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="85c49-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="85c49-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="85c49-113">[in, out] À l'entrée, soit un pointeur valide, soit NULL.</span><span class="sxs-lookup"><span data-stu-id="85c49-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="85c49-114">Lors de la sortie, si _lpulTableStatus_ est un pointeur valide, il pointe vers l'état le plus récent de la table.</span><span class="sxs-lookup"><span data-stu-id="85c49-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="85c49-115">Si _lpulTableStatus_ a la valeur null, aucune information d'État n'est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="85c49-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="85c49-116">Si **WaitForCompletion** renvoie une valeur HRESULT qui ne réussit pas, le contenu de _lpulTableStatus_ n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="85c49-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85c49-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85c49-117">Return value</span></span>

<span data-ttu-id="85c49-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="85c49-118">S_OK</span></span> 
  
> <span data-ttu-id="85c49-119">L'opération d'attente a réussi.</span><span class="sxs-lookup"><span data-stu-id="85c49-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="85c49-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="85c49-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="85c49-121">Le tableau ne prend pas en charge l'exécution des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="85c49-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="85c49-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="85c49-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="85c49-123">L'opération asynchrone ou les opérations ne se sont pas terminées dans le temps imparti.</span><span class="sxs-lookup"><span data-stu-id="85c49-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85c49-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="85c49-124">Remarks</span></span>

<span data-ttu-id="85c49-125">La méthode **IMAPITable:: WaitForCompletion** interrompt le traitement jusqu'à ce que toutes les opérations asynchrones actuellement en cours pour la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="85c49-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="85c49-126">**WaitForCompletion** permet aux opérations asynchrones d'effectuer entièrement ou d'exécuter un certain nombre de millisecondes, comme indiqué par _ulTimeout_, avant d'être interrompue.</span><span class="sxs-lookup"><span data-stu-id="85c49-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="85c49-127">Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable:: GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="85c49-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85c49-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85c49-128">See also</span></span>



[<span data-ttu-id="85c49-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="85c49-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="85c49-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="85c49-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="85c49-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="85c49-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="85c49-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="85c49-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="85c49-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="85c49-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="85c49-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85c49-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

