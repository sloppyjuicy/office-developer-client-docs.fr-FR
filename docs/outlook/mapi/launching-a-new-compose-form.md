---
title: Lancement d'un nouveau formulaire de composition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270055"
---
# <a name="launching-a-new-compose-form"></a>Lancement d'un nouveau formulaire de composition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les implémenteurs de serveur de formulaire doivent s'attendre à la séquence suivante d'appels de méthode à leurs serveurs de formulaires et à leurs objets de formulaire lorsqu'une application cliente ouvre un nouveau message pour la composition:
  
1. L'application cliente appelle la méthode [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour obtenir des informations de classe sur la classe de message du serveur de formulaire. 
    
2. L'application cliente appelle [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) pour obtenir un nouvel objet Form. 
    
3. Le gestionnaire de formulaires MAPI charge le serveur de formulaires, s'il n'est pas déjà en mémoire, et obtient une interface [IMAPIForm](imapiformiunknown.md) à partir du serveur de formulaire. 
    
4. L'application cliente prend l'interface **IMAPIForm** résultante et appelle la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) pour obtenir l'interface [IPersistMessage](ipersistmessageiunknown.md) de l'objet. 
    
5. L'application cliente appelle la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md) pour associer l'objet formulaire à [IMessage](imessageimapiprop.md), afficher le contexte et conseiller les objets récepteurs.
    
6. L'application cliente appelle la méthode [IMAPIForm::D overb](imapiform-doverb.md) pour appeler le verbe Open. 
    
## <a name="see-also"></a>Voir aussi



[Interactions de serveur de formulaire](form-server-interactions.md)

