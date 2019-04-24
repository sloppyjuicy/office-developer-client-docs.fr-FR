---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331842"
---
# <a name="callerrelease"></a><span data-ttu-id="4a7b6-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="4a7b6-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="4a7b6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a7b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a7b6-105">Définit une fonction de rappel qui peut publier un objet de données de tableau lors de la publication d'un affichage de tableau.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a7b6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4a7b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a7b6-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="4a7b6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4a7b6-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="4a7b6-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4a7b6-109">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4a7b6-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="4a7b6-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="4a7b6-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4a7b6-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a7b6-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="4a7b6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a7b6-112">Parameters</span></span>

 <span data-ttu-id="4a7b6-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="4a7b6-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="4a7b6-114">dans Données de l'appelant enregistrées par MAPI avec la vue de table et transmises à la fonction de rappel basée sur **CALLERRELEASE** .</span><span class="sxs-lookup"><span data-stu-id="4a7b6-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="4a7b6-115">Les données fournissent un contexte sur l'affichage tableau en cours de publication.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="4a7b6-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="4a7b6-116">_lpTblData_</span></span>
  
> <span data-ttu-id="4a7b6-117">dans Pointeur vers l'interface [ITableData: IUnknown](itabledataiunknown.md) pour l'objet de données de tableau sous-jacent de la vue de tableau en cours de publication.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="4a7b6-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="4a7b6-118">_lpVue_</span></span>
  
> <span data-ttu-id="4a7b6-119">dans Pointeur vers l'interface [IMAPITable: IUnknown](imapitableiunknown.md) pour l'affichage tableau en cours de publication.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="4a7b6-120">Il s'agit d'une interface pour l'objet Table renvoyé dans le paramètre _lppMAPITable_ de la méthode [ITableData:: HrGetView](itabledata-hrgetview.md) qui a créé l'objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4a7b6-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a7b6-121">Return value</span></span>

<span data-ttu-id="4a7b6-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="4a7b6-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4a7b6-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a7b6-123">Remarks</span></span>

<span data-ttu-id="4a7b6-124">Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData:: HrGetView](itabledata-hrgetview.md) pour créer une vue triée en lecture seule de la table.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="4a7b6-125">L'appel à **HrGetView** transmet un pointeur vers une fonction de rappel basée sur **CALLERRELEASE** et également un contexte à enregistrer avec la vue de table.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="4a7b6-126">Lorsque le décompte de références de l'affichage de tableau est remis à zéro et que la vue est publiée, l'implémentation de la méthode **IMAPITable** appelle la fonction de rappel, en transmettant le contexte dans le paramètre _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="4a7b6-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="4a7b6-127">Une utilisation courante d'une fonction de rappel basée sur **CALLERRELEASE** consiste à libérer l'objet de données de la table sous-jacente et à ne pas le suivre pendant un traitement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="4a7b6-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

