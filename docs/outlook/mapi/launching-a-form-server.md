---
title: Lancement d’un serveur de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270048"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="7cbe6-103">Lancement d’un serveur de formulaires</span><span class="sxs-lookup"><span data-stu-id="7cbe6-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="7cbe6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cbe6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cbe6-105">La série d’interactions qui se produit lorsqu’un formulaire est chargé à partir d’un stockage persistant (c’est-à-dire, à partir d’une bibliothèque de formulaires) pour afficher un message est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7cbe6-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="7cbe6-106">Le client de messagerie obtient la classe de message, les indicateurs de message et l’état du message.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="7cbe6-107">Cette étape est facultative . Si ces données ne sont pas fournies à l’étape 2, le gestionnaire de formulaires les récupère.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="7cbe6-108">Le client de messagerie appelle [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) avec le message cible.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="7cbe6-109">Le gestionnaire de formulaire charge le serveur de formulaires à partir de la bibliothèque de formulaires appropriée.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="7cbe6-110">Si le serveur de formulaires du message cible n’est pas installé, le gestionnaire de formulaires installe également les fichiers exécutables du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="7cbe6-111">Le gestionnaire de formulaire appelle [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l’objet de formulaire pour obtenir les interfaces [IMAPIForm : IUnknown](imapiformiunknown.md) et [IPersistMessage : IUnknown](ipersistmessageiunknown.md) de l’objet formulaire.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="7cbe6-112">Le gestionnaire de formulaire appelle [IPersistMessage::Load](ipersistmessage-load.md) avec le site de message et les interfaces de message à partir de l’objet visionneuse.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="7cbe6-113">L’objet formulaire rappelle la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="7cbe6-114">Le gestionnaire de formulaire appelle la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) de l’objet formulaire avec l’interface de contexte d’affichage à partir du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="7cbe6-115">L’objet formulaire rappelle la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="7cbe6-116">L’objet formulaire rappelle la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="7cbe6-117">Le client de messagerie appelle la méthode [IMAPIForm::Advise](imapiform-advise.md) de l’objet formulaire avec les interfaces de contexte d’affichage de l’objet visionneuse et de l’objet de site de message.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="7cbe6-118">Le client de messagerie appelle la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) de l’objet formulaire.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="7cbe6-119">L’objet formulaire crée son interface utilisateur, si nécessaire, et interagit avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cbe6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cbe6-120">See also</span></span>



[<span data-ttu-id="7cbe6-121">Interactions avec le serveur de formulaires</span><span class="sxs-lookup"><span data-stu-id="7cbe6-121">Form Server Interactions</span></span>](form-server-interactions.md)

