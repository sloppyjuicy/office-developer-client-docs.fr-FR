---
title: Appel de MAPI à partir de services Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385577"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="1e496-103">Appel de MAPI à partir de services Windows</span><span class="sxs-lookup"><span data-stu-id="1e496-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="1e496-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e496-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e496-105">Pour activer les applications clientes MAPI qui sont enregistrées en tant que services Windows pour fonctionner avec des fournisseurs de services compatible MAPI, MAPI impose plusieurs limitations et exigences.</span><span class="sxs-lookup"><span data-stu-id="1e496-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="1e496-106">Clients MAPI ont les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e496-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="1e496-107">Ils ne peuvent pas autoriser une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e496-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="1e496-108">Ils peuvent envoyer des messages uniquement par le biais d’une banque de messages étroitement couplés et de transport fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1e496-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="1e496-109">En outre, les clients MAPI peuvent envoyer et recevoir des messages à l’aide uniquement le serveur Microsoft Exchange ou un autre fournisseur de transport sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1e496-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="1e496-110">En raison de problèmes de sécurité et l’identité entre les applications clientes et le spouleur MAPI, la plupart des fournisseurs de transport ne sont pas pris en charge dans un service.</span><span class="sxs-lookup"><span data-stu-id="1e496-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="1e496-111">Toutes les applications clientes MAPI, si elles sont implémentées en tant que services Windows, doivent appeler la fonction [exécuter MAPIInitialize](mapiinitialize.md) pour initialiser les bibliothèques de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e496-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="1e496-112">Un appel à la fonction [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) est également nécessaire d’utiliser les bibliothèques OLE.</span><span class="sxs-lookup"><span data-stu-id="1e496-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="1e496-113">[Exécuter MAPIInitialize](mapiinitialize.md) et [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) émettre des appels à la fonction [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) pour initialiser les bibliothèques de composant COM (Object Model).</span><span class="sxs-lookup"><span data-stu-id="1e496-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="1e496-114">Les clients services doivent définir un indicateur spécial, MAPI_NT_SERVICE, dans le membre **ulFlags** de la structure [MAPIINIT_0](mapiinit_0.md) qui est passé à [exécuter MAPIInitialize](mapiinitialize.md) et dans le paramètre _ulFlags_ qui est transmis à la [MAPILogonEx](mapilogonex.md) fonction pour informer les MAPI de leur implémentation spéciale.</span><span class="sxs-lookup"><span data-stu-id="1e496-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="1e496-115">Clients MAPI qui sont écrites en tant que services Windows et écrits avec l’interface client MAPI ont une exigence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1e496-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="1e496-116">Ils doivent définir l’indicateur MAPI_NO_MAIL dans l’appel de [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="1e496-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="1e496-117">Autres types de clients n’ont pas de définir un indicateur d’ouverture de session, car elle est automatiquement définie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e496-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="1e496-118">Pour gérer les messages dans un thread d’initialisation, un client MAPI qui est implémenté en tant que service effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e496-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="1e496-119">Appelle la fonction [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) lorsque les blocs de thread principal.</span><span class="sxs-lookup"><span data-stu-id="1e496-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="1e496-120">Appelle la séquence [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)et à [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) des fonctions de Windows pour gérer le message lorsque [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) renvoie la somme de la valeur du paramètre _nCount_ et valeur de **WAIT_OBJECT_0**, ce qui indique qu’un message est dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1e496-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e496-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e496-121">See also</span></span>



[<span data-ttu-id="1e496-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="1e496-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="1e496-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="1e496-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="1e496-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="1e496-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="1e496-125">Problèmes d’environnement d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1e496-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

