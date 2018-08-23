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
ms.openlocfilehash: 66aa5fe08b1c0be3906fa9a0483bbdec37c095c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564499"
---
# <a name="launching-a-new-compose-form"></a>Lancement d’un nouveau formulaire de composition

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’implémentation de formulaire serveur doit attendre la séquence suivante d’appels de méthode à leur serveur de formulaire et les objets de formulaire lorsqu’une application cliente ouvre un nouveau message pour composer :
  
1. L’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour obtenir des informations de classe à propos de la classe de message du formulaire serveur. 
    
2. L’application cliente appelle [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) pour obtenir un nouvel objet de formulaire. 
    
3. Le Gestionnaire de formulaire MAPI charge le serveur de formulaire, s’il n’est pas déjà en mémoire et obtient une interface [IMAPIForm](imapiformiunknown.md) à partir du serveur du formulaire. 
    
4. L’application cliente prend l’interface **IMAPIForm** qui en résulte et appelle la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) pour obtenir [IPersistMessage](ipersistmessageiunknown.md) interface l’objet. 
    
5. L’application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) pour associer l’objet form [IMessage](imessageimapiprop.md), contexte de vue et objets de récepteur de notification.
    
6. L’application cliente appelle la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) pour appeler le verbe open. 
    
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaire](form-server-interactions.md)

