---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585135"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="43a15-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="43a15-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="43a15-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43a15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43a15-105">Convertit un identificateur d’entrée plus conviviaux identificateur d’entrée interne d’une banque de messages par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="43a15-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="43a15-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="43a15-106">Header file:</span></span>  <br/> |<span data-ttu-id="43a15-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43a15-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="43a15-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="43a15-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="43a15-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="43a15-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="43a15-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="43a15-110">Called by:</span></span>  <br/> |<span data-ttu-id="43a15-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="43a15-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="43a15-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="43a15-112">Parameters</span></span>

 <span data-ttu-id="43a15-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43a15-113">_ulFlags_</span></span>
  
> <span data-ttu-id="43a15-114">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="43a15-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="43a15-115">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="43a15-115">The following flag can be set:</span></span>
    
<span data-ttu-id="43a15-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43a15-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="43a15-117">Les chaînes sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="43a15-117">The strings are in Unicode format.</span></span> <span data-ttu-id="43a15-118">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="43a15-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="43a15-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="43a15-119">_szDLLName_</span></span>
  
> <span data-ttu-id="43a15-120">[in] Nom de la DLL du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="43a15-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="43a15-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="43a15-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="43a15-122">[in] Taille, en octets, de l’identificateur d’entrée d’origine pour la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="43a15-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="43a15-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="43a15-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="43a15-124">[in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="43a15-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="43a15-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="43a15-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="43a15-126">[out] Pointeur vers la taille, en octets, de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="43a15-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="43a15-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="43a15-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="43a15-128">[out] Pointeur vers un pointeur vers une structure **ENTRYID** qui contient l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="43a15-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="43a15-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="43a15-129">Return value</span></span>

<span data-ttu-id="43a15-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="43a15-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43a15-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="43a15-131">Remarks</span></span>

<span data-ttu-id="43a15-132">Objet store message conserve un identificateur d’entrée interne qui est uniquement explicite pour coresident de fournisseurs de service avec cette banque d’informations.</span><span class="sxs-lookup"><span data-stu-id="43a15-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="43a15-133">Pour les autres composants de messagerie MAPI fournit une version renvoyé à la ligne de l’identificateur d’entrée interne qui rend reconnaissable qui appartiennent à la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="43a15-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="43a15-134">Fournisseurs de services coresident doivent toujours être donnés à l’identificateur d’entrée non message magasin d’origine ; applications clientes doivent toujours être données à la version encapsulée, qui est alors utilisable n’importe où dans le domaine de messagerie et dans d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="43a15-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="43a15-135">Un fournisseur de services peut renvoyer un identificateur d’entrée de magasin de message à l’aide de la fonction **WrapStoreEntryID** ou la méthode [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , qui appelle la fonction **WrapStoreEntryID** .</span><span class="sxs-lookup"><span data-stu-id="43a15-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="43a15-136">Le fournisseur doit encapsuler l’identificateur d’entrée lors de l’exposition **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la banque de messages propriété ou l’écriture dans une section de profil et lors de l’exposition de la **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) propriété.</span><span class="sxs-lookup"><span data-stu-id="43a15-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="43a15-137">MAPI encapsule un identificateur d’entrée de magasin de message lors de la réponse à un appel [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="43a15-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="43a15-138">Lorsqu’une application cliente transmet un identificateur d’entrée de magasin de message encapsulé à MAPI, par exemple dans un appel [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI Désencapsule l’identificateur d’entrée avant de les utiliser pour appeler une méthode de fournisseur telles que [IMSProvider::Logon](imsprovider-logon.md) ou [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="43a15-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

