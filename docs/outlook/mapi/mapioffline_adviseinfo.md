---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270034"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="7f114-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="7f114-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="7f114-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f114-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f114-105">Fournit des informations à **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** pour inscrire le rappel pour un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7f114-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7f114-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7f114-106">Quick info</span></span>

<span data-ttu-id="7f114-107">Voir **IMAPIOfflineMgr:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="7f114-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="7f114-108">Members</span><span class="sxs-lookup"><span data-stu-id="7f114-108">Members</span></span>

<span data-ttu-id="7f114-109">_ulSize_: taille de **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="7f114-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="7f114-110">_ulClientToken_: jeton défini par le client à propos d'un rappel.</span><span class="sxs-lookup"><span data-stu-id="7f114-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="7f114-111">Il s'agit du membre *ulClientToken* de la structure **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** transmis à **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="7f114-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="7f114-112">_CallbackType_: type de rappel à effectuer.</span><span class="sxs-lookup"><span data-stu-id="7f114-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="7f114-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="7f114-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="7f114-114">Le type de rappel est par notification.</span><span class="sxs-lookup"><span data-stu-id="7f114-114">The type of callback is by notification.</span></span> <span data-ttu-id="7f114-115">Il s'agit du seul type de rappel pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7f114-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="7f114-116">*pCallback* doit indiquer l'interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="7f114-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="7f114-117">_pCallback_: interface à utiliser pour le rappel.</span><span class="sxs-lookup"><span data-stu-id="7f114-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="7f114-118">Il s'agit de l'implémentation du client de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="7f114-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="7f114-119">_ulAdviseTypes_: type de notification, tel qu'identifié par la condition pour conseiller.</span><span class="sxs-lookup"><span data-stu-id="7f114-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="7f114-120">Le seul type pris en charge est MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="7f114-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="7f114-121">_ulStateMask_: le seul État pris en charge est MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="7f114-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f114-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f114-122">See also</span></span>

- [<span data-ttu-id="7f114-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="7f114-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="7f114-124">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="7f114-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="7f114-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7f114-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="7f114-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="7f114-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

