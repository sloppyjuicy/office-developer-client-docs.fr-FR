---
title: Lancement d’un nouveau formulaire de composition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 29ad3393340d356a043f5df5115b9112d8e3b3df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610355"
---
# <a name="launching-a-new-compose-form"></a>Lancement d’un nouveau formulaire de composition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les implémenteurs de serveur de formulaire doivent s’attendre à ce que la séquence suivante d’appels de méthode soit appliquée à leur serveur de formulaires et à leurs objets de formulaire lorsqu’une application cliente ouvre un nouveau message pour la composition :
  
1. L’application cliente appelle [la méthode IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour obtenir des informations de classe sur la classe de message du serveur de formulaires. 
    
2. L’application cliente appelle [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) pour obtenir un nouvel objet de formulaire. 
    
3. Le gestionnaire de formulaire MAPI charge le serveur de formulaires, s’il n’est pas déjà en mémoire, et obtient une interface [IMAPIForm](imapiformiunknown.md) à partir du serveur de formulaires. 
    
4. L’application cliente prend l’interface **IMAPIForm** qui en résulte et appelle la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) pour obtenir l’interface [IPersistMessage](ipersistmessageiunknown.md) de l’objet. 
    
5. L’application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) pour associer l’objet de formulaire à [IMessage,](imessageimapiprop.md)afficher le contexte et conseiller les objets de type sink.
    
6. L’application cliente appelle [la méthode IMAPIForm::D oVerb](imapiform-doverb.md) pour appeler le verbe ouvert. 
    
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaires](form-server-interactions.md)

