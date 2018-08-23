---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565094"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="7fb9d-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="7fb9d-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="7fb9d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fb9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fb9d-105">Fournit des informations à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** pour enregistrer le rappel pour un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7fb9d-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7fb9d-106">Quick info</span></span>

<span data-ttu-id="7fb9d-107">Voir **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a><span data-ttu-id="7fb9d-108">Members</span><span class="sxs-lookup"><span data-stu-id="7fb9d-108">Members</span></span>

<span data-ttu-id="7fb9d-109">_ulSize_: la taille de **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="7fb9d-110">_ulClientToken_: un jeton défini par le client sur un rappel.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="7fb9d-111">Il est membre de la structure **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** transmis à **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** *ulClientToken* .</span><span class="sxs-lookup"><span data-stu-id="7fb9d-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="7fb9d-112">_CallbackType_: Type de rappel à effectuer.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="7fb9d-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="7fb9d-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="7fb9d-114">Le type de rappel est par notification.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-114">The type of callback is by notification.</span></span> <span data-ttu-id="7fb9d-115">Il s’agit du seul type pris en charge de rappel.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="7fb9d-116">*pCallback* doit indiquer l’interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="7fb9d-117">_pCallback_: Interface à utiliser pour le rappel.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="7fb9d-118">Il s’agit d’implémentation du client de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="7fb9d-119">_ulAdviseTypes_: les types de notifications, tels qu’identifiés par la condition pour conseiller.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="7fb9d-120">Le seul type pris en charge est MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="7fb9d-121">_ulStateMask_: le seul état pris en charge est MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="7fb9d-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fb9d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fb9d-122">See also</span></span>

- [<span data-ttu-id="7fb9d-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="7fb9d-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="7fb9d-124">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="7fb9d-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="7fb9d-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7fb9d-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="7fb9d-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="7fb9d-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

