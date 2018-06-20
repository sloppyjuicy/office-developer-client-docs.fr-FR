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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aff46cca7a7d530b2eede1790176058e3b91abc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787475"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="0d7e2-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="0d7e2-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="0d7e2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d7e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d7e2-105">Convertit un identificateur d’entrée plus conviviaux identificateur d’entrée interne d’une banque de messages par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d7e2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0d7e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d7e2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d7e2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0d7e2-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="0d7e2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d7e2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d7e2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d7e2-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="0d7e2-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d7e2-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0d7e2-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0d7e2-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="0d7e2-112">Parameters</span></span>

 <span data-ttu-id="0d7e2-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d7e2-113">_ulFlags_</span></span>
  
> <span data-ttu-id="0d7e2-114">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="0d7e2-115">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="0d7e2-115">The following flag can be set:</span></span>
    
<span data-ttu-id="0d7e2-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d7e2-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0d7e2-117">Les chaînes sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-117">The strings are in Unicode format.</span></span> <span data-ttu-id="0d7e2-118">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0d7e2-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="0d7e2-119">_szDLLName_</span></span>
  
> <span data-ttu-id="0d7e2-120">[in] Nom de la DLL du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="0d7e2-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="0d7e2-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="0d7e2-122">[in] Taille, en octets, de l’identificateur d’entrée d’origine pour la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="0d7e2-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="0d7e2-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="0d7e2-124">[in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="0d7e2-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="0d7e2-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="0d7e2-126">[out] Pointeur vers la taille, en octets, de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="0d7e2-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="0d7e2-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="0d7e2-128">[out] Pointeur vers un pointeur vers une structure **ENTRYID** qui contient l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d7e2-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d7e2-129">Return value</span></span>

<span data-ttu-id="0d7e2-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d7e2-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d7e2-131">Remarks</span></span>

<span data-ttu-id="0d7e2-132">Objet store message conserve un identificateur d’entrée interne qui est uniquement explicite pour coresident de fournisseurs de service avec cette banque d’informations.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="0d7e2-133">Pour les autres composants de messagerie MAPI fournit une version renvoyé à la ligne de l’identificateur d’entrée interne qui rend reconnaissable qui appartiennent à la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="0d7e2-134">Fournisseurs de services coresident doivent toujours être donnés à l’identificateur d’entrée non message magasin d’origine ; applications clientes doivent toujours être données à la version encapsulée, qui est alors utilisable n’importe où dans le domaine de messagerie et dans d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="0d7e2-135">Un fournisseur de services peut renvoyer un identificateur d’entrée de magasin de message à l’aide de la fonction **WrapStoreEntryID** ou la méthode [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , qui appelle la fonction **WrapStoreEntryID** .</span><span class="sxs-lookup"><span data-stu-id="0d7e2-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="0d7e2-136">Le fournisseur doit encapsuler l’identificateur d’entrée lors de l’exposition **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la banque de messages propriété ou l’écriture dans une section de profil et lors de l’exposition de la **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) propriété.</span><span class="sxs-lookup"><span data-stu-id="0d7e2-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0d7e2-137">MAPI encapsule un identificateur d’entrée de magasin de message lors de la réponse à un appel [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="0d7e2-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="0d7e2-138">Lorsqu’une application cliente transmet un identificateur d’entrée de magasin de message encapsulé à MAPI, par exemple dans un appel [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI Désencapsule l’identificateur d’entrée avant de les utiliser pour appeler une méthode de fournisseur telles que [IMSProvider::Logon](imsprovider-logon.md) ou [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="0d7e2-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

