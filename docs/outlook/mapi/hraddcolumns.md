---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422473"
---
# <a name="hraddcolumns"></a><span data-ttu-id="d7d29-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="d7d29-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="d7d29-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7d29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7d29-105">Ajoute ou déplace des colonnes au début d’un tableau existant.</span><span class="sxs-lookup"><span data-stu-id="d7d29-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7d29-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d7d29-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7d29-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d7d29-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7d29-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d7d29-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7d29-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7d29-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7d29-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d7d29-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7d29-111">Applications clientes et fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="d7d29-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="d7d29-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7d29-112">Parameters</span></span>

 <span data-ttu-id="d7d29-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="d7d29-113">_lptbl_</span></span>
  
> <span data-ttu-id="d7d29-114">[in] Pointeur vers la table MAPI affectée.</span><span class="sxs-lookup"><span data-stu-id="d7d29-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="d7d29-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="d7d29-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="d7d29-116">[in] Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriétés pour les propriétés à ajouter ou déplacer au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="d7d29-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="d7d29-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d7d29-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d7d29-118">[in] Pointeur vers la **fonction MAPIAllocateBuffer.**</span><span class="sxs-lookup"><span data-stu-id="d7d29-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="d7d29-119">Utilisé pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d7d29-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="d7d29-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d7d29-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d7d29-121">[in] Pointeur vers la **fonction MAPIFreeBuffer.**</span><span class="sxs-lookup"><span data-stu-id="d7d29-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="d7d29-122">Utilisé pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d7d29-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7d29-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7d29-123">Return value</span></span>

 <span data-ttu-id="d7d29-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="d7d29-124">**S_OK**</span></span>
  
> <span data-ttu-id="d7d29-125">L’appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.</span><span class="sxs-lookup"><span data-stu-id="d7d29-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7d29-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7d29-126">Remarks</span></span>

<span data-ttu-id="d7d29-127">La **fonction HrAddColumns équivaut** à utiliser **HrAddColumnsEx** avec  _lpfnFilterColumns_ définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="d7d29-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7d29-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d29-128">See also</span></span>



[<span data-ttu-id="d7d29-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="d7d29-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="d7d29-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d7d29-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d7d29-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d7d29-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d7d29-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d7d29-132">SPropTagArray</span></span>](sproptagarray.md)

