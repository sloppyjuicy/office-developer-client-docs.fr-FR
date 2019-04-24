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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348068"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="db856-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="db856-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="db856-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db856-105">Sépare l'identificateur d'entrée composé d'un objet, généralement un message dans une banque de messages, dans l'identificateur d'entrée de cet objet dans le magasin et dans l'identificateur d'entrée de la Banque.</span><span class="sxs-lookup"><span data-stu-id="db856-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db856-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="db856-106">Header file:</span></span>  <br/> |<span data-ttu-id="db856-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="db856-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="db856-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="db856-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="db856-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="db856-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="db856-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="db856-110">Called by:</span></span>  <br/> |<span data-ttu-id="db856-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="db856-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="db856-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db856-112">Parameters</span></span>

 <span data-ttu-id="db856-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="db856-113">_psession_</span></span>
  
> <span data-ttu-id="db856-114">dans Pointeur vers la session en cours d'utilisation par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="db856-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="db856-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="db856-115">_cbEID_</span></span>
  
> <span data-ttu-id="db856-116">dans Taille, en octets, de l'identificateur d'entrée composée à séparer.</span><span class="sxs-lookup"><span data-stu-id="db856-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="db856-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="db856-117">_pEID_</span></span>
  
> <span data-ttu-id="db856-118">dans Pointeur vers l'identificateur d'entrée composée à séparer.</span><span class="sxs-lookup"><span data-stu-id="db856-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="db856-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="db856-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="db856-120">remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de la Banque de messages qui contient l'objet.</span><span class="sxs-lookup"><span data-stu-id="db856-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="db856-121">Si le paramètre _pEID_ pointe vers un identificateur d'entrée non composé, le paramètre _pcbStoreEID_ pointe vers la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="db856-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="db856-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="db856-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="db856-123">remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné de la Banque de messages qui contient l'objet.</span><span class="sxs-lookup"><span data-stu-id="db856-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="db856-124">Si le paramètre _pEID_ pointe vers un identificateur d'entrée non composé, la valeur null est renvoyée dans le paramètre _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="db856-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="db856-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="db856-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="db856-126">remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de l'objet.</span><span class="sxs-lookup"><span data-stu-id="db856-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="db856-127">Si le paramètre _pEID_ pointe vers un identificateur d'entrée non composé, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="db856-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="db856-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="db856-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="db856-129">remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné de l'objet.</span><span class="sxs-lookup"><span data-stu-id="db856-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="db856-130">Si le paramètre _pEID_ pointe vers un identificateur d'entrée qui n'est pas composé, _ppMsgEID_ pointe vers un pointeur vers une copie de l'identificateur d'entrée incomposé.</span><span class="sxs-lookup"><span data-stu-id="db856-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="db856-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db856-131">Return value</span></span>

<span data-ttu-id="db856-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="db856-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db856-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="db856-133">Remarks</span></span>

<span data-ttu-id="db856-134">Si l'identificateur spécifié par le paramètre _pEID_ est composé, il est scindé en identificateur d'entrée de l'objet au sein de sa banque de messages et de l'identificateur d'entrée de la Banque.</span><span class="sxs-lookup"><span data-stu-id="db856-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="db856-135">Les chaînes d'identificateur d'entrée non composées sont simplement copiées.</span><span class="sxs-lookup"><span data-stu-id="db856-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="db856-136">L'identificateur composé à séparer est généralement un identificateur créé par la fonction [HrComposeEID](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="db856-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="db856-137">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="db856-137">Notes to callers</span></span>

<span data-ttu-id="db856-138">La mémoire qui contient le paramètre _pEID_ est publiée lors de l'exécution correcte de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="db856-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="db856-139">L'implémentation appelante est chargée de libérer de la mémoire pour les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="db856-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

