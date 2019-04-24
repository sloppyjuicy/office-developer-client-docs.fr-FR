---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348194"
---
# <a name="hraddcolumns"></a><span data-ttu-id="e8875-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="e8875-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="e8875-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8875-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8875-105">Ajoute ou déplace des colonnes au début d'une table existante.</span><span class="sxs-lookup"><span data-stu-id="e8875-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8875-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e8875-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8875-107">mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e8875-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e8875-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e8875-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e8875-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e8875-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e8875-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e8875-110">Called by:</span></span>  <br/> |<span data-ttu-id="e8875-111">Applications clientes et fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="e8875-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="e8875-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8875-112">Parameters</span></span>

 <span data-ttu-id="e8875-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="e8875-113">_lptbl_</span></span>
  
> <span data-ttu-id="e8875-114">dans Pointeur vers le tableau MAPI affecté.</span><span class="sxs-lookup"><span data-stu-id="e8875-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="e8875-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="e8875-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="e8875-116">dans Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacer au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="e8875-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="e8875-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e8875-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e8875-118">dans Pointeur vers la fonction **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="e8875-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="e8875-119">Permet d'allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8875-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="e8875-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e8875-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e8875-121">dans Pointeur vers la fonction **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="e8875-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="e8875-122">Permet de libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8875-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8875-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8875-123">Return value</span></span>

 <span data-ttu-id="e8875-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="e8875-124">**S_OK**</span></span>
  
> <span data-ttu-id="e8875-125">L'appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.</span><span class="sxs-lookup"><span data-stu-id="e8875-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8875-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8875-126">Remarks</span></span>

<span data-ttu-id="e8875-127">La fonction **HrAddColumns** est équivalente à l'utilisation de **HrAddColumnsEx** avec _lpfnFilterColumns_ définie sur null.</span><span class="sxs-lookup"><span data-stu-id="e8875-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8875-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8875-128">See also</span></span>



[<span data-ttu-id="e8875-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="e8875-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="e8875-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e8875-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e8875-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e8875-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e8875-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e8875-132">SPropTagArray</span></span>](sproptagarray.md)

