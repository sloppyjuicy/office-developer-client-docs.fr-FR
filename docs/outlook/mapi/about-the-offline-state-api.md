---
title: À propos de l’API d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: aa30a173251193d74d6560c8dce2663463a18e36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565983"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="f657f-103">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="f657f-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="f657f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f657f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f657f-105">L’API d’état en mode hors connexion prend en charge les rappels indiquant les modifications de l’état de connexion d’un utilisateur dans Microsoft Outlook 2013 et Microsoft Outlook 2010 — par exemple, d’en cours en ligne dans Outlook 2013 ou Outlook 2010 pour en cours en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f657f-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="f657f-106">L’API utilise un objet global en mode hors connexion dans Outlook 2013 ou Outlook 2010 pour le suivi des modifications pour un profil de compte d’utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="f657f-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="f657f-107">Notification est la seule forme prises en charge de rappel.</span><span class="sxs-lookup"><span data-stu-id="f657f-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="f657f-108">Comme des clients de cette API, les fournisseurs de messagerie qui vous souhaitez être averti de ces changements d’état de connexion procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f657f-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="f657f-109">Mettre en œuvre **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="f657f-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="f657f-110">Ouvrez un objet existant en mode hors connexion pour un profil spécifique à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="f657f-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="f657f-111">Déterminer si l’objet est en mesure de fournir des notifications en ligne ou hors connexion à l’aide de **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="f657f-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="f657f-112">Enregistrer l’objet pour les notifications en ligne ou hors connexion à l’aide de **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="f657f-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="f657f-113">Désormais, les fournisseurs de messagerie peuvent recevoir des notifications que Outlook 2013 ou Outlook 2010 envoyer à l’aide de **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="f657f-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="f657f-114">Lors de l’arrêt, supprimez l’enregistrement pour les notifications en ligne et hors connexion à l’aide de **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="f657f-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f657f-115">En règle générale, Outlook 2013 et Outlook 2010 peuvent informer un client de modifications en ligne/hors ligne ainsi que d’autres modifications, mais l’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f657f-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="f657f-116">Le client doit ignorer toutes les autres notifications.</span><span class="sxs-lookup"><span data-stu-id="f657f-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="f657f-117">Pour plus d’informations, voir **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** et **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="f657f-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="f657f-118">Pour obtenir un exemple d’un client qui utilise l’API de l’état en mode hors connexion, consultez la rubrique [sur l’exemple en mode hors connexion état Add-in](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="f657f-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="f657f-119">Le complément exemple hors connexion état est un complément COM qui utilise l’API de l’état en mode hors connexion pour surveiller et modifier l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="f657f-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="f657f-120">Cette API fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="f657f-120">This API provides the following:</span></span>
  
<span data-ttu-id="f657f-121">Définitions :</span><span class="sxs-lookup"><span data-stu-id="f657f-121">Definitions:</span></span>
  
- [<span data-ttu-id="f657f-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f657f-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="f657f-123">Types de données :</span><span class="sxs-lookup"><span data-stu-id="f657f-123">Data types:</span></span>
  
- <span data-ttu-id="f657f-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="f657f-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="f657f-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="f657f-127">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="f657f-127">Functions:</span></span>
  
- <span data-ttu-id="f657f-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="f657f-129">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="f657f-129">Interfaces:</span></span>
  
- <span data-ttu-id="f657f-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="f657f-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="f657f-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f657f-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

