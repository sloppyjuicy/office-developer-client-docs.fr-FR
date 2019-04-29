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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407059"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="b109e-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b109e-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="b109e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b109e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b109e-105">Interrompt le traitement jusqu'à ce qu'une ou plusieurs opérations asynchrones en cours sur la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="b109e-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="b109e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b109e-106">Parameters</span></span>

 <span data-ttu-id="b109e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b109e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b109e-108">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b109e-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b109e-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="b109e-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="b109e-110">dans Nombre maximal de millisecondes d'attente de l'opération asynchrone ou des opérations à effectuer.</span><span class="sxs-lookup"><span data-stu-id="b109e-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="b109e-111">Pour attendre indéfiniment jusqu'à la fin de l'opération, définissez _ulTimeout_ sur 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b109e-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="b109e-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="b109e-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="b109e-113">[in, out] À l'entrée, soit un pointeur valide, soit NULL.</span><span class="sxs-lookup"><span data-stu-id="b109e-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="b109e-114">Lors de la sortie, si _lpulTableStatus_ est un pointeur valide, il pointe vers l'état le plus récent de la table.</span><span class="sxs-lookup"><span data-stu-id="b109e-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="b109e-115">Si _lpulTableStatus_ a la valeur null, aucune information d'État n'est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="b109e-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="b109e-116">Si **WaitForCompletion** renvoie une valeur HRESULT qui ne réussit pas, le contenu de _lpulTableStatus_ n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b109e-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b109e-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b109e-117">Return value</span></span>

<span data-ttu-id="b109e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b109e-118">S_OK</span></span> 
  
> <span data-ttu-id="b109e-119">L'opération d'attente a réussi.</span><span class="sxs-lookup"><span data-stu-id="b109e-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="b109e-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b109e-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b109e-121">Le tableau ne prend pas en charge l'exécution des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="b109e-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="b109e-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b109e-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="b109e-123">L'opération asynchrone ou les opérations ne se sont pas terminées dans le temps imparti.</span><span class="sxs-lookup"><span data-stu-id="b109e-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b109e-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="b109e-124">Remarks</span></span>

<span data-ttu-id="b109e-125">La méthode **IMAPITable:: WaitForCompletion** interrompt le traitement jusqu'à ce que toutes les opérations asynchrones actuellement en cours pour la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="b109e-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="b109e-126">**WaitForCompletion** permet aux opérations asynchrones d'effectuer entièrement ou d'exécuter un certain nombre de millisecondes, comme indiqué par _ulTimeout_, avant d'être interrompue.</span><span class="sxs-lookup"><span data-stu-id="b109e-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="b109e-127">Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable:: GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b109e-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b109e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b109e-128">See also</span></span>



[<span data-ttu-id="b109e-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="b109e-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="b109e-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="b109e-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="b109e-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b109e-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="b109e-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b109e-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="b109e-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b109e-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="b109e-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b109e-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

