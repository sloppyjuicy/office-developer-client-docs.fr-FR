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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e97e1d5302d8247cb09ce7cb1b581582405300a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568127"
---
# <a name="callerrelease"></a><span data-ttu-id="85362-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="85362-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="85362-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85362-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85362-105">Définit une fonction de rappel pouvant déclencher un objet de données de table lors de l’affichage tableau a été publié.</span><span class="sxs-lookup"><span data-stu-id="85362-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85362-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="85362-106">Header file:</span></span>  <br/> |<span data-ttu-id="85362-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="85362-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="85362-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="85362-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="85362-109">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="85362-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="85362-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="85362-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="85362-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="85362-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="85362-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85362-112">Parameters</span></span>

 <span data-ttu-id="85362-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="85362-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="85362-114">[in] Fonction de rappel en fonction de données de l’appelant enregistré par MAPI avec l’affichage tableau et transmises à la **CALLERRELEASE** .</span><span class="sxs-lookup"><span data-stu-id="85362-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="85362-115">Les données fournissent un contexte relatif à l’affichage tableau libéré.</span><span class="sxs-lookup"><span data-stu-id="85362-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="85362-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="85362-116">_lpTblData_</span></span>
  
> <span data-ttu-id="85362-117">[in] Pointeur vers le [ITableData : IUnknown](itabledataiunknown.md) interface pour l’objet de données de table sous-jacentes de la vue table publiée.</span><span class="sxs-lookup"><span data-stu-id="85362-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="85362-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="85362-118">_lpVue_</span></span>
  
> <span data-ttu-id="85362-119">[in] Pointeur vers le [IMAPITable : IUnknown](imapitableiunknown.md) interface pour l’affichage de la table publiée.</span><span class="sxs-lookup"><span data-stu-id="85362-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="85362-120">Il s’agit d’une interface de l’objet table renvoyé dans le paramètre _lppMAPITable_ de la méthode [ITableData::HrGetView](itabledata-hrgetview.md) qui a créé l’objet pour libérer.</span><span class="sxs-lookup"><span data-stu-id="85362-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85362-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="85362-121">Return value</span></span>

<span data-ttu-id="85362-122">Aucune</span><span class="sxs-lookup"><span data-stu-id="85362-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85362-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="85362-123">Remarks</span></span>

<span data-ttu-id="85362-124">Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData::HrGetView](itabledata-hrgetview.md) pour créer un affichage en lecture seule, trié de la table.</span><span class="sxs-lookup"><span data-stu-id="85362-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="85362-125">L’appel vers **HrGetView** passe un pointeur vers une fonction de rappel **CALLERRELEASE** basé et également un contexte soit enregistré avec l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="85362-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="85362-126">Lorsque le décompte de références de l’affichage tableau renvoie zéro et la vue est publiée, l’implémentation **IMAPITable** appelle la fonction de rappel, en passant le contexte dans le paramètre _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="85362-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="85362-127">Une utilisation courante d’une fonction de rappel **CALLERRELEASE** en est pour libérer de l’objet de données de table sous-jacente et n’ont pas à garder une trace des il lors du traitement suivant.</span><span class="sxs-lookup"><span data-stu-id="85362-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

