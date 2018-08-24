---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0eb0374788da629c4c28eff2fce93536cf65a4ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582986"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="1cd86-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="1cd86-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="1cd86-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cd86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cd86-105">Crée un affichage tableau, qui retourne un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="1cd86-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="1cd86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cd86-106">Parameters</span></span>

 <span data-ttu-id="1cd86-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="1cd86-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="1cd86-108">[in] Pointeur vers une structure d’ordre de tri qui décrit l’ordre de tri pour l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="1cd86-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="1cd86-109">Si NULL est indiqué dans le paramètre _lpSSortOrderSet_ , l’affichage n’est pas trié.</span><span class="sxs-lookup"><span data-stu-id="1cd86-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="1cd86-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="1cd86-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="1cd86-111">[in] Pointeur vers une fonction de rappel selon le prototype [CALLERRELEASE](callerrelease.md) que les appels MAPI lorsqu’il le libère l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1cd86-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="1cd86-112">Si NULL est indiqué dans le paramètre _lpfCallerRelease_ , aucune fonction n’est appelée sur la version de la vue.</span><span class="sxs-lookup"><span data-stu-id="1cd86-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="1cd86-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1cd86-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="1cd86-114">[in] Les données qui doivent être enregistrées avec la nouvelle vue et transmises à la fonction de rappel désignée par _lpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="1cd86-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="1cd86-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="1cd86-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="1cd86-116">[out] Pointeur vers un pointeur vers la vue nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="1cd86-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cd86-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1cd86-117">Return value</span></span>

<span data-ttu-id="1cd86-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cd86-118">S_OK</span></span> 
  
> <span data-ttu-id="1cd86-119">L’affichage a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="1cd86-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cd86-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="1cd86-120">Remarks</span></span>

<span data-ttu-id="1cd86-121">La méthode **ITableData::HrGetView** crée un affichage en lecture seule des données dans le tableau, trié dans l’ordre indiqué par le paramètre _lpSSortOrderSet_ .</span><span class="sxs-lookup"><span data-stu-id="1cd86-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="1cd86-122">Le curseur est placé au début de la première ligne dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1cd86-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="1cd86-123">Une implémentation d’interface **IMAPITable** pour accéder à la vue est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1cd86-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="1cd86-124">Fournisseurs de services d’appel **HrGetView** lorsqu’ils souhaitent accorder un accès au client à un tableau.</span><span class="sxs-lookup"><span data-stu-id="1cd86-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="1cd86-125">**HrGetView** crée l’affichage et retourne le pointeur **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="1cd86-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="1cd86-126">Fournisseurs de services de passer à son tour le pointeur sur le client.</span><span class="sxs-lookup"><span data-stu-id="1cd86-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="1cd86-127">Lorsque le client a terminé à l’aide de la table et appelle la méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** appelle la fonction de rappel vers laquelle pointée le paramètre _lpfCallerRelease_ .</span><span class="sxs-lookup"><span data-stu-id="1cd86-127">When the client is finished using the table and calls its [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="1cd86-128">Si un fournisseur de services doit renvoyer à un client une vue possédant une colonne personnalisée définie ou une restriction, le fournisseur peut appeler les méthodes la vue [IMAPITable::SetColumns](imapitable-setcolumns.md) et [IMAPITable](imapitable-restrict.md) avant d’autoriser l’accès au client.</span><span class="sxs-lookup"><span data-stu-id="1cd86-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1cd86-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cd86-129">See also</span></span>



[<span data-ttu-id="1cd86-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="1cd86-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="1cd86-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cd86-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="1cd86-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="1cd86-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="1cd86-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cd86-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

