---
title: Threading dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405540"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="7138a-103">Threading dans MAPI</span><span class="sxs-lookup"><span data-stu-id="7138a-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="7138a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7138a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7138a-105">Un thread est l’entité de base à laquelle un système d’exploitation alloue du temps processeur.</span><span class="sxs-lookup"><span data-stu-id="7138a-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="7138a-106">Un thread possède ses propres registres, pile, priorité et stockage, mais partage un espace d’adressaton et des ressources de processus telles que les jetons d’accès.</span><span class="sxs-lookup"><span data-stu-id="7138a-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="7138a-107">Les threads partagent également la mémoire, avec un thread lisant ce qu’un autre thread a écrit.</span><span class="sxs-lookup"><span data-stu-id="7138a-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="7138a-108">Les clients MAPI utilisent les modèles de thread génériques suivants.</span><span class="sxs-lookup"><span data-stu-id="7138a-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="7138a-109">**Modèle de thread**</span><span class="sxs-lookup"><span data-stu-id="7138a-109">**Threading model**</span></span>|<span data-ttu-id="7138a-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="7138a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7138a-111">Modèle de thread unique</span><span class="sxs-lookup"><span data-stu-id="7138a-111">Single threading model</span></span>  <br/> |<span data-ttu-id="7138a-112">Tous les objets sont utilisés sur le thread unique.</span><span class="sxs-lookup"><span data-stu-id="7138a-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="7138a-113">Modèle de threads de threads d’appart</span><span class="sxs-lookup"><span data-stu-id="7138a-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="7138a-114">Un objet ne peut être utilisé que sur le thread qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="7138a-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="7138a-115">Modèle de thread gratuit ou de thread-party</span><span class="sxs-lookup"><span data-stu-id="7138a-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="7138a-116">Un objet peut être utilisé sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="7138a-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="7138a-117">MAPI utilise le modèle de thread gratuit, qui prend en charge les objets thread-safe qui peuvent être utilisés sur n’importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="7138a-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="7138a-118">OLE utilise le modèle de threads de threads de threads.</span><span class="sxs-lookup"><span data-stu-id="7138a-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="7138a-119">Le modèle de threads en mode apartment prend en charge les objets qui doivent être explicitement transférés lorsqu’un thread autre que celui qui a créé l’objet doit utiliser cet objet.</span><span class="sxs-lookup"><span data-stu-id="7138a-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="7138a-120">Le mécanisme utilisé par OLE pour transférer des objets d’un thread à un autre est appelé marshaling.</span><span class="sxs-lookup"><span data-stu-id="7138a-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="7138a-121">Le marshaling implique un objet stub et un objet proxy.</span><span class="sxs-lookup"><span data-stu-id="7138a-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="7138a-122">Ces objets spéciaux packagent les paramètres de l’interface dans l’objet à marshaler, transfèrent ces paramètres à l’autre thread et les déballent à l’arrivée.</span><span class="sxs-lookup"><span data-stu-id="7138a-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="7138a-123">Un conflit entre les deux modèles multithread survient lorsqu’un objet MAPI de thread libre est envoyé à un autre processus à l’aide de l’appel de procédure distante OLE « léger » ou LRPC.</span><span class="sxs-lookup"><span data-stu-id="7138a-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="7138a-124">LRPC modifie la sémantique de l’objet de threads libres en threads de threads en threads de threads en interposant les interfaces stub et proxy avec le comportement de thread de thread entre l’objet et son appelant.</span><span class="sxs-lookup"><span data-stu-id="7138a-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="7138a-125">La prise en compte des situations dans MAPI qui entraînent ce conflit peut aider les clients et les fournisseurs de services à éviter les problèmes.</span><span class="sxs-lookup"><span data-stu-id="7138a-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="7138a-126">Un objet MAPI est accessible :</span><span class="sxs-lookup"><span data-stu-id="7138a-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="7138a-127">Via des appels directs à ses méthodes à l’aide d’un pointeur d’interface renvoyé par un fournisseur de services ou MAPI lié au processus du client, tel que l’objet de session renvoyé par [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="7138a-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="7138a-128">Via des appels indirects à ses méthodes à l’aide d’un pointeur d’interface renvoyé par n’importe quel fournisseur de services, tel que l’objet dossier copié à partir d’un autre dossier dans [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="7138a-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="7138a-129">Par le biais d’une fonction de rappel, telle que la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) transmise à un fournisseur de services ou à MAPI dans un appel de conseil ou aux méthodes qui peuvent indiquer la progression d’une longue opération. </span><span class="sxs-lookup"><span data-stu-id="7138a-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

