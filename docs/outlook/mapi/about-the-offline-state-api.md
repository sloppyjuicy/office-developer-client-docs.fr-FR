---
title: À propos de l’API d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321783"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="d8f15-103">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d8f15-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="d8f15-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8f15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8f15-105">L'API d'État hors connexion prend en charge les rappels indiquant les modifications apportées à l'état de connexion d'un utilisateur dans Microsoft Outlook 2013 et Microsoft Outlook 2010, par exemple en étant en ligne dans Outlook 2013 ou Outlook 2010 en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d8f15-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="d8f15-106">L'API utilise un objet hors connexion global dans Outlook 2013 ou Outlook 2010 pour suivre les modifications apportées à un profil de compte d'utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="d8f15-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="d8f15-107">La notification est la seule forme de rappel prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d8f15-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="d8f15-108">En tant que clients de cette API, les fournisseurs de messagerie qui souhaitent être avertis de ces changements d'état de connexion effectuent les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="d8f15-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="d8f15-109">Implémenter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8f15-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="d8f15-110">Ouvrez un objet hors connexion existant pour un profil spécifique à l'aide de **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8f15-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="d8f15-111">Déterminez si l'objet peut fournir des notifications en ligne ou hors ligne à l'aide de **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8f15-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="d8f15-112">Inscrivez l'objet pour les notifications en ligne ou hors connexion à l'aide de **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8f15-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="d8f15-113">Les fournisseurs de messagerie peuvent désormais recevoir des notifications qu'Outlook 2013 ou Outlook 2010 envoient à l'aide de **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="d8f15-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="d8f15-114">Lors de l'arrêt, supprimez l'inscription pour les notifications en ligne et hors connexion à l'aide de **[IMAPIOfflineMgr::](imapiofflinemgr-unadvise.md)** Unadvise.</span><span class="sxs-lookup"><span data-stu-id="d8f15-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d8f15-115">En règle générale, Outlook 2013 et Outlook 2010 peuvent informer un client des modifications en ligne/hors connexion, ainsi que d'autres modifications, mais l'API d'État hors connexion prend en charge uniquement les notifications pour les modifications en ligne et hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d8f15-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="d8f15-116">Le client doit ignorer toutes les autres notifications.</span><span class="sxs-lookup"><span data-stu-id="d8f15-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="d8f15-117">Pour plus d'informations, voir **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** et **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="d8f15-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="d8f15-118">Pour obtenir un exemple de client qui utilise l'API d'État hors connexion, voir [à propos de l'exemple de complément d'État hors connexion](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d8f15-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="d8f15-119">L'exemple de complément d'État hors connexion est un complément COM qui utilise l'API d'État hors connexion pour surveiller et modifier l'état de connexion.</span><span class="sxs-lookup"><span data-stu-id="d8f15-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="d8f15-120">Cette API fournit les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="d8f15-120">This API provides the following:</span></span>
  
<span data-ttu-id="d8f15-121">Définitions :</span><span class="sxs-lookup"><span data-stu-id="d8f15-121">Definitions:</span></span>
  
- [<span data-ttu-id="d8f15-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d8f15-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="d8f15-123">Types de données:</span><span class="sxs-lookup"><span data-stu-id="d8f15-123">Data types:</span></span>
  
- <span data-ttu-id="d8f15-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="d8f15-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="d8f15-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="d8f15-127">Fonctions :</span><span class="sxs-lookup"><span data-stu-id="d8f15-127">Functions:</span></span>
  
- <span data-ttu-id="d8f15-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="d8f15-129">Interfaces :</span><span class="sxs-lookup"><span data-stu-id="d8f15-129">Interfaces:</span></span>
  
- <span data-ttu-id="d8f15-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="d8f15-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="d8f15-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f15-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

