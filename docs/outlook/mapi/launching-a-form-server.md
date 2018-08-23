---
title: Lancement d’un serveur de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 87299ce4335492a744dd4ee965b4f8b85bcedc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564891"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="4921c-103">Lancement d’un serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="4921c-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="4921c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4921c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4921c-105">La série d’interactions qui se produit lorsqu’un formulaire est chargé à partir d’un stockage persistant (c'est-à-dire, à partir d’une bibliothèque de formulaires) pour afficher un message est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4921c-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="4921c-106">Le client de messagerie Obtient la classe de message du message, indicateurs de message et statut du message.</span><span class="sxs-lookup"><span data-stu-id="4921c-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="4921c-107">Cette étape est facultative ; Si ces éléments de données ne sont pas fournies à l’étape 2, le Gestionnaire de formulaires les récupérer.</span><span class="sxs-lookup"><span data-stu-id="4921c-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="4921c-108">Le client de messagerie appelle [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) avec le message cible.</span><span class="sxs-lookup"><span data-stu-id="4921c-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="4921c-109">Le Gestionnaire de formulaire charge le serveur de formulaire à partir de la bibliothèque de formulaires approprié.</span><span class="sxs-lookup"><span data-stu-id="4921c-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="4921c-110">Si le serveur de formulaire pour le message cible n’est pas installé, le Gestionnaire de formulaire installe les fichiers de formulaire exécutable, ainsi que.</span><span class="sxs-lookup"><span data-stu-id="4921c-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="4921c-111">Le Gestionnaire de formulaire appelle [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l’objet de formulaire pour obtenir l’objet formulaire [IMAPIForm : IUnknown](imapiformiunknown.md) et [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="4921c-111">The form manager calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="4921c-112">Le Gestionnaire de formulaire appelle [IPersistMessage::Load](ipersistmessage-load.md) avec le message d’interfaces de site et le message à partir de l’objet de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="4921c-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="4921c-113">L’objet form rappelle [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) méthode du client messagerie.</span><span class="sxs-lookup"><span data-stu-id="4921c-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="4921c-114">Le Gestionnaire de formulaire appelle la méthode de [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) de l’objet formulaire avec l’interface de contexte d’affichage à partir du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4921c-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="4921c-115">L’objet form rappelle [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) méthode du client messagerie.</span><span class="sxs-lookup"><span data-stu-id="4921c-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="4921c-116">L’objet form rappelle [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) méthode du client messagerie.</span><span class="sxs-lookup"><span data-stu-id="4921c-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="4921c-117">Le client de messagerie appelle méthode [IMAPIForm::Advise](imapiform-advise.md) de l’objet formulaire avec la vue interfaces context à partir de l’objet de la visionneuse et de l’objet de site de message.</span><span class="sxs-lookup"><span data-stu-id="4921c-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="4921c-118">Le client de messagerie appelle la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) de l’objet formulaire.</span><span class="sxs-lookup"><span data-stu-id="4921c-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="4921c-119">L’objet form crée son interface utilisateur, si nécessaire et interagit avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4921c-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4921c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4921c-120">See also</span></span>



[<span data-ttu-id="4921c-121">Interactions avec le serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="4921c-121">Form Server Interactions</span></span>](form-server-interactions.md)

