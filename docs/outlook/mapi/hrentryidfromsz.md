---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437727"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="15520-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="15520-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="15520-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15520-105">Recrée un identificateur d’entrée à partir de son codage ASCII.</span><span class="sxs-lookup"><span data-stu-id="15520-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15520-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="15520-106">Header file:</span></span>  <br/> |<span data-ttu-id="15520-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="15520-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="15520-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="15520-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="15520-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="15520-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="15520-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="15520-110">Called by:</span></span>  <br/> |<span data-ttu-id="15520-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="15520-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="15520-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="15520-112">Parameters</span></span>

 <span data-ttu-id="15520-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="15520-113">_sz_</span></span>
  
> <span data-ttu-id="15520-114">[in] Pointeur vers la chaîne ASCII à partir de laquelle créer un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="15520-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="15520-115">_pcb_</span><span class="sxs-lookup"><span data-stu-id="15520-115">_pcb_</span></span>
  
> <span data-ttu-id="15520-116">[out] Pointeur vers la taille, en octets, de l’identificateur d’entrée pointé par le _paramètre ppentry._</span><span class="sxs-lookup"><span data-stu-id="15520-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="15520-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="15520-117">_ppentry_</span></span>
  
> <span data-ttu-id="15520-118">[out] Pointeur vers un pointeur vers la structure [ENTRYID](entryid.md) renvoyée qui contient le nouvel identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="15520-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15520-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15520-119">Return value</span></span>

<span data-ttu-id="15520-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="15520-120">S_OK</span></span>
  
> <span data-ttu-id="15520-121">La recréation a réussi.</span><span class="sxs-lookup"><span data-stu-id="15520-121">The recreation was successful.</span></span>
    
<span data-ttu-id="15520-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="15520-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="15520-123">L’ID d’entrée n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="15520-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15520-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="15520-124">Remarks</span></span>

<span data-ttu-id="15520-125">Les **fonctions HrEntryIDFromSz** et [HrSzFromEntryID](hrszfromentryid.md) permettent de convertir les formats de chaîne et binaires des identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="15520-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="15520-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="15520-126">Notes to callers</span></span>

<span data-ttu-id="15520-127">La **fonction HrEntryIDFromSz** alloue de la mémoire pour la chaîne ASCII à l’aide de la [fonction MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="15520-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

