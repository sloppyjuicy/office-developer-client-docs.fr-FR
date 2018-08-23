---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573368"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="6d623-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="6d623-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="6d623-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d623-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d623-105">Sépare l’identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages, dans l’identificateur d’entrée de cet objet dans le magasin et l’identificateur d’entrée du magasin.</span><span class="sxs-lookup"><span data-stu-id="6d623-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d623-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6d623-106">Header file:</span></span>  <br/> |<span data-ttu-id="6d623-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6d623-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6d623-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6d623-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6d623-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6d623-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6d623-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6d623-110">Called by:</span></span>  <br/> |<span data-ttu-id="6d623-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="6d623-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="6d623-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d623-112">Parameters</span></span>

 <span data-ttu-id="6d623-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="6d623-113">_psession_</span></span>
  
> <span data-ttu-id="6d623-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="6d623-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="6d623-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="6d623-115">_cbEID_</span></span>
  
> <span data-ttu-id="6d623-116">[in] Taille, en octets, de l’identificateur d’entrée composés d’être séparées.</span><span class="sxs-lookup"><span data-stu-id="6d623-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="6d623-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="6d623-117">_pEID_</span></span>
  
> <span data-ttu-id="6d623-118">[in] Pointeur vers l’identificateur d’entrée composés d’être séparées.</span><span class="sxs-lookup"><span data-stu-id="6d623-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="6d623-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="6d623-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="6d623-120">[out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de la banque de messages qui contient l’objet.</span><span class="sxs-lookup"><span data-stu-id="6d623-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="6d623-121">Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, le paramètre _pcbStoreEID_ pointe sur une valeur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6d623-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="6d623-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="6d623-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="6d623-123">[out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée de la banque de messages qui contient l’objet.</span><span class="sxs-lookup"><span data-stu-id="6d623-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="6d623-124">Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, NULL est renvoyée dans le paramètre _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="6d623-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="6d623-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="6d623-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="6d623-126">[out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6d623-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="6d623-127">Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="6d623-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="6d623-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="6d623-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="6d623-129">[out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6d623-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="6d623-130">Si le paramètre _pEID_ pointe vers un identificateur d’entrée non composés, _ppMsgEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée non composés.</span><span class="sxs-lookup"><span data-stu-id="6d623-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6d623-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d623-131">Return value</span></span>

<span data-ttu-id="6d623-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6d623-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d623-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d623-133">Remarks</span></span>

<span data-ttu-id="6d623-134">Si l’identificateur spécifié par le paramètre _pEID_ est composée, elle est divisée en l’identificateur d’entrée de l’objet dans sa banque de messages et l’identificateur d’entrée du magasin.</span><span class="sxs-lookup"><span data-stu-id="6d623-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="6d623-135">Chaînes identificateur d’entrée non composés sont simplement copiés.</span><span class="sxs-lookup"><span data-stu-id="6d623-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="6d623-136">L’identificateur composé à être séparée est généralement créée par la fonction [HrComposeEID](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="6d623-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6d623-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="6d623-137">Notes to callers</span></span>

<span data-ttu-id="6d623-138">La mémoire qui contient le paramètre _pEID_ est publiée en cas de réussite de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6d623-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="6d623-139">Implémentation de l’appelante est chargée de libérer de la mémoire pour les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="6d623-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

