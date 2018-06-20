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
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783513"
---
# <a name="hraddcolumns"></a><span data-ttu-id="4d8c1-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="4d8c1-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="4d8c1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d8c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d8c1-105">Ajoute ou déplacer des colonnes au début d’une table existante.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d8c1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4d8c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="4d8c1-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4d8c1-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4d8c1-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4d8c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4d8c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4d8c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4d8c1-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="4d8c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="4d8c1-111">Applications clientes et des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="4d8c1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d8c1-112">Parameters</span></span>

 <span data-ttu-id="4d8c1-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="4d8c1-113">_lptbl_</span></span>
  
> <span data-ttu-id="4d8c1-114">[in] Pointeur vers le tableau MAPI affecté.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="4d8c1-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="4d8c1-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="4d8c1-116">[in] Pointeur vers une structure **SPropTagArray** qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacées vers le début de la table.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="4d8c1-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4d8c1-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4d8c1-118">[in] Pointeur vers la fonction **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="4d8c1-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="4d8c1-119">Utilisé pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="4d8c1-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4d8c1-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4d8c1-121">[in] Pointeur vers la fonction **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="4d8c1-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="4d8c1-122">Utilisé pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d8c1-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4d8c1-123">Return value</span></span>

 <span data-ttu-id="4d8c1-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="4d8c1-124">**S_OK**</span></span>
  
> <span data-ttu-id="4d8c1-125">L’appel a réussi et les colonnes spécifiées ont été déplacés ou ajoutés.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d8c1-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d8c1-126">Remarks</span></span>

<span data-ttu-id="4d8c1-127">La fonction **HrAddColumns** est équivalente à l’utilisation de **HrAddColumnsEx** avec _lpfnFilterColumns_ la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="4d8c1-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d8c1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d8c1-128">See also</span></span>



[<span data-ttu-id="4d8c1-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="4d8c1-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="4d8c1-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4d8c1-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4d8c1-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4d8c1-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4d8c1-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4d8c1-132">SPropTagArray</span></span>](sproptagarray.md)

