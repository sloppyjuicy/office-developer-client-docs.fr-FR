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
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387726"
---
# <a name="launching-a-form-server"></a>Lancement d’un serveur de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La série d’interactions qui se produit lorsqu’un formulaire est chargé à partir d’un stockage persistant (c'est-à-dire, à partir d’une bibliothèque de formulaires) pour afficher un message est la suivante :
  
1. Le client de messagerie Obtient la classe de message du message, indicateurs de message et statut du message. Cette étape est facultative ; Si ces éléments de données ne sont pas fournies à l’étape 2, le Gestionnaire de formulaires les récupérer.
    
2. Le client de messagerie appelle [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) avec le message cible. 
    
3. Le Gestionnaire de formulaire charge le serveur de formulaire à partir de la bibliothèque de formulaires approprié. Si le serveur de formulaire pour le message cible n’est pas installé, le Gestionnaire de formulaire installe les fichiers de formulaire exécutable, ainsi que.
    
4. Le Gestionnaire de formulaire appelle [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l’objet de formulaire pour obtenir l’objet formulaire [IMAPIForm : IUnknown](imapiformiunknown.md) et [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces. 
    
5. Le Gestionnaire de formulaire appelle [IPersistMessage::Load](ipersistmessage-load.md) avec le message d’interfaces de site et le message à partir de l’objet de la visionneuse. 
    
6. L’objet form rappelle [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) méthode du client messagerie. 
    
7. Le Gestionnaire de formulaire appelle la méthode de [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) de l’objet formulaire avec l’interface de contexte d’affichage à partir du client de messagerie. 
    
8. L’objet form rappelle [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) méthode du client messagerie. 
    
9. L’objet form rappelle [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) méthode du client messagerie. 
    
10. Le client de messagerie appelle méthode [IMAPIForm::Advise](imapiform-advise.md) de l’objet formulaire avec la vue interfaces context à partir de l’objet de la visionneuse et de l’objet de site de message. 
    
11. Le client de messagerie appelle la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) de l’objet formulaire. 
    
12. L’objet form crée son interface utilisateur, si nécessaire et interagit avec l’utilisateur.
    
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaire](form-server-interactions.md)

