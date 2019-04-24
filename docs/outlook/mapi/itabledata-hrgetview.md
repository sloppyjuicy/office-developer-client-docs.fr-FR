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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278714"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="33100-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="33100-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="33100-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33100-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33100-105">Crée un affichage tableau en renvoyant un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="33100-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="33100-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33100-106">Parameters</span></span>

 <span data-ttu-id="33100-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="33100-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="33100-108">dans Pointeur vers une structure d'ordre de tri qui décrit l'ordre de tri de la vue de table.</span><span class="sxs-lookup"><span data-stu-id="33100-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="33100-109">Si NULL est transmis dans le paramètre _lpSSortOrderSet_ , la vue n'est pas triée.</span><span class="sxs-lookup"><span data-stu-id="33100-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="33100-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="33100-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="33100-111">dans Pointeur vers une fonction de rappel basée sur le prototype [CALLERRELEASE](callerrelease.md) que MAPI appelle lorsqu'il libère la vue.</span><span class="sxs-lookup"><span data-stu-id="33100-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="33100-112">Si NULL est passé dans le paramètre _lpfCallerRelease_ , aucune fonction n'est appelée sur la version de la vue.</span><span class="sxs-lookup"><span data-stu-id="33100-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="33100-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="33100-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="33100-114">dans Les données qui doivent être enregistrées avec la nouvelle vue et transmises à la fonction de rappel pointée par _lpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="33100-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="33100-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="33100-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="33100-116">remarquer Pointeur vers un pointeur vers l'affichage nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="33100-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33100-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="33100-117">Return value</span></span>

<span data-ttu-id="33100-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="33100-118">S_OK</span></span> 
  
> <span data-ttu-id="33100-119">L'affichage a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="33100-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33100-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="33100-120">Remarks</span></span>

<span data-ttu-id="33100-121">La méthode **ITableData:: HrGetView** crée une vue en lecture seule des données de la table, triée dans l'ordre dans lequel le paramètre _lpSSortOrderSet_ .</span><span class="sxs-lookup"><span data-stu-id="33100-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="33100-122">Le curseur est placé au début de la première ligne de la vue.</span><span class="sxs-lookup"><span data-stu-id="33100-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="33100-123">Une implémentation d'interface **IMAPITable** pour accéder à la vue est retournée.</span><span class="sxs-lookup"><span data-stu-id="33100-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="33100-124">Les fournisseurs de services appellent **HrGetView** lorsqu'ils doivent accorder à un client l'accès à une table.</span><span class="sxs-lookup"><span data-stu-id="33100-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="33100-125">**HrGetView** crée l'affichage et renvoie le pointeur **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="33100-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="33100-126">Les fournisseurs de services passent à leur tour le pointeur sur le client.</span><span class="sxs-lookup"><span data-stu-id="33100-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="33100-127">Une fois que le client a terminé d'utiliser la table et appelle sa méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** appelle la fonction de rappel pointée par le paramètre _lpfCallerRelease_ .</span><span class="sxs-lookup"><span data-stu-id="33100-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="33100-128">Si un fournisseur de services doit retourner à un client une vue avec un jeu de colonnes personnalisé ou une restriction, le fournisseur peut appeler les méthodes [IMAPITable:: SetColumns](imapitable-setcolumns.md) et [IMAPITable:: Restrict](imapitable-restrict.md) avant d'autoriser l'accès au client.</span><span class="sxs-lookup"><span data-stu-id="33100-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33100-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33100-129">See also</span></span>



[<span data-ttu-id="33100-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="33100-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="33100-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33100-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="33100-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="33100-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="33100-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33100-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

