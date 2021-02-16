---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429046"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="08183-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="08183-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="08183-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08183-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08183-105">Crée un identificateur d’entrée composé pour un objet, généralement un message dans une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="08183-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08183-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="08183-106">Header file:</span></span>  <br/> |<span data-ttu-id="08183-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="08183-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="08183-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="08183-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="08183-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="08183-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="08183-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="08183-110">Called by:</span></span>  <br/> |<span data-ttu-id="08183-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="08183-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a><span data-ttu-id="08183-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08183-112">Parameters</span></span>

 <span data-ttu-id="08183-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="08183-113">_psession_</span></span>
  
> <span data-ttu-id="08183-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="08183-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="08183-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="08183-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="08183-116">[in] Taille, en octets, de la clé d’enregistrement de la boutique de messages qui détient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="08183-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="08183-117">Si zéro est transmis dans le paramètre  _cbStoreRecordKey,_ le paramètre  _ppEID_ pointe vers une copie de l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08183-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="08183-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="08183-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="08183-119">[in] Pointeur vers la clé d’enregistrement de la magasin de messages qui contient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="08183-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="08183-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="08183-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="08183-121">[in] Taille, en octets, de l’identificateur d’entrée du message ou d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="08183-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="08183-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="08183-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="08183-123">[in] Pointeur vers l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08183-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="08183-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="08183-124">_pcbEID_</span></span>
  
> <span data-ttu-id="08183-125">[out] Pointeur vers la taille, en octets, de l’identificateur renvoyé.</span><span class="sxs-lookup"><span data-stu-id="08183-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="08183-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="08183-126">_ppEID_</span></span>
  
> <span data-ttu-id="08183-127">[out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyé.</span><span class="sxs-lookup"><span data-stu-id="08183-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="08183-128">Si la valeur du paramètre  _cbStoreRecordKey_ est supérieure à zéro, le paramètre  _ppEID_ pointe vers un pointeur vers l’identificateur d’entrée composé créé.</span><span class="sxs-lookup"><span data-stu-id="08183-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="08183-129">Si  _cbStoreRecordKey_ est zéro,  _ppEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08183-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08183-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="08183-130">Return value</span></span>

<span data-ttu-id="08183-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="08183-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08183-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="08183-132">Remarks</span></span>

<span data-ttu-id="08183-133">Si le message ou un autre objet pour lequel l’identificateur d’entrée composée est créé réside dans une magasin de messages, l’identificateur est créé à partir de l’identificateur d’entrée de l’objet et de la clé d’enregistrement de la boutique.</span><span class="sxs-lookup"><span data-stu-id="08183-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="08183-134">Si l’objet ne se trouve pas dans une banque, c’est-à-dire, si le nombre d’bytes pour la clé d’enregistrement de la banque transmise dans  _cbStoreRecordKey_ est zéro, l’identificateur d’entrée de l’objet est simplement copié.</span><span class="sxs-lookup"><span data-stu-id="08183-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="08183-135">La **fonction HrComposeEID** permet aux applications de travailler avec des objets dans plusieurs magasins via l’utilisation d’identificateurs d’entrée composés.</span><span class="sxs-lookup"><span data-stu-id="08183-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="08183-136">Une application peut appeler la [fonction HrDecomposeEID](hrdecomposeeid.md) pour fractionner l’identificateur d’entrée composé en ses constituants d’origine.</span><span class="sxs-lookup"><span data-stu-id="08183-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08183-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08183-137">See also</span></span>



[<span data-ttu-id="08183-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="08183-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="08183-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="08183-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

