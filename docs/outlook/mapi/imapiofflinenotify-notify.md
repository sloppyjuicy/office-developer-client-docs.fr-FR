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
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410692"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="25a90-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="25a90-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="25a90-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25a90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25a90-105">Envoie des notifications au client concernant les modifications apportées à l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="25a90-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="25a90-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="25a90-106">Parameters</span></span>

 <span data-ttu-id="25a90-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="25a90-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="25a90-108">[in] Notification Outlook au client.</span><span class="sxs-lookup"><span data-stu-id="25a90-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="25a90-109">La notification indique la partie de l’état de connexion qui a changé, l’ancien état de connexion et le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="25a90-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25a90-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="25a90-110">Remarks</span></span>

<span data-ttu-id="25a90-111">Outlook utilise cette méthode pour envoyer des rappels de notification à un client.</span><span class="sxs-lookup"><span data-stu-id="25a90-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="25a90-112">Pour rendre cette interface disponible pour Microsoft Outlook 2010 ou Microsoft Outlook 2013, le client doit implémenter cette interface et lui transmettre un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lors de la configuration des rappels à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="25a90-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="25a90-113">Le client passe également à **MAPIOFFLINE_ADVISEINFO** un jeton client que Outlook 2010 ou Outlook 2013 utilise dans **IMAPIOfflineNotify::Notify** pour identifier le client inscrit pour le rappel de notification.</span><span class="sxs-lookup"><span data-stu-id="25a90-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="25a90-114">En règle générale, Outlook 2010 et Outlook 2013 peuvent notifier un client de modifications en ligne/hors connexion et d’autres modifications d’état de connexion, mais l’API d’état hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion.</span><span class="sxs-lookup"><span data-stu-id="25a90-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="25a90-115">Le client doit ignorer toutes les autres notifications.</span><span class="sxs-lookup"><span data-stu-id="25a90-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25a90-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25a90-116">See also</span></span>



[<span data-ttu-id="25a90-117">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="25a90-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="25a90-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="25a90-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

