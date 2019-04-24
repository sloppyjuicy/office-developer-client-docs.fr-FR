---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346416"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="be97c-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="be97c-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="be97c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be97c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be97c-105">Encode un identificateur d'entrée dans une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="be97c-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be97c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="be97c-106">Header file:</span></span>  <br/> |<span data-ttu-id="be97c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="be97c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="be97c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="be97c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="be97c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="be97c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="be97c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="be97c-110">Called by:</span></span>  <br/> |<span data-ttu-id="be97c-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="be97c-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="be97c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be97c-112">Parameters</span></span>

 <span data-ttu-id="be97c-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="be97c-113">_cb_</span></span>
  
> <span data-ttu-id="be97c-114">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _pENTRY_ .</span><span class="sxs-lookup"><span data-stu-id="be97c-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="be97c-115">_pENTRY_</span><span class="sxs-lookup"><span data-stu-id="be97c-115">_pentry_</span></span>
  
> <span data-ttu-id="be97c-116">dans Pointeur vers une structure [EntryID](entryid.md) qui contient l'identificateur d'entrée à coder.</span><span class="sxs-lookup"><span data-stu-id="be97c-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="be97c-117">_PSZ_</span><span class="sxs-lookup"><span data-stu-id="be97c-117">_psz_</span></span>
  
> <span data-ttu-id="be97c-118">remarquer Pointeur vers la chaîne ASCII renvoyée.</span><span class="sxs-lookup"><span data-stu-id="be97c-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be97c-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be97c-119">Return value</span></span>

<span data-ttu-id="be97c-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="be97c-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be97c-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="be97c-121">Remarks</span></span>

<span data-ttu-id="be97c-122">Les fonctions [HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID** fournissent une conversion entre les formats de chaîne et binaires des identificateurs d'entrée.</span><span class="sxs-lookup"><span data-stu-id="be97c-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="be97c-123">Avec MAPI, vous devez utiliser des structures avec des données binaires.</span><span class="sxs-lookup"><span data-stu-id="be97c-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="be97c-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="be97c-124">Notes to callers</span></span>

<span data-ttu-id="be97c-125">La fonction **HrSzFromEntryID** alloue de la mémoire pour la chaîne ASCII à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="be97c-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

