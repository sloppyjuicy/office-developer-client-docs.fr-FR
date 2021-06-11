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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409208"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="8e031-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="8e031-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="8e031-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e031-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e031-105">Convertit l’identificateur d’entrée interne d’une boutique de messages en un identificateur d’entrée plus utilisable par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8e031-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e031-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8e031-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e031-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e031-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8e031-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8e031-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8e031-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8e031-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8e031-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8e031-110">Called by:</span></span>  <br/> |<span data-ttu-id="8e031-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="8e031-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8e031-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e031-112">Parameters</span></span>

 <span data-ttu-id="8e031-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e031-113">_ulFlags_</span></span>
  
> <span data-ttu-id="8e031-114">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="8e031-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="8e031-115">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="8e031-115">The following flag can be set:</span></span>
    
<span data-ttu-id="8e031-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e031-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8e031-117">Les chaînes sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e031-117">The strings are in Unicode format.</span></span> <span data-ttu-id="8e031-118">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="8e031-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="8e031-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="8e031-119">_szDLLName_</span></span>
  
> <span data-ttu-id="8e031-120">[in] Nom de la DLL du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="8e031-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="8e031-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="8e031-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="8e031-122">[in] Taille, en octets, de l’identificateur d’entrée d’origine de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="8e031-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="8e031-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="8e031-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="8e031-124">[in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="8e031-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="8e031-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="8e031-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="8e031-126">[out] Pointeur vers la taille, en octets, du nouvel identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8e031-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="8e031-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="8e031-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="8e031-128">[out] Pointeur vers un pointeur vers une structure **ENTRYID** qui contient le nouvel identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8e031-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e031-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e031-129">Return value</span></span>

<span data-ttu-id="8e031-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8e031-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e031-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e031-131">Remarks</span></span>

<span data-ttu-id="8e031-132">Un objet de magasin de messages conserve un identificateur d’entrée interne qui n’est significatif que pour les fournisseurs de services coresident avec cette magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="8e031-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="8e031-133">Pour les autres composants de messagerie, MAPI fournit une version wrapped de l’identificateur d’entrée interne qui la rend reconnaissable car elle appartient à la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="8e031-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="8e031-134">Les fournisseurs de services Coresident doivent toujours se faire donner l’identificateur d’entrée de magasin de messages d’origine non enveloppé ; les applications clientes doivent toujours avoir la version wrapped, qui est ensuite utilisable n’importe où dans le domaine de messagerie et dans d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="8e031-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="8e031-135">Un fournisseur de services peut encapsuler un identificateur d’entrée de magasin de messages à l’aide de la fonction **WrapStoreEntryID** ou de la méthode [IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) qui appelle la fonction **WrapStoreEntryID.**</span><span class="sxs-lookup"><span data-stu-id="8e031-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="8e031-136">Le fournisseur doit encapsuler l’identificateur d’entrée lors de l’exposition de la propriété **PR_ENTRYID (** [PidTagEntryId](pidtagentryid-canonical-property.md)) de la boutique de messages ou de son écriture dans une section de profil, et lors de l’exposition de la propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e031-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="8e031-137">MAPI encapsule un identificateur d’entrée de magasin de messages lors de la réponse à un appel [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="8e031-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="8e031-138">Lorsqu’une application cliente transmet un identificateur d’entrée de magasin de messages enveloppé à MAPI, par exemple dans un appel [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI démasque l’identificateur d’entrée avant de l’utiliser pour appeler une méthode de fournisseur telle que [IMSProvider::Logon](imsprovider-logon.md) ou [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

