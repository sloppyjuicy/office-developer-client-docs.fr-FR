---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783890"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="43451-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="43451-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="43451-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43451-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43451-105">Envoie des notifications au client sur les modifications de l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="43451-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="43451-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43451-106">Parameters</span></span>

 <span data-ttu-id="43451-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="43451-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="43451-108">[in] La notification qui envoie au client Outlook.</span><span class="sxs-lookup"><span data-stu-id="43451-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="43451-109">La notification indique la partie de l’état de connexion qui a été modifié, l’état de connexion ancien et le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="43451-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43451-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="43451-110">Remarks</span></span>

<span data-ttu-id="43451-111">Outlook utilise cette méthode pour envoyer les rappels de notification à un client.</span><span class="sxs-lookup"><span data-stu-id="43451-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="43451-112">Pour que cette interface disponible pour Microsoft Outlook 2010 ou Microsoft Outlook 2013, le client doit implémenter cette interface et lui passer un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lorsque vous configurez des rappels à l’aide de **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="43451-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="43451-113">Le client transfère également à **MAPIOFFLINE_ADVISEINFO** un jeton client que Outlook 2010 ou Outlook 2013 utilise **IMAPIOfflineNotify::Notify** pour identifier le client enregistré pour le rappel de notification.</span><span class="sxs-lookup"><span data-stu-id="43451-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="43451-114">En règle générale, Outlook 2010 et Outlook 2013 peuvent informer un client de modifications en ligne/hors connexion et les autres changements d’état de connexion, mais l’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion.</span><span class="sxs-lookup"><span data-stu-id="43451-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="43451-115">Le client doit ignorer toutes les autres notifications.</span><span class="sxs-lookup"><span data-stu-id="43451-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43451-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43451-116">See also</span></span>



[<span data-ttu-id="43451-117">À propos de l’API d’état en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="43451-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="43451-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="43451-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

