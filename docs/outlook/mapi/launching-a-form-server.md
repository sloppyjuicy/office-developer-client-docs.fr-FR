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
# <a name="launching-a-form-server"></a>Lancement d’un serveur de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La série d’interactions qui se produit lorsqu’un formulaire est chargé à partir d’un stockage persistant (c’est-à-dire, à partir d’une bibliothèque de formulaires) pour afficher un message est la suivante :
  
1. Le client de messagerie obtient la classe de message, les indicateurs de message et l’état du message. Cette étape est facultative . Si ces données ne sont pas fournies à l’étape 2, le gestionnaire de formulaires les récupère.
    
2. Le client de messagerie appelle [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) avec le message cible. 
    
3. Le gestionnaire de formulaire charge le serveur de formulaires à partir de la bibliothèque de formulaires appropriée. Si le serveur de formulaires du message cible n’est pas installé, le gestionnaire de formulaires installe également les fichiers exécutables du formulaire.
    
4. Le gestionnaire de formulaire appelle [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l’objet de formulaire pour obtenir les interfaces [IMAPIForm : IUnknown](imapiformiunknown.md) et [IPersistMessage : IUnknown](ipersistmessageiunknown.md) de l’objet formulaire. 
    
5. Le gestionnaire de formulaire appelle [IPersistMessage::Load](ipersistmessage-load.md) avec le site de message et les interfaces de message à partir de l’objet visionneuse. 
    
6. L’objet formulaire rappelle la méthode [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) du client de messagerie. 
    
7. Le gestionnaire de formulaire appelle la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) de l’objet formulaire avec l’interface de contexte d’affichage à partir du client de messagerie. 
    
8. L’objet formulaire rappelle la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) du client de messagerie. 
    
9. L’objet formulaire rappelle la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) du client de messagerie. 
    
10. Le client de messagerie appelle la méthode [IMAPIForm::Advise](imapiform-advise.md) de l’objet formulaire avec les interfaces de contexte d’affichage de l’objet visionneuse et de l’objet de site de message. 
    
11. Le client de messagerie appelle la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) de l’objet formulaire. 
    
12. L’objet formulaire crée son interface utilisateur, si nécessaire, et interagit avec l’utilisateur.
    
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaires](form-server-interactions.md)

