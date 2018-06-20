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
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782993"
---
# <a name="callerrelease"></a><span data-ttu-id="a43fb-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="a43fb-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="a43fb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a43fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a43fb-105">Définit une fonction de rappel pouvant déclencher un objet de données de table lors de l’affichage tableau a été publié.</span><span class="sxs-lookup"><span data-stu-id="a43fb-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a43fb-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a43fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="a43fb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a43fb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a43fb-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a43fb-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a43fb-109">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a43fb-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="a43fb-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="a43fb-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a43fb-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a43fb-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="a43fb-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a43fb-112">Parameters</span></span>

 <span data-ttu-id="a43fb-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="a43fb-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="a43fb-114">[in] Fonction de rappel en fonction de données de l’appelant enregistré par MAPI avec l’affichage tableau et transmises à la **CALLERRELEASE** .</span><span class="sxs-lookup"><span data-stu-id="a43fb-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="a43fb-115">Les données fournissent un contexte relatif à l’affichage tableau libéré.</span><span class="sxs-lookup"><span data-stu-id="a43fb-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="a43fb-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="a43fb-116">_lpTblData_</span></span>
  
> <span data-ttu-id="a43fb-117">[in] Pointeur vers le [ITableData : IUnknown](itabledataiunknown.md) interface pour l’objet de données de table sous-jacentes de la vue table publiée.</span><span class="sxs-lookup"><span data-stu-id="a43fb-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="a43fb-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="a43fb-118">_lpVue_</span></span>
  
> <span data-ttu-id="a43fb-119">[in] Pointeur vers le [IMAPITable : IUnknown](imapitableiunknown.md) interface pour l’affichage de la table publiée.</span><span class="sxs-lookup"><span data-stu-id="a43fb-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="a43fb-120">Il s’agit d’une interface de l’objet table renvoyé dans le paramètre _lppMAPITable_ de la méthode [ITableData::HrGetView](itabledata-hrgetview.md) qui a créé l’objet pour libérer.</span><span class="sxs-lookup"><span data-stu-id="a43fb-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a43fb-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a43fb-121">Return value</span></span>

<span data-ttu-id="a43fb-122">Aucune</span><span class="sxs-lookup"><span data-stu-id="a43fb-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a43fb-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="a43fb-123">Remarks</span></span>

<span data-ttu-id="a43fb-124">Une application cliente ou un fournisseur de services qui a rempli un objet de données de table peut appeler [ITableData::HrGetView](itabledata-hrgetview.md) pour créer un affichage en lecture seule, trié de la table.</span><span class="sxs-lookup"><span data-stu-id="a43fb-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="a43fb-125">L’appel vers **HrGetView** passe un pointeur vers une fonction de rappel **CALLERRELEASE** basé et également un contexte soit enregistré avec l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="a43fb-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="a43fb-126">Lorsque le décompte de références de l’affichage tableau renvoie zéro et la vue est publiée, l’implémentation **IMAPITable** appelle la fonction de rappel, en passant le contexte dans le paramètre _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="a43fb-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="a43fb-127">Une utilisation courante d’une fonction de rappel **CALLERRELEASE** en est pour libérer de l’objet de données de table sous-jacente et n’ont pas à garder une trace des il lors du traitement suivant.</span><span class="sxs-lookup"><span data-stu-id="a43fb-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

