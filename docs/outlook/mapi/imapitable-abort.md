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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406149"
---
# <a name="imapitableabort"></a><span data-ttu-id="3722c-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="3722c-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="3722c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3722c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3722c-105">Arrête toutes les opérations asynchrones en cours pour la table.</span><span class="sxs-lookup"><span data-stu-id="3722c-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="3722c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3722c-106">Parameters</span></span>

<span data-ttu-id="3722c-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="3722c-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3722c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3722c-108">Return value</span></span>

<span data-ttu-id="3722c-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3722c-109">S_OK</span></span> 
  
> <span data-ttu-id="3722c-110">Une ou plusieurs opérations asynchrones ont été arrêtées.</span><span class="sxs-lookup"><span data-stu-id="3722c-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="3722c-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="3722c-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="3722c-112">Une opération asynchrone est en cours et ne peut pas être arrêtée ou elle est déjà terminée.</span><span class="sxs-lookup"><span data-stu-id="3722c-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3722c-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3722c-113">Remarks</span></span>

<span data-ttu-id="3722c-114">La **méthode IMAPITable::Abort** arrête toute opération asynchrone en cours.</span><span class="sxs-lookup"><span data-stu-id="3722c-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3722c-115">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3722c-115">Notes to callers</span></span>

<span data-ttu-id="3722c-116">Pour savoir si une opération asynchrone est en cours, appelez la méthode [IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="3722c-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="3722c-117">Si **Abort** interrompt le traitement d’un appel à la méthode [IMAPITable::Restrict,](imapitable-restrict.md) l’état de la table sera tel qu’il était au moment du traitement de l’appel d’abandon. </span><span class="sxs-lookup"><span data-stu-id="3722c-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="3722c-118">Si **Abort** interrompt le traitement d’un appel à la méthode [IMAPITable::SortTable,](imapitable-sorttable.md) l’ordre de tri de la table n’est pas affecté et reste tel qu’il était avant l’appel **sortTable.**</span><span class="sxs-lookup"><span data-stu-id="3722c-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3722c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3722c-119">See also</span></span>



[<span data-ttu-id="3722c-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="3722c-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="3722c-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3722c-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="3722c-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3722c-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="3722c-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3722c-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

