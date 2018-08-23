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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3bcad4c236f71390f7a048eb66860720e9180e06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582041"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="c6caa-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="c6caa-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="c6caa-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6caa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6caa-105">Crée une chaîne ASCII qui représente un identificateur d’entrée composée d’un objet, généralement un message dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c6caa-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6caa-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c6caa-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6caa-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c6caa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c6caa-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="c6caa-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c6caa-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c6caa-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c6caa-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="c6caa-110">Called by:</span></span>  <br/> |<span data-ttu-id="c6caa-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="c6caa-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c6caa-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6caa-112">Parameters</span></span>

 <span data-ttu-id="c6caa-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="c6caa-113">_psession_</span></span>
  
> <span data-ttu-id="c6caa-114">[in] Pointeur vers la session en cours d’utilisation par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="c6caa-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="c6caa-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="c6caa-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="c6caa-116">[in] Taille, en octets, de la clé d’enregistrement de la banque de messages qui contient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="c6caa-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="c6caa-117">Si la valeur zéro est transmise dans le paramètre _cbStoreRecordKey_ , le paramètre _pszMsgID_ pointe vers une copie de l’identificateur d’entrée est converti en texte.</span><span class="sxs-lookup"><span data-stu-id="c6caa-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="c6caa-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="c6caa-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="c6caa-119">[in] Pointeur vers la clé d’enregistrement de la banque de messages qui contient le message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="c6caa-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="c6caa-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="c6caa-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="c6caa-121">[in] Taille, en octets, de l’identificateur d’entrée du message ou un autre objet.</span><span class="sxs-lookup"><span data-stu-id="c6caa-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="c6caa-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="c6caa-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="c6caa-123">[in] Pointeur vers l’identificateur d’entrée de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c6caa-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="c6caa-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="c6caa-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="c6caa-125">[out] Pointeur vers la chaîne retournée ASCII.</span><span class="sxs-lookup"><span data-stu-id="c6caa-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="c6caa-126">Si le paramètre _cbStoreRecordKey_ est supérieur à zéro, le paramètre _pszMsgID_ pointe vers un identificateur d’entrée composés convertis en texte.</span><span class="sxs-lookup"><span data-stu-id="c6caa-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="c6caa-127">Si _cbStoreRecordKey_ est égale à zéro, points _pszMsgID_ à un identificateur d’entrée non composés convertis en texte.</span><span class="sxs-lookup"><span data-stu-id="c6caa-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6caa-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c6caa-128">Return value</span></span>

<span data-ttu-id="c6caa-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c6caa-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6caa-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6caa-130">Remarks</span></span>

<span data-ttu-id="c6caa-131">Si le message ou un autre objet pour lequel l’identificateur d’entrée composés est en cours de création se trouve dans une banque de messages, la chaîne d’identificateur est créée à partir d’identificateur d’entrée de l’objet et la clé d’enregistrement du magasin.</span><span class="sxs-lookup"><span data-stu-id="c6caa-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="c6caa-132">Si l’objet n’est pas dans une banque, autrement dit, si le nombre d’octets pour la clé d’enregistrement magasin passé dans le paramètre _cbStoreRecordKey_ est égale à zéro, identificateur d’entrée de l’objet est simplement copié et converti en une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c6caa-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="c6caa-133">La fonction **HrComposeMsgID** équivaut à appeler la fonction [HrComposeEID](hrcomposeeid.md) , puis la fonction [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="c6caa-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="c6caa-134">**HrComposeMsgID** permet aux applications de client travailler avec des objets dans plusieurs magasins à l’aide d’identificateurs d’entrée composés.</span><span class="sxs-lookup"><span data-stu-id="c6caa-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="c6caa-135">Une application peut appeler la fonction [HrDecomposeMsgID](hrdecomposemsgid.md) pour fractionner l’identificateur d’entrée composés en ses composants d’origine.</span><span class="sxs-lookup"><span data-stu-id="c6caa-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

