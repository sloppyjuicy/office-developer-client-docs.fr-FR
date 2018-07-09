---
title: L’initialisation de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784333"
---
# <a name="initializing-mapi"></a><span data-ttu-id="038d8-103">L’initialisation de MAPI</span><span class="sxs-lookup"><span data-stu-id="038d8-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="038d8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="038d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="038d8-105">Toutes les applications clientes qui utilisent les bibliothèques MAPI doivent appeler la fonction **exécuter MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="038d8-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="038d8-106">Pour plus d’informations, voir [exécuter MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="038d8-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="038d8-107">**Exécuter MAPIInitialize** initialise les données globales pour la session et prépare les bibliothèques d’accepter les appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="038d8-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="038d8-108">Il existe quelques indicateurs qui sont importantes pour définir dans certaines situations :</span><span class="sxs-lookup"><span data-stu-id="038d8-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="038d8-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="038d8-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="038d8-110">Définir l’indicateur MAPI_NT_SERVICE si votre client est implémentée comme un service Windows.</span><span class="sxs-lookup"><span data-stu-id="038d8-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="038d8-111">Si votre client est un service Windows et vous ne définissez pas cet indicateur, MAPI le reconnaît pas en tant que service.</span><span class="sxs-lookup"><span data-stu-id="038d8-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="038d8-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="038d8-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="038d8-113">L’indicateur MAPI_MULTITHREAD_NOTIFICATIONS se rapporte à comment MAPI gère les notifications.</span><span class="sxs-lookup"><span data-stu-id="038d8-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="038d8-114">MAPI crée une fenêtre masquée qui reçoit les messages de fenêtre lorsque les modifications sont apportées à un objet de génération de notifications.</span><span class="sxs-lookup"><span data-stu-id="038d8-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="038d8-115">Les messages de fenêtre sont traités à un moment donné, à l’origine de l’envoi des notifications et les méthodes de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) appropriées à appeler.</span><span class="sxs-lookup"><span data-stu-id="038d8-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="038d8-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="038d8-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="038d8-117">Définir l’indicateur MAPI_NO_COINT pour pouvoir **exécuter MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](http://msdn.microsoft.com/fr-fr/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="038d8-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/fr-fr/library/ms886303.aspx).</span></span> <span data-ttu-id="038d8-118">Si une structure **MAPIINIT_0** est passée à **exécuter MAPIInitialize** avec _ulFlags_ défini sur MAPI_NO_COINIT, MAPI part du principe que COM a déjà été initialisé et ignorer l’appel à **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="038d8-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="038d8-119">Si l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS n’est pas transmise, MAPI crée la fenêtre de notification sur le thread qui a été utilisé pour votre premier appel **exécuter MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="038d8-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="038d8-120">MAPI crée la fenêtre de notification sur un thread distinct si MAPI_MULTITHREAD_NOTIFICATIONS est passé, un thread dédié à la gestion des notifications.</span><span class="sxs-lookup"><span data-stu-id="038d8-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="038d8-121">MAPI attend le thread qui est utilisé pour créer la fenêtre de notification masqué :</span><span class="sxs-lookup"><span data-stu-id="038d8-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="038d8-122">Avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="038d8-122">Have a message loop.</span></span>
    
- <span data-ttu-id="038d8-123">Ne pas bloquer pendant toute la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="038d8-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="038d8-124">Avoir une durée de vie plue que tout autre thread créé par votre client.</span><span class="sxs-lookup"><span data-stu-id="038d8-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="038d8-125">Vous pouvez choisir de thread qui est utilisé en définissant un indicateur dans le premier appel **exécuter MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="038d8-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="038d8-126">Le risque en autorisant un de vos threads pour gérer les notifications est que si le thread disparaît, la destruction de la fenêtre de notification et les notifications ne peuvent plus être envoyées à n’importe lequel de vos autres threads.</span><span class="sxs-lookup"><span data-stu-id="038d8-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="038d8-127">En outre, un traitement spécial peut être nécessaire pour contrôler la distribution des messages de notification qui sont publiés dans la file d’attente de messages de la fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="038d8-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="038d8-128">Si vous utilisez une fenêtre séparée pour gérer les notifications, être assuré que les notifications seront affiche au moment opportun sur une thread approprié.</span><span class="sxs-lookup"><span data-stu-id="038d8-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="038d8-129">Vous n’aurez pas de code spécial pour rechercher et traiter les messages Windows qui sont publiés dans la fenêtre de notification.</span><span class="sxs-lookup"><span data-stu-id="038d8-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="038d8-130">MAPI recommande les types suivants d’applications clientes d’utiliser un thread distinct pour créer la fenêtre masquée pour la prise en charge de la notification :</span><span class="sxs-lookup"><span data-stu-id="038d8-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="038d8-131">Tous les clients multithreads.</span><span class="sxs-lookup"><span data-stu-id="038d8-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="038d8-132">Applications de la console Windows services seul thread et Win32.</span><span class="sxs-lookup"><span data-stu-id="038d8-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="038d8-133">Un seul thread les clients qui n’ont pas besoin d’utiliser leur thread principale pour notification.</span><span class="sxs-lookup"><span data-stu-id="038d8-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="038d8-134">Pour utiliser l’approche de thread distinct, appelez **exécuter MAPIInitialize** sur chaque thread, l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="038d8-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="038d8-135">Uniquement d’un client premier appel à **exécuter MAPIInitialize** provoque une fenêtre masquée à créer pour prendre en charge les notifications.</span><span class="sxs-lookup"><span data-stu-id="038d8-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="038d8-136">Cause uniquement les appels suivants à incrémenter un décompte de références.</span><span class="sxs-lookup"><span data-stu-id="038d8-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

