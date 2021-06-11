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
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278714"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="746ce-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="746ce-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="746ce-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="746ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="746ce-105">Crée une vue de tableau, renvoyant un pointeur vers une [implémentation IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="746ce-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="746ce-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="746ce-106">Parameters</span></span>

 <span data-ttu-id="746ce-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="746ce-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="746ce-108">[in] Pointeur vers une structure d’ordre de tri qui décrit l’ordre de tri pour l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="746ce-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="746ce-109">Si NULL est transmis dans le  _paramètre lpSSortOrderSet,_ l’affichage n’est pas trié.</span><span class="sxs-lookup"><span data-stu-id="746ce-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="746ce-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="746ce-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="746ce-111">[in] Pointeur vers une fonction de rappel basée sur le prototype [CALLERRELEASE](callerrelease.md) que MAPI appelle lorsqu’il libère l’affichage.</span><span class="sxs-lookup"><span data-stu-id="746ce-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="746ce-112">Si NULL est transmis dans le  _paramètre lpfCallerRelease,_ aucune fonction n’est appelée lors de la publication de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="746ce-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="746ce-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="746ce-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="746ce-114">[in] Les données qui doivent être enregistrées avec la nouvelle vue et transmises à la fonction de rappel pointée par  _lpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="746ce-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="746ce-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="746ce-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="746ce-116">[out] Pointeur vers un pointeur vers la vue nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="746ce-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="746ce-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="746ce-117">Return value</span></span>

<span data-ttu-id="746ce-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="746ce-118">S_OK</span></span> 
  
> <span data-ttu-id="746ce-119">L’affichage a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="746ce-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="746ce-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="746ce-120">Remarks</span></span>

<span data-ttu-id="746ce-121">La **méthode ITableData::HrGetView** crée une vue en lecture seule des données de la table, triées dans l’ordre indiqué par le paramètre _lpSSortOrderSet._</span><span class="sxs-lookup"><span data-stu-id="746ce-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="746ce-122">Le curseur est placé au début de la première ligne de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="746ce-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="746ce-123">Une **implémentation d’interface IMAPITable** pour accéder à l’affichage est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="746ce-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="746ce-124">Les fournisseurs de services **appellent HrGetView** lorsqu’ils ont besoin d’accorder à un client l’accès à une table.</span><span class="sxs-lookup"><span data-stu-id="746ce-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="746ce-125">**HrGetView crée** l’affichage et renvoie le **pointeur IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="746ce-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="746ce-126">À leur tour, les fournisseurs de services passent le pointeur au client.</span><span class="sxs-lookup"><span data-stu-id="746ce-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="746ce-127">Lorsque le client a terminé d’utiliser la table et appelle sa méthode [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) **HrGetView** appelle la fonction de rappel pointée par le paramètre _lpfCallerRelease._</span><span class="sxs-lookup"><span data-stu-id="746ce-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="746ce-128">Si un fournisseur de services doit retourner à un client un affichage qui possède un ensemble de colonnes personnalisé ou une restriction, il peut appeler les méthodes [IMAPITable::SetColumns](imapitable-setcolumns.md) et [IMAPITable::Restrict](imapitable-restrict.md) de l’affichage avant d’autoriser l’accès au client.</span><span class="sxs-lookup"><span data-stu-id="746ce-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="746ce-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="746ce-129">See also</span></span>



[<span data-ttu-id="746ce-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="746ce-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="746ce-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="746ce-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="746ce-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="746ce-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="746ce-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="746ce-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

