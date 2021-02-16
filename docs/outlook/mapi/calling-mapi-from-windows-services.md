---
title: Appel de MAPI à partir de Windows Services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318103"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="153ce-103">Appel de MAPI à partir de Windows Services</span><span class="sxs-lookup"><span data-stu-id="153ce-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="153ce-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="153ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="153ce-105">Pour permettre aux applications clientes MAPI écrites en tant que services Windows de fonctionner avec des fournisseurs de services conformes MAPI, MAPI impose plusieurs limitations et exigences.</span><span class="sxs-lookup"><span data-stu-id="153ce-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="153ce-106">Les clients MAPI ont les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="153ce-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="153ce-107">Ils ne peuvent pas autoriser une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="153ce-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="153ce-108">Ils peuvent envoyer des messages uniquement par le biais d’un fournisseur de transport et d’une magasin de messages étroitement couplés.</span><span class="sxs-lookup"><span data-stu-id="153ce-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="153ce-109">En outre, les clients MAPI peuvent envoyer et recevoir des messages en utilisant uniquement le Microsoft Exchange Server ou un autre fournisseur de transport basé sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="153ce-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="153ce-110">En raison de problèmes d’identité et de sécurité entre les applications clientes et lepooler MAPI, la plupart des fournisseurs de transport ne sont pas pris en charge dans un service.</span><span class="sxs-lookup"><span data-stu-id="153ce-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="153ce-111">Toutes les applications clientes MAPI, qu’elles soient implémentées en tant que services Windows, doivent appeler la fonction [MAPIInitialize](mapiinitialize.md) pour initialiser les bibliothèques MAPI.</span><span class="sxs-lookup"><span data-stu-id="153ce-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="153ce-112">Un appel à la [fonction OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) est également nécessaire pour utiliser les bibliothèques OLE.</span><span class="sxs-lookup"><span data-stu-id="153ce-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="153ce-113">[MAPIInitialize](mapiinitialize.md) et [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) appellent la fonction [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) pour initialiser les bibliothèques COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="153ce-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="153ce-114">Les clients qui sont des services doivent définir un indicateur spécial, MAPI_NT_SERVICE, dans le membre **ulFlags** de la structure MAPIINIT_0 qui [est](mapiinit_0.md) transmis à [MAPIInitialize](mapiinitialize.md) et dans le paramètre  _ulFlags_ qui est transmis à la fonction [MAPILogonEx](mapilogonex.md) pour informer MAPI de leur implémentation spéciale.</span><span class="sxs-lookup"><span data-stu-id="153ce-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="153ce-115">Les clients MAPI écrits en tant que services Windows et écrits avec l’interface cliente MAPI ont une exigence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="153ce-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="153ce-116">Ils doivent définir l’MAPI_NO_MAIL dans l’appel à [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="153ce-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="153ce-117">Les autres types de clients n’ont pas à définir d’indicateur pour l’accès, car il est automatiquement définie par MAPI.</span><span class="sxs-lookup"><span data-stu-id="153ce-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="153ce-118">Pour gérer les messages dans un thread d’initialisation, un client MAPI implémenté en tant que service :</span><span class="sxs-lookup"><span data-stu-id="153ce-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="153ce-119">Appelle la [fonction MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) lorsque le thread principal se bloque.</span><span class="sxs-lookup"><span data-stu-id="153ce-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="153ce-120">Appelle la [séquence getMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)et [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) des fonctions Windows pour gérer le message lorsque [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) renvoie la somme de la valeur du paramètre  _nCount_ et la valeur de **WAIT_OBJECT_0**, qui indique qu’un message est dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="153ce-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="153ce-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="153ce-121">See also</span></span>



[<span data-ttu-id="153ce-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="153ce-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="153ce-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="153ce-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="153ce-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="153ce-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="153ce-125">Problèmes de l’environnement d’exploitation</span><span class="sxs-lookup"><span data-stu-id="153ce-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

