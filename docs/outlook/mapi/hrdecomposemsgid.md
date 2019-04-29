---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404434"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="8103c-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="8103c-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="8103c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8103c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8103c-105">Sépare la représentation ASCII de l'identificateur d'entrée composé d'un objet, généralement un message dans une banque de messages, dans l'identificateur d'entrée de cet objet dans le magasin et l'identificateur d'entrée du magasin.</span><span class="sxs-lookup"><span data-stu-id="8103c-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8103c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8103c-106">Header file:</span></span>  <br/> |<span data-ttu-id="8103c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8103c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8103c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8103c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8103c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8103c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8103c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8103c-110">Called by:</span></span>  <br/> |<span data-ttu-id="8103c-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="8103c-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="8103c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8103c-112">Parameters</span></span>

 <span data-ttu-id="8103c-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="8103c-113">_psession_</span></span>
  
> <span data-ttu-id="8103c-114">dans Pointeur vers la session en cours d'utilisation par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="8103c-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="8103c-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="8103c-115">_szMsgID_</span></span>
  
> <span data-ttu-id="8103c-116">dans La chaîne représentant l'identificateur d'entrée de l'objet.</span><span class="sxs-lookup"><span data-stu-id="8103c-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="8103c-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="8103c-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="8103c-118">remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de la Banque de messages qui contient l'objet.</span><span class="sxs-lookup"><span data-stu-id="8103c-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="8103c-119">Si le paramètre _szMsgID_ pointe vers une chaîne d'identificateur d'entrée non composée, le paramètre _pcbStoreEID_ pointe vers zéro.</span><span class="sxs-lookup"><span data-stu-id="8103c-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="8103c-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="8103c-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="8103c-121">remarquer Pointeur vers un pointeur vers l'identificateur d'entrée retourné de la Banque de messages qui contient l'objet.</span><span class="sxs-lookup"><span data-stu-id="8103c-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="8103c-122">Si le paramètre _szMsgID_ pointe vers un identificateur d'entrée non composé, la valeur null est renvoyée dans le paramètre _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="8103c-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="8103c-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="8103c-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="8103c-124">remarquer Pointeur vers la taille renvoyée, en octets, de l'identificateur d'entrée de l'objet dans son magasin.</span><span class="sxs-lookup"><span data-stu-id="8103c-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="8103c-125">Si le paramètre _szMsgID_ pointe vers une chaîne d'identificateur d'entrée non composée, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="8103c-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="8103c-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="8103c-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="8103c-127">remarquer Pointeur vers un pointeur vers la chaîne d'identificateur d'entrée renvoyée de l'objet dans son magasin.</span><span class="sxs-lookup"><span data-stu-id="8103c-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="8103c-128">Si le paramètre _szMsgID_ pointe vers un identificateur d'entrée décomposée, _ppMsgEID_ pointe vers un pointeur vers une copie convertie de l'identificateur d'entrée de composition.</span><span class="sxs-lookup"><span data-stu-id="8103c-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8103c-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8103c-129">Return value</span></span>

<span data-ttu-id="8103c-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8103c-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8103c-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="8103c-131">Remarks</span></span>

<span data-ttu-id="8103c-132">Si l'identificateur spécifié par le paramètre _szMsgID_ est composé, il est converti à partir de ASCII et scindé en l'identificateur d'entrée de l'objet dans sa banque de messages et l'identificateur d'entrée du magasin.</span><span class="sxs-lookup"><span data-stu-id="8103c-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="8103c-133">Les chaînes d'identificateur d'entrée non composées sont simplement converties et copiées.</span><span class="sxs-lookup"><span data-stu-id="8103c-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="8103c-134">La chaîne d'identificateur composée à séparer est généralement une chaîne créée par la fonction [HrComposeMsgID](hrcomposemsgid.md) .</span><span class="sxs-lookup"><span data-stu-id="8103c-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="8103c-135">L'appel de la fonction **HrDecomposeMsgID** équivaut à l'appel de la fonction [HrEntryIDFromSz](hrentryidfromsz.md) , puis à la fonction [HrDecomposeEID](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="8103c-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

