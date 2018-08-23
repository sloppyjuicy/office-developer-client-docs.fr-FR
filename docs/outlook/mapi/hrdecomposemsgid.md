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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 828d7ebcbceead02441165e3af92ec7b47d9f001
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564625"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="6f1f8-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="6f1f8-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="6f1f8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f1f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f1f8-105">Sépare la représentation ASCII de l’identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages, l’identificateur d’entrée de cet objet dans le magasin et l’identificateur d’entrée du magasin.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f1f8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6f1f8-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f1f8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6f1f8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6f1f8-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6f1f8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6f1f8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6f1f8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6f1f8-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6f1f8-110">Called by:</span></span>  <br/> |<span data-ttu-id="6f1f8-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="6f1f8-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6f1f8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f1f8-112">Parameters</span></span>

 <span data-ttu-id="6f1f8-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="6f1f8-113">_psession_</span></span>
  
> <span data-ttu-id="6f1f8-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="6f1f8-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="6f1f8-115">_szMsgID_</span></span>
  
> <span data-ttu-id="6f1f8-116">[in] La chaîne représentant l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="6f1f8-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="6f1f8-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="6f1f8-118">[out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de la banque de messages qui contient l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="6f1f8-119">Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée non composés chaîne, le paramètre _pcbStoreEID_ pointe sur zéro.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="6f1f8-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="6f1f8-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="6f1f8-121">[out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée de la banque de messages qui contient l’objet.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="6f1f8-122">Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée non composés, NULL est renvoyée dans le paramètre _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="6f1f8-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="6f1f8-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="6f1f8-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="6f1f8-124">[out] Pointeur vers la taille retournée, en octets, de l’identificateur d’entrée de l’objet dans son magasin.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="6f1f8-125">Si le paramètre _szMsgID_ pointe vers une chaîne d’identificateur de l’entrée non composés, le paramètre _pcbMsgEID_ est égal à la valeur du paramètre _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="6f1f8-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="6f1f8-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="6f1f8-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="6f1f8-127">[out] Pointeur vers un pointeur vers la chaîne d’identificateur de l’objet dans son magasin entrée retournée.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="6f1f8-128">Si le paramètre _szMsgID_ pointe vers un identificateur d’entrée non composés, _ppMsgEID_ pointe vers un pointeur vers une copie convertie de l’identificateur d’entrée non composés.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f1f8-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6f1f8-129">Return value</span></span>

<span data-ttu-id="6f1f8-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f1f8-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f1f8-131">Remarks</span></span>

<span data-ttu-id="6f1f8-132">Si l’identificateur spécifié par le paramètre _szMsgID_ est composée, il est converti à partir d’ASCII et résulter de l’identificateur d’entrée de l’objet dans sa banque de messages et l’identificateur d’entrée du magasin.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="6f1f8-133">Chaînes identificateur d’entrée non composés sont simplement convertis et copiés.</span><span class="sxs-lookup"><span data-stu-id="6f1f8-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="6f1f8-134">La chaîne d’identificateur composés à être séparée est généralement créée par la fonction [HrComposeMsgID](hrcomposemsgid.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1f8-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="6f1f8-135">La fonction **HrDecomposeMsgID** équivaut à appeler la fonction [HrEntryIDFromSz](hrentryidfromsz.md) , puis la fonction [HrDecomposeEID](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1f8-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

