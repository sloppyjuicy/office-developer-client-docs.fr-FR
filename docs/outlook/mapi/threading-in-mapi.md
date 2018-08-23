---
title: Threading dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d9ee45ea7a3592a2b0fc0675bbdb6e640f9bd046
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580389"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="4d9ac-103">Threading dans MAPI</span><span class="sxs-lookup"><span data-stu-id="4d9ac-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="4d9ac-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d9ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d9ac-105">Un thread est l’entité de base à laquelle un système d’exploitation alloue du temps processeur.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="4d9ac-106">Un thread a ses propres registres, pile, priorité et stockage, mais partage un adresse espace et traiter les ressources telles que des jetons d’accès.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="4d9ac-107">Threads partagent également la mémoire, avec un seul thread lecture qu’un autre thread qu’il a écrite.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="4d9ac-108">Clients MAPI utilisent les modèles de thread génériques suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="4d9ac-109">**Modèle de thread**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-109">**Threading model**</span></span>|<span data-ttu-id="4d9ac-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d9ac-111">Modèle de thread unique</span><span class="sxs-lookup"><span data-stu-id="4d9ac-111">Single threading model</span></span>  <br/> |<span data-ttu-id="4d9ac-112">Tous les objets sont utilisés sur le thread unique.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="4d9ac-113">Modèle de thread Apartment</span><span class="sxs-lookup"><span data-stu-id="4d9ac-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="4d9ac-114">Un objet peut être utilisé uniquement sur le thread qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="4d9ac-115">Modèle de threading gratuite ou thread tiers</span><span class="sxs-lookup"><span data-stu-id="4d9ac-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="4d9ac-116">Un objet peut être utilisé sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="4d9ac-117">MAPI utilise le modèle de thread libre, prise en charge des objets thread-safe qui peuvent être utilisés sur n’importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="4d9ac-118">OLE utilise le modèle de thread de cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="4d9ac-119">Le modèle de thread apartment prend en charge les objets qui doivent être transférés explicitement lorsqu’un thread différent de celui qui a créé l’objet doit utiliser cet objet.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="4d9ac-120">Le mécanisme OLE utilise pour transférer des objets à partir d’un thread à l’autre est appelé marshaling.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="4d9ac-121">Le marshaling implique un objet stub et un objet proxy.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="4d9ac-122">Ces objets spéciaux empaqueter les paramètres de l’interface de l’objet à remarshaler, de transférer ces paramètres à l’autre thread et les décompresser à l’arrivée.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="4d9ac-123">Conflit entre les deux modèles multithreads se produit lorsqu’un objet MAPI libre de threads est envoyé à un autre processus utilisant OLE « léger » appel de procédure distante ou LRPC.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="4d9ac-124">LRPC change la sémantique de l’objet de modèle de thread libre à cloisonnement des threads par interposing interfaces stub et proxy avec apartment threading comportement entre l’objet et son appelant.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="4d9ac-125">Présentation des situations MAPI conduire à ce conflit peut aider les clients et fournisseurs de services éviter des problèmes.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="4d9ac-126">Un objet MAPI est accessible :</span><span class="sxs-lookup"><span data-stu-id="4d9ac-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="4d9ac-127">Via des appels directs à ses méthodes à l’aide d’une interface pointeur renvoyé par un fournisseur de services ou MAPI liée au processus du client, tel que l’objet session retournée à partir de [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="4d9ac-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="4d9ac-128">Par le biais des appels indirects à ses méthodes à l’aide d’un pointeur d’interface retourné par n’importe quel fournisseur de services, comme l’objet folder copiés à partir d’un autre dossier dans [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="4d9ac-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="4d9ac-129">Via une fonction de rappel, telles que la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) passée à un fournisseur de services MAPI ou un appel **Advise** ou les méthodes qui peuvent afficher la progression sur une longue opération.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

