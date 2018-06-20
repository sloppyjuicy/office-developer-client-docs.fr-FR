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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783523"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="aed39-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="aed39-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="aed39-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aed39-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aed39-105">Crée un identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="aed39-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aed39-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="aed39-106">Header file:</span></span>  <br/> |<span data-ttu-id="aed39-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="aed39-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="aed39-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="aed39-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aed39-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aed39-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aed39-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="aed39-110">Called by:</span></span>  <br/> |<span data-ttu-id="aed39-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="aed39-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="aed39-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aed39-112">Parameters</span></span>

 <span data-ttu-id="aed39-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="aed39-113">_psession_</span></span>
  
> <span data-ttu-id="aed39-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="aed39-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="aed39-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="aed39-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="aed39-116">[in] Taille, en octets, de la clé d’enregistrement de la banque de message contenant le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="aed39-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="aed39-117">Si la valeur zéro est transmise dans le paramètre _cbStoreRecordKey_ , le paramètre _ppEID_ pointe vers une copie de l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aed39-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="aed39-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="aed39-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="aed39-119">[in] Pointeur vers la clé d’enregistrement de la banque de messages qui contient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="aed39-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="aed39-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="aed39-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="aed39-121">[in] Taille, en octets, de l’identificateur d’entrée du message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="aed39-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="aed39-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="aed39-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="aed39-123">[in] Pointeur vers l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aed39-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="aed39-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="aed39-124">_pcbEID_</span></span>
  
> <span data-ttu-id="aed39-125">[out] Pointeur vers la taille, en octets, de l’identificateur retourné.</span><span class="sxs-lookup"><span data-stu-id="aed39-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="aed39-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="aed39-126">_ppEID_</span></span>
  
> <span data-ttu-id="aed39-127">[out] Pointeur vers un pointeur vers l’identificateur d’entrée renvoyée.</span><span class="sxs-lookup"><span data-stu-id="aed39-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="aed39-128">Si la valeur du paramètre _cbStoreRecordKey_ est supérieure à zéro, le paramètre _ppEID_ pointe vers un pointeur vers l’identificateur d’entrée composés qui est créé.</span><span class="sxs-lookup"><span data-stu-id="aed39-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="aed39-129">Si _cbStoreRecordKey_ est égale à zéro, _ppEID_ pointe vers un pointeur vers une copie de l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aed39-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aed39-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aed39-130">Return value</span></span>

<span data-ttu-id="aed39-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aed39-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aed39-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="aed39-132">Remarks</span></span>

<span data-ttu-id="aed39-133">Si le message ou un autre objet pour lequel l’identificateur d’entrée composés est en cours de création se trouve dans une banque de messages, l’identificateur est créé à partir d’identificateur d’entrée de l’objet et la clé d’enregistrement du magasin.</span><span class="sxs-lookup"><span data-stu-id="aed39-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="aed39-134">Si l’objet n’est pas dans une banque, autrement dit, si le nombre d’octets pour la clé d’enregistrement magasin passé _cbStoreRecordKey_ est égale à zéro, identificateur d’entrée de l’objet est simplement copié.</span><span class="sxs-lookup"><span data-stu-id="aed39-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="aed39-135">La fonction **HrComposeEID** permet aux applications de travailler avec des objets dans des magasins de plusieurs identificateurs d’entrée composés grâce à l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="aed39-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="aed39-136">Une application peut appeler la fonction [HrDecomposeEID](hrdecomposeeid.md) pour fractionner l’identificateur d’entrée composés en ses composants d’origine.</span><span class="sxs-lookup"><span data-stu-id="aed39-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aed39-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aed39-137">See also</span></span>



[<span data-ttu-id="aed39-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="aed39-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="aed39-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="aed39-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

