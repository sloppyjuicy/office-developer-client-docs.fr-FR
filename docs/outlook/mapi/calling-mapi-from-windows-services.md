---
title: L’appel MAPI à partir des Services Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6465b2d24c3a38da40f2d1e6df79c2fa256b64b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782988"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="72d14-103">L’appel MAPI à partir des Services Windows</span><span class="sxs-lookup"><span data-stu-id="72d14-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="72d14-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72d14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72d14-105">Pour activer les applications clientes MAPI qui sont enregistrées en tant que services Windows pour fonctionner avec des fournisseurs de services compatible MAPI, MAPI impose plusieurs limitations et exigences.</span><span class="sxs-lookup"><span data-stu-id="72d14-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="72d14-106">Clients MAPI ont les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="72d14-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="72d14-107">Ils ne peuvent pas autoriser une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="72d14-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="72d14-108">Ils peuvent envoyer des messages uniquement par le biais d’une banque de messages étroitement couplés et de transport fournisseur.</span><span class="sxs-lookup"><span data-stu-id="72d14-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="72d14-109">En outre, les clients MAPI peuvent envoyer et recevoir des messages à l’aide uniquement le serveur Microsoft Exchange ou un autre fournisseur de transport sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="72d14-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="72d14-110">En raison de problèmes de sécurité et l’identité entre les applications clientes et le spouleur MAPI, la plupart des fournisseurs de transport ne sont pas pris en charge dans un service.</span><span class="sxs-lookup"><span data-stu-id="72d14-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="72d14-111">Toutes les applications clientes MAPI, si elles sont implémentées en tant que services Windows, doivent appeler la fonction [exécuter MAPIInitialize](mapiinitialize.md) pour initialiser les bibliothèques de MAPI.</span><span class="sxs-lookup"><span data-stu-id="72d14-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="72d14-112">Un appel à la fonction [OleInitialize](http://msdn.microsoft.com/fr-fr/library/ms690134%28v=VS.85%29.aspx) est également nécessaire d’utiliser les bibliothèques OLE.</span><span class="sxs-lookup"><span data-stu-id="72d14-112">A call to the [OleInitialize](http://msdn.microsoft.com/fr-fr/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="72d14-113">[Exécuter MAPIInitialize](mapiinitialize.md) et [OleInitialize](http://msdn.microsoft.com/fr-fr/library/ms690134%28v=VS.85%29.aspx) émettre des appels à la fonction [CoInitialize](http://msdn.microsoft.com/fr-fr/library/ms678543%28VS.85%29.aspx) pour initialiser les bibliothèques de composant COM (Object Model).</span><span class="sxs-lookup"><span data-stu-id="72d14-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](http://msdn.microsoft.com/fr-fr/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](http://msdn.microsoft.com/fr-fr/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="72d14-114">Les clients services doivent définir un indicateur spécial, MAPI_NT_SERVICE, dans le membre **ulFlags** de la structure [MAPIINIT_0](mapiinit_0.md) qui est passé à [exécuter MAPIInitialize](mapiinitialize.md) et dans le paramètre _ulFlags_ qui est transmis à la [MAPILogonEx](mapilogonex.md) fonction pour informer les MAPI de leur implémentation spéciale.</span><span class="sxs-lookup"><span data-stu-id="72d14-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="72d14-115">Clients MAPI qui sont écrites en tant que services Windows et écrits avec l’interface client MAPI ont une exigence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="72d14-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="72d14-116">Ils doivent définir l’indicateur MAPI_NO_MAIL dans l’appel de [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="72d14-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="72d14-117">Autres types de clients n’ont pas de définir un indicateur d’ouverture de session, car elle est automatiquement définie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="72d14-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="72d14-118">Pour gérer les messages dans un thread d’initialisation, un client MAPI qui est implémenté en tant que service effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="72d14-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="72d14-119">Appelle la fonction [MsgWaitForMultipleObjects](http://msdn.microsoft.com/fr-fr/library/ms684242%28VS.85%29.aspx) lorsque les blocs de thread principal.</span><span class="sxs-lookup"><span data-stu-id="72d14-119">Calls the [MsgWaitForMultipleObjects](http://msdn.microsoft.com/fr-fr/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="72d14-120">Appelle la séquence [GetMessage](http://msdn.microsoft.com/fr-fr/library/ms644936%28VS.85%29.aspx) [TranslateMessage](http://msdn.microsoft.com/fr-fr/library/ms644955%28VS.85%29.aspx)et à [DispatchMessage](http://msdn.microsoft.com/fr-fr/library/ms644934%28VS.85%29.aspx) des fonctions de Windows pour gérer le message lorsque [MsgWaitForMultipleObjects](http://msdn.microsoft.com/fr-fr/library/ms684242%28VS.85%29.aspx) renvoie la somme de la valeur du paramètre _nCount_ et valeur de **WAIT_OBJECT_0**, ce qui indique qu’un message est dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="72d14-120">Calls the [GetMessage](http://msdn.microsoft.com/fr-fr/library/ms644936%28VS.85%29.aspx), [TranslateMessage](http://msdn.microsoft.com/fr-fr/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](http://msdn.microsoft.com/fr-fr/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](http://msdn.microsoft.com/fr-fr/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72d14-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d14-121">See also</span></span>



[<span data-ttu-id="72d14-122">Exécuter MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="72d14-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="72d14-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="72d14-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="72d14-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="72d14-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="72d14-125">Problèmes d’environnement d’exploitation</span><span class="sxs-lookup"><span data-stu-id="72d14-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

