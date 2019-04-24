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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347809"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="cc368-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="cc368-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="cc368-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc368-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc368-105">Recrée un identificateur d'entrée à partir de son codage ASCII.</span><span class="sxs-lookup"><span data-stu-id="cc368-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc368-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cc368-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc368-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="cc368-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cc368-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="cc368-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc368-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc368-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc368-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="cc368-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc368-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="cc368-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="cc368-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc368-112">Parameters</span></span>

 <span data-ttu-id="cc368-113">_t_</span><span class="sxs-lookup"><span data-stu-id="cc368-113">_sz_</span></span>
  
> <span data-ttu-id="cc368-114">dans Pointeur vers la chaîne ASCII à partir de laquelle créer un identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="cc368-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="cc368-115">_circuits_</span><span class="sxs-lookup"><span data-stu-id="cc368-115">_pcb_</span></span>
  
> <span data-ttu-id="cc368-116">remarquer Pointeur vers la taille, en octets, de l'identificateur d'entrée pointé par le paramètre _ppentry_ .</span><span class="sxs-lookup"><span data-stu-id="cc368-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="cc368-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="cc368-117">_ppentry_</span></span>
  
> <span data-ttu-id="cc368-118">remarquer Pointeur vers un pointeur vers la structure [EntryID](entryid.md) renvoyée qui contient le nouvel identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="cc368-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cc368-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc368-119">Return value</span></span>

<span data-ttu-id="cc368-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc368-120">S_OK</span></span>
  
> <span data-ttu-id="cc368-121">La loisirs a réussi.</span><span class="sxs-lookup"><span data-stu-id="cc368-121">The recreation was successful.</span></span>
    
<span data-ttu-id="cc368-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cc368-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="cc368-123">L'ID d'entrée n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cc368-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc368-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc368-124">Remarks</span></span>

<span data-ttu-id="cc368-125">Les fonctions **HrEntryIDFromSz** et [HrSzFromEntryID](hrszfromentryid.md) fournissent une conversion entre les formats de chaîne et binaires des identificateurs d'entrée.</span><span class="sxs-lookup"><span data-stu-id="cc368-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cc368-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="cc368-126">Notes to callers</span></span>

<span data-ttu-id="cc368-127">La fonction **HrEntryIDFromSz** alloue de la mémoire pour la chaîne ASCII à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cc368-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

