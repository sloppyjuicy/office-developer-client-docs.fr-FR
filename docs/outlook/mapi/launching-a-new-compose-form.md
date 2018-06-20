---
title: Lancer un nouveau formulaire de composition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8d1b94c70e4de6310d2e84cf002c4e3199fced2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784531"
---
# <a name="launching-a-new-compose-form"></a>Lancer un nouveau formulaire de composition

  
  
**S’applique à**: Outlook 
  
L’implémentation de formulaire serveur doit attendre la séquence suivante d’appels de méthode à leur serveur de formulaire et les objets de formulaire lorsqu’une application cliente ouvre un nouveau message pour composer :
  
1. L’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour obtenir des informations de classe à propos de la classe de message du formulaire serveur. 
    
2. L’application cliente appelle [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) pour obtenir un nouvel objet de formulaire. 
    
3. Le Gestionnaire de formulaire MAPI charge le serveur de formulaire, s’il n’est pas déjà en mémoire et obtient une interface [IMAPIForm](imapiformiunknown.md) à partir du serveur du formulaire. 
    
4. L’application cliente prend l’interface **IMAPIForm** qui en résulte et appelle la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) pour obtenir [IPersistMessage](ipersistmessageiunknown.md) interface l’objet. 
    
5. L’application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) pour associer l’objet form [IMessage](imessageimapiprop.md), contexte de vue et objets de récepteur de notification.
    
6. L’application cliente appelle la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) pour appeler le verbe open. 
    
## <a name="see-also"></a>Voir aussi



[Formulaire serveur Interactions](form-server-interactions.md)

