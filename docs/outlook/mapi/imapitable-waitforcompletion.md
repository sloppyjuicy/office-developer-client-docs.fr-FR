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
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="e14aa-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e14aa-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="e14aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e14aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e14aa-105">Suspend le traitement jusqu’à ce qu’une ou plusieurs opérations asynchrones en cours sur la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="e14aa-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="e14aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e14aa-106">Parameters</span></span>

 <span data-ttu-id="e14aa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e14aa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e14aa-108">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e14aa-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e14aa-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="e14aa-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="e14aa-110">[in] Nombre maximal de millisecondes à attendre pour que l’opération ou les opérations asynchrones se terminent.</span><span class="sxs-lookup"><span data-stu-id="e14aa-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="e14aa-111">Pour attendre indéfiniment que l’achèvement se produise, définissez  _ulTimeout_ sur 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="e14aa-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="e14aa-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="e14aa-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="e14aa-113">[in, out] Lors de l’entrée, pointeur valide ou NULL.</span><span class="sxs-lookup"><span data-stu-id="e14aa-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="e14aa-114">En sortie, si  _lpulTableStatus_ est un pointeur valide, il pointe vers l’état le plus récent du tableau.</span><span class="sxs-lookup"><span data-stu-id="e14aa-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="e14aa-115">Si  _lpulTableStatus a_ la valeur NULL, aucune information d’état n’est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e14aa-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="e14aa-116">Si **WaitForCompletion** renvoie une valeur HRESULT infructueuse, le contenu de  _lpulTableStatus_ n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e14aa-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e14aa-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e14aa-117">Return value</span></span>

<span data-ttu-id="e14aa-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e14aa-118">S_OK</span></span> 
  
> <span data-ttu-id="e14aa-119">L’opération d’attente a réussi.</span><span class="sxs-lookup"><span data-stu-id="e14aa-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="e14aa-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e14aa-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e14aa-121">Le tableau ne prend pas en charge l’attente de la fin des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="e14aa-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="e14aa-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e14aa-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="e14aa-123">L’opération asynchrone ou les opérations ne se sont pas terminées dans l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e14aa-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e14aa-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e14aa-124">Remarks</span></span>

<span data-ttu-id="e14aa-125">La **méthode IMAPITable::WaitForCompletion** suspend le traitement jusqu’à ce que toutes les opérations asynchrones en cours pour la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="e14aa-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="e14aa-126">**WaitForCompletion** peut permettre aux opérations asynchrones soit de se terminer entièrement, soit de s’exécuter pendant un certain nombre de millisecondes, comme indiqué par  _ulTimeout_, avant d’être interrompues.</span><span class="sxs-lookup"><span data-stu-id="e14aa-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="e14aa-127">Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="e14aa-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e14aa-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e14aa-128">See also</span></span>



[<span data-ttu-id="e14aa-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="e14aa-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="e14aa-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="e14aa-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="e14aa-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="e14aa-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="e14aa-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e14aa-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="e14aa-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e14aa-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e14aa-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e14aa-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

