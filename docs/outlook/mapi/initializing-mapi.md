---
title: Initialisation de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309729"
---
# <a name="initializing-mapi"></a><span data-ttu-id="93849-103">Initialisation de MAPI</span><span class="sxs-lookup"><span data-stu-id="93849-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="93849-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93849-105">Toutes les applications clientes qui utilisent les bibliothèques MAPI doivent appeler la **fonction MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="93849-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="93849-106">Pour plus d’informations, [voir MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="93849-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="93849-107">**MAPIInitialize** initialise les données globales de la session et prépare les bibliothèques MAPI à accepter les appels.</span><span class="sxs-lookup"><span data-stu-id="93849-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="93849-108">Quelques indicateurs sont importants à définir dans certaines situations :</span><span class="sxs-lookup"><span data-stu-id="93849-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="93849-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="93849-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="93849-110">Définissez l MAPI_NT_SERVICE si votre client est implémenté en tant que service Windows.</span><span class="sxs-lookup"><span data-stu-id="93849-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="93849-111">Si votre client est un service Windows et que vous ne définissez pas cet indicateur, MAPI ne le reconnaîtra pas en tant que service.</span><span class="sxs-lookup"><span data-stu-id="93849-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="93849-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="93849-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="93849-113">L MAPI_MULTITHREAD_NOTIFICATIONS de gestion des notifications est lié à la façon dont MAPI gère les notifications.</span><span class="sxs-lookup"><span data-stu-id="93849-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="93849-114">MAPI crée une fenêtre masquée qui reçoit des messages de fenêtre lorsque des modifications sont apportées à un objet générant des notifications.</span><span class="sxs-lookup"><span data-stu-id="93849-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="93849-115">Les messages de fenêtre sont traitées à un moment donné, ce qui entraîne l’envoi des notifications et l’appel des méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) appropriées.</span><span class="sxs-lookup"><span data-stu-id="93849-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="93849-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="93849-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="93849-117">Définissez l MAPI_NO_COINT de sorte que **MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="93849-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="93849-118">Si une structure MAPIINIT_0 est transmise à **MAPIInitialize** avec _ulFlags_ définie sur MAPI_NO_COINIT, MAPI suppose que COM **a** déjà été initialisé et ignore l’appel à **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="93849-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="93849-119">Si MAPI_MULTITHREAD_NOTIFICATIONS’indicateur n’est pas passé, MAPI crée la fenêtre de notification sur le thread qui a été utilisé pour votre premier appel **MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="93849-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="93849-120">MAPI crée la fenêtre de notification sur un thread distinct si MAPI_MULTITHREAD_NOTIFICATIONS est transmis : un thread dédié à la gestion des notifications.</span><span class="sxs-lookup"><span data-stu-id="93849-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="93849-121">MAPI attend du thread utilisé pour créer la fenêtre de notification masquée :</span><span class="sxs-lookup"><span data-stu-id="93849-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="93849-122">Avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="93849-122">Have a message loop.</span></span>
    
- <span data-ttu-id="93849-123">Restez débloqué tout au long de la durée de vie de la session.</span><span class="sxs-lookup"><span data-stu-id="93849-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="93849-124">Avoir une durée de vie plus longue que tout autre thread créé par votre client.</span><span class="sxs-lookup"><span data-stu-id="93849-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="93849-125">Vous pouvez choisir le fil de discussion utilisé en fixant un indicateur dans le premier **appel MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="93849-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="93849-126">Le risque de permettre à l’un de vos threads de gérer les notifications est que si le thread disparaît, la fenêtre de notification est détruite et les notifications ne peuvent plus être envoyées à aucun de vos autres threads.</span><span class="sxs-lookup"><span data-stu-id="93849-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="93849-127">En outre, un traitement spécial peut être nécessaire pour contrôler la distribution des messages de notification publiés dans la file d’attente de messages de la fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="93849-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="93849-128">Si vous utilisez une fenêtre distincte pour gérer les notifications, soyez certain que les notifications apparaîtront au moment approprié sur un thread approprié.</span><span class="sxs-lookup"><span data-stu-id="93849-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="93849-129">Vous n’aurez pas besoin de code spécial pour vérifier et traiter les messages Windows publiés dans la fenêtre de notification.</span><span class="sxs-lookup"><span data-stu-id="93849-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="93849-130">MAPI recommande que les types d’applications clientes suivants utilisent un thread distinct pour créer la fenêtre masquée pour la prise en charge des notifications :</span><span class="sxs-lookup"><span data-stu-id="93849-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="93849-131">Tous les clients multithread.</span><span class="sxs-lookup"><span data-stu-id="93849-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="93849-132">Services Windows à thread unique et applications console Win32.</span><span class="sxs-lookup"><span data-stu-id="93849-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="93849-133">Clients à thread unique qui n’ont pas besoin d’utiliser leur thread principal pour la notification.</span><span class="sxs-lookup"><span data-stu-id="93849-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="93849-134">Pour utiliser l’approche de thread distincte, appelez **MAPIInitialize** sur chaque thread, en MAPI_MULTITHREAD_NOTIFICATIONS’indicateur.</span><span class="sxs-lookup"><span data-stu-id="93849-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="93849-135">Seul le premier appel d’un client à **MAPIInitialize** entraîne la création d’une fenêtre masquée pour prendre en charge les notifications.</span><span class="sxs-lookup"><span data-stu-id="93849-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="93849-136">Les appels suivants entraînent uniquement l’incrémentation d’un nombre de références.</span><span class="sxs-lookup"><span data-stu-id="93849-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

