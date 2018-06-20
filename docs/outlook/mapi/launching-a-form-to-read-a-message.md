---
title: Lancement d’un formulaire pour lire un Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784518"
---
# <a name="launching-a-form-to-read-a-message"></a>Lancement d’un formulaire pour lire un Message

  
  
**S’applique à**: Outlook 
  
L’implémentation de formulaire serveur doit attendre la séquence suivante d’appels de méthode à leur serveur du formulaire et les objets de formulaire lorsqu’une application cliente charge un message :
  
1. L’application cliente ouvre le Gestionnaire de formulaire avec un appel à la fonction [MAPIOpenFormMgr](mapiopenformmgr.md) . 
    
2. L’application cliente appelle la méthode [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , qui renvoie un objet avec [IMAPIForm](imapiformiunknown.md). Le Gestionnaire de formulaire peut-être être annulée maintenant s’il ne doit pas être utilisé pour des activations de formulaire. Notez qu’un appel à **LoadForm** peut prendre du temps car le Gestionnaire de formulaire peut-être installer des fichiers exécutables du serveur de formulaire avant de continuer. 
    
3. Le cas échéant, l’application cliente peut préparer [IMAPIViewContext](imapiviewcontextiunknown.md) opérations de contrôle qui peuvent entraîner l’objet de formulaire pour charger le message précédent ou suivant dans le dossier. L’application cliente peut utiliser la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) pour modifier le contexte d’affichage par défaut qui a été défini lors de l’appel **LoadForm** . 
    
4. L’application cliente appelle la méthode [IPersistMessage::Load](ipersistmessage-load.md) pour charger les données de message dans l’objet form. 
    
5. L’application cliente appelle [IMAPIForm::DoVerb](imapiform-doverb.md) pour appeler le verbe open, en passant le pointeur d’interface [IMAPIViewContext](imapiviewcontextiunknown.md) facultatif. 
    
## <a name="see-also"></a>Voir aussi



[Formulaire serveur Interactions](form-server-interactions.md)

