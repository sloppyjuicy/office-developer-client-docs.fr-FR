---
title: Lancement d’un nouveau formulaire de composition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391772"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="7e276-103">Lancement d’un nouveau formulaire de composition</span><span class="sxs-lookup"><span data-stu-id="7e276-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="7e276-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e276-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e276-105">L’implémentation de formulaire serveur doit attendre la séquence suivante d’appels de méthode à leur serveur de formulaire et les objets de formulaire lorsqu’une application cliente ouvre un nouveau message pour composer :</span><span class="sxs-lookup"><span data-stu-id="7e276-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="7e276-106">L’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour obtenir des informations de classe à propos de la classe de message du formulaire serveur.</span><span class="sxs-lookup"><span data-stu-id="7e276-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="7e276-107">L’application cliente appelle [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) pour obtenir un nouvel objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7e276-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="7e276-108">Le Gestionnaire de formulaire MAPI charge le serveur de formulaire, s’il n’est pas déjà en mémoire et obtient une interface [IMAPIForm](imapiformiunknown.md) à partir du serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7e276-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="7e276-109">L’application cliente prend l’interface **IMAPIForm** qui en résulte et appelle la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) pour obtenir [IPersistMessage](ipersistmessageiunknown.md) interface l’objet.</span><span class="sxs-lookup"><span data-stu-id="7e276-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="7e276-110">L’application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) pour associer l’objet form [IMessage](imessageimapiprop.md), contexte de vue et objets de récepteur de notification.</span><span class="sxs-lookup"><span data-stu-id="7e276-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="7e276-111">L’application cliente appelle la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) pour appeler le verbe open.</span><span class="sxs-lookup"><span data-stu-id="7e276-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7e276-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e276-112">See also</span></span>



[<span data-ttu-id="7e276-113">Interactions avec le serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="7e276-113">Form Server Interactions</span></span>](form-server-interactions.md)

