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
ms.openlocfilehash: a524a7eb40c33d6de2f64cd5373c9a39a8a1e3df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565297"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="cd486-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="cd486-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="cd486-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd486-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd486-105">Recrée un identificateur d’entrée à partir de l’encodage ASCII.</span><span class="sxs-lookup"><span data-stu-id="cd486-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd486-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cd486-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd486-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cd486-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cd486-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="cd486-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd486-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cd486-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cd486-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="cd486-110">Called by:</span></span>  <br/> |<span data-ttu-id="cd486-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="cd486-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="cd486-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd486-112">Parameters</span></span>

 <span data-ttu-id="cd486-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="cd486-113">_sz_</span></span>
  
> <span data-ttu-id="cd486-114">[in] Pointeur vers la chaîne de caractères ASCII à partir de laquelle créer un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cd486-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="cd486-115">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="cd486-115">_pcb_</span></span>
  
> <span data-ttu-id="cd486-116">[out] Pointeur vers la taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _ppentry_ .</span><span class="sxs-lookup"><span data-stu-id="cd486-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="cd486-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="cd486-117">_ppentry_</span></span>
  
> <span data-ttu-id="cd486-118">[out] Pointeur vers un pointeur vers la structure [ENTRYID](entryid.md) retournée qui contient l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cd486-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cd486-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cd486-119">Return value</span></span>

<span data-ttu-id="cd486-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd486-120">S_OK</span></span>
  
> <span data-ttu-id="cd486-121">La recréation a réussi.</span><span class="sxs-lookup"><span data-stu-id="cd486-121">The recreation was successful.</span></span>
    
<span data-ttu-id="cd486-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cd486-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="cd486-123">L’identificateur d’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cd486-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd486-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd486-124">Remarks</span></span>

<span data-ttu-id="cd486-125">Les fonctions **HrEntryIDFromSz** et [HrSzFromEntryID](hrszfromentryid.md) fournissent la conversion entre les formats binaires d’identificateurs d’entrée de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cd486-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cd486-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="cd486-126">Notes to callers</span></span>

<span data-ttu-id="cd486-127">La fonction **HrEntryIDFromSz** alloue de la mémoire de la chaîne ASCII à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cd486-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

