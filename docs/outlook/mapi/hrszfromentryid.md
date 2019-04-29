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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411553"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="51890-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="51890-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="51890-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51890-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51890-105">Encode un identificateur d'entrée dans une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="51890-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51890-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="51890-106">Header file:</span></span>  <br/> |<span data-ttu-id="51890-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="51890-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="51890-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="51890-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="51890-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="51890-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="51890-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="51890-110">Called by:</span></span>  <br/> |<span data-ttu-id="51890-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="51890-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="51890-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51890-112">Parameters</span></span>

 <span data-ttu-id="51890-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="51890-113">_cb_</span></span>
  
> <span data-ttu-id="51890-114">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _pENTRY_ .</span><span class="sxs-lookup"><span data-stu-id="51890-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="51890-115">_pENTRY_</span><span class="sxs-lookup"><span data-stu-id="51890-115">_pentry_</span></span>
  
> <span data-ttu-id="51890-116">dans Pointeur vers une structure [EntryID](entryid.md) qui contient l'identificateur d'entrée à coder.</span><span class="sxs-lookup"><span data-stu-id="51890-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="51890-117">_PSZ_</span><span class="sxs-lookup"><span data-stu-id="51890-117">_psz_</span></span>
  
> <span data-ttu-id="51890-118">remarquer Pointeur vers la chaîne ASCII renvoyée.</span><span class="sxs-lookup"><span data-stu-id="51890-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51890-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51890-119">Return value</span></span>

<span data-ttu-id="51890-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="51890-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51890-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="51890-121">Remarks</span></span>

<span data-ttu-id="51890-122">Les fonctions [HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID** fournissent une conversion entre les formats de chaîne et binaires des identificateurs d'entrée.</span><span class="sxs-lookup"><span data-stu-id="51890-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="51890-123">Avec MAPI, vous devez utiliser des structures avec des données binaires.</span><span class="sxs-lookup"><span data-stu-id="51890-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51890-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="51890-124">Notes to callers</span></span>

<span data-ttu-id="51890-125">La fonction **HrSzFromEntryID** alloue de la mémoire pour la chaîne ASCII à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="51890-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

