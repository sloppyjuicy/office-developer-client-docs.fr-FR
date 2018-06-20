---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784066"
---
# <a name="imapitableabort"></a><span data-ttu-id="65bcf-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="65bcf-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="65bcf-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65bcf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65bcf-105">Arrête toutes les opérations asynchrones en cours pour la table.</span><span class="sxs-lookup"><span data-stu-id="65bcf-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="65bcf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65bcf-106">Parameters</span></span>

<span data-ttu-id="65bcf-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="65bcf-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="65bcf-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="65bcf-108">Return value</span></span>

<span data-ttu-id="65bcf-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="65bcf-109">S_OK</span></span> 
  
> <span data-ttu-id="65bcf-110">Un ou plusieurs des opérations asynchrones ont été arrêtées.</span><span class="sxs-lookup"><span data-stu-id="65bcf-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="65bcf-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="65bcf-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="65bcf-112">Une opération asynchrone est en cours et ne peut pas être arrêtée ou il a déjà effectué.</span><span class="sxs-lookup"><span data-stu-id="65bcf-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65bcf-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="65bcf-113">Remarks</span></span>

<span data-ttu-id="65bcf-114">La méthode **IMAPITable::Abort** arrête toute opération asynchrone est en cours.</span><span class="sxs-lookup"><span data-stu-id="65bcf-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="65bcf-115">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="65bcf-115">Notes to callers</span></span>

<span data-ttu-id="65bcf-116">Pour savoir si une opération asynchrone est en cours, appelez la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="65bcf-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="65bcf-117">Si **l’abandon** interrompt le traitement d’un appel à la méthode [IMAPITable](imapitable-restrict.md) , l’état de la table sera telle qu’elle était au moment de que l’appel **abandonner** est traité.</span><span class="sxs-lookup"><span data-stu-id="65bcf-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="65bcf-118">Si **abandonner** interrompt le traitement d’un appel à la méthode [IMAPITable::SortTable](imapitable-sorttable.md) , ordre de tri de la table n’est pas affecté et reste tel qu’il était avant l’appel de **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="65bcf-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65bcf-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65bcf-119">See also</span></span>



[<span data-ttu-id="65bcf-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="65bcf-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="65bcf-121">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="65bcf-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="65bcf-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="65bcf-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="65bcf-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65bcf-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

