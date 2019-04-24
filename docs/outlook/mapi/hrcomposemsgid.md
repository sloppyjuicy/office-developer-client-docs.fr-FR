---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348047"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="8dc6e-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="8dc6e-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="8dc6e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dc6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dc6e-105">Crée une chaîne ASCII représentant un identificateur d'entrée composée pour un objet, généralement un message dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8dc6e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8dc6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="8dc6e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8dc6e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8dc6e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8dc6e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8dc6e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8dc6e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8dc6e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8dc6e-110">Called by:</span></span>  <br/> |<span data-ttu-id="8dc6e-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="8dc6e-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="8dc6e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8dc6e-112">Parameters</span></span>

 <span data-ttu-id="8dc6e-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-113">_psession_</span></span>
  
> <span data-ttu-id="8dc6e-114">dans Pointeur vers la session en cours d'utilisation par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="8dc6e-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="8dc6e-116">dans Taille, en octets, de la clé d'enregistrement de la Banque de messages qui contient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="8dc6e-117">Si la valeur zéro est transmise au paramètre _cbStoreRecordKey_ , le paramètre _pszMsgID_ pointe vers une copie de l'identificateur d'entrée converti en texte.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="8dc6e-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="8dc6e-119">dans Pointeur vers la clé d'enregistrement de la Banque de messages qui contient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="8dc6e-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="8dc6e-121">dans Taille, en octets, de l'identificateur d'entrée du message ou d'un autre objet.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="8dc6e-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="8dc6e-123">dans Pointeur vers l'identificateur d'entrée de l'objet.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="8dc6e-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="8dc6e-125">remarquer Pointeur vers la chaîne ASCII renvoyée.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="8dc6e-126">Si le paramètre _cbStoreRecordKey_ est supérieur à zéro, le paramètre _pszMsgID_ pointe vers un identificateur d'entrée composé converti en texte.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="8dc6e-127">Si _cbStoreRecordKey_ est égal à zéro, _pszMsgID_ pointe vers un identificateur d'entrée non composé converti en texte.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8dc6e-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8dc6e-128">Return value</span></span>

<span data-ttu-id="8dc6e-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8dc6e-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="8dc6e-130">Remarks</span></span>

<span data-ttu-id="8dc6e-131">Si le message ou un autre objet pour lequel l'identificateur d'entrée composé est créé réside dans une banque de messages, la chaîne de l'identificateur est créée à partir de l'identificateur d'entrée de l'objet et de la clé d'enregistrement de la Banque.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="8dc6e-132">Si l'objet n'est pas dans un magasin, autrement dit, si le nombre d'octets pour la clé d'enregistrement passée dans le paramètre _cbStoreRecordKey_ est égal à zéro, l'identificateur d'entrée de l'objet est simplement copié et converti en chaîne.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="8dc6e-133">L'appel de la fonction **HrComposeMsgID** équivaut à l'appel de la fonction [HrComposeEID](hrcomposeeid.md) , puis à la fonction [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="8dc6e-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="8dc6e-134">**HrComposeMsgID** permet aux applications clientes de fonctionner avec des objets dans plusieurs magasins par le biais de l'utilisation d'identificateurs d'entrée composés.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="8dc6e-135">Une application peut appeler la fonction [HrDecomposeMsgID](hrdecomposemsgid.md) pour fractionner l'identificateur d'entrée composée en ses composants d'origine.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

