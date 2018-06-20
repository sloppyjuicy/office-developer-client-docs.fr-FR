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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c7859e033924786e415f9faa9f75021ea47968c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784100"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="209a0-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="209a0-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="209a0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="209a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="209a0-105">Interrompt le traitement jusqu'à ce qu’un ou plusieurs asynchrones opérations en cours sur la table est terminé.</span><span class="sxs-lookup"><span data-stu-id="209a0-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="209a0-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="209a0-106">Parameters</span></span>

 <span data-ttu-id="209a0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="209a0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="209a0-108">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="209a0-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="209a0-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="209a0-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="209a0-110">[in] Nombre maximal de millisecondes d’attente pour l’opération asynchrone ou les opérations à effectuer.</span><span class="sxs-lookup"><span data-stu-id="209a0-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="209a0-111">Pour attendre indéfiniment jusqu'à ce que l’exécution se produit, définissez _ulTimeout_ sur 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="209a0-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="209a0-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="209a0-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="209a0-113">[entrée, sortie] À l’entrée, un pointeur valide ou valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="209a0-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="209a0-114">Dans la sortie, si _lpulTableStatus_ est un pointeur valid, il pointe vers le dernier état de la table.</span><span class="sxs-lookup"><span data-stu-id="209a0-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="209a0-115">Si _lpulTableStatus_ est NULL, aucune information d’état n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="209a0-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="209a0-116">Si **WaitForCompletion** renvoie une valeur HRESULT échoue, le contenu de _lpulTableStatus_ n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="209a0-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="209a0-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="209a0-117">Return value</span></span>

<span data-ttu-id="209a0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="209a0-118">S_OK</span></span> 
  
> <span data-ttu-id="209a0-119">L’opération d’attente a réussi.</span><span class="sxs-lookup"><span data-stu-id="209a0-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="209a0-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="209a0-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="209a0-121">Le tableau ne gère pas en attente pour l’exécution d’opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="209a0-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="209a0-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="209a0-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="209a0-123">L’opération asynchrone ou les opérations ne s’est pas terminée dans le délai spécifié.</span><span class="sxs-lookup"><span data-stu-id="209a0-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="209a0-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="209a0-124">Remarks</span></span>

<span data-ttu-id="209a0-125">La méthode **IMAPITable::WaitForCompletion** interrompt le traitement jusqu'à ce qu’une opération asynchrone actuellement en cours de la table est terminé.</span><span class="sxs-lookup"><span data-stu-id="209a0-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="209a0-126">**WaitForCompletion** peut autoriser les opérations asynchrones à entièrement terminée ou pour exécuter un certain nombre de millisecondes, comme indiqué par _ulTimeout_, avant d’être interrompu.</span><span class="sxs-lookup"><span data-stu-id="209a0-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="209a0-127">Pour détecter les opérations asynchrones en cours, appelez la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="209a0-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="209a0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="209a0-128">See also</span></span>



[<span data-ttu-id="209a0-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="209a0-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="209a0-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="209a0-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="209a0-131">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="209a0-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="209a0-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="209a0-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="209a0-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="209a0-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="209a0-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="209a0-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

