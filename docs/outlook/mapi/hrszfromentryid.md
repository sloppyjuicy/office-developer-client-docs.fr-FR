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
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783560"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="96b84-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="96b84-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="96b84-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96b84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96b84-105">Code un identificateur d’entrée en une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="96b84-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96b84-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="96b84-106">Header file:</span></span>  <br/> |<span data-ttu-id="96b84-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="96b84-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="96b84-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="96b84-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="96b84-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96b84-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96b84-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="96b84-110">Called by:</span></span>  <br/> |<span data-ttu-id="96b84-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="96b84-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="96b84-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96b84-112">Parameters</span></span>

 <span data-ttu-id="96b84-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="96b84-113">_cb_</span></span>
  
> <span data-ttu-id="96b84-114">[in] Taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _pentry_ .</span><span class="sxs-lookup"><span data-stu-id="96b84-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="96b84-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="96b84-115">_pentry_</span></span>
  
> <span data-ttu-id="96b84-116">[in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée qui doivent être codées.</span><span class="sxs-lookup"><span data-stu-id="96b84-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="96b84-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="96b84-117">_psz_</span></span>
  
> <span data-ttu-id="96b84-118">[out] Pointeur vers la chaîne retournée ASCII.</span><span class="sxs-lookup"><span data-stu-id="96b84-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="96b84-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="96b84-119">Return value</span></span>

<span data-ttu-id="96b84-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="96b84-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96b84-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="96b84-121">Remarks</span></span>

<span data-ttu-id="96b84-122">Les fonctions [HrEntryIDFromSz](hrentryidfromsz.md) et **HrSzFromEntryID** fournissent la conversion entre les formats binaires d’identificateurs d’entrée de chaîne.</span><span class="sxs-lookup"><span data-stu-id="96b84-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="96b84-123">MAPI, vous devez utiliser les structures des données binaires.</span><span class="sxs-lookup"><span data-stu-id="96b84-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="96b84-124">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="96b84-124">Notes to callers</span></span>

<span data-ttu-id="96b84-125">La fonction **HrSzFromEntryID** alloue de la mémoire de la chaîne ASCII à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="96b84-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

