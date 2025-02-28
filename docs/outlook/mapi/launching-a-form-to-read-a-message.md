---
title: Lancement d’un formulaire pour lire un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
ms.openlocfilehash: a91ff173d01d707cd5804fd24b3cbca213aaa193
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371253"
---
# <a name="launching-a-form-to-read-a-message"></a>Lancement d’un formulaire pour lire un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les implémenteurs de serveur de formulaire doivent s’attendre à ce que la séquence suivante d’appels de méthode soit appliquée à leur serveur de formulaires et à leurs objets de formulaire lorsqu’une application cliente charge un message :
  
1. L’application cliente ouvre le gestionnaire de formulaires avec un appel à la [fonction MAPIOpenFormMgr](mapiopenformmgr.md) . 
    
2. L’application cliente appelle [la méthode IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , qui renvoie un objet avec [IMAPIForm](imapiformiunknown.md). Le gestionnaire de formulaires peut être publié maintenant s’il ne sera pas utilisé pour d’autres activations de formulaires. Notez qu’un appel à **LoadForm** peut prendre un certain temps, car le gestionnaire de formulaires peut avoir à installer les fichiers exécutables du serveur de formulaires avant de poursuivre. 
    
3. L’application cliente peut éventuellement préparer [IMAPIViewContext](imapiviewcontextiunknown.md) pour contrôler les opérations qui peuvent entraîner le chargement du message précédent ou suivant dans le dossier par l’objet formulaire. L’application cliente peut utiliser la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) pour modifier le contexte d’affichage par défaut qui a été définie dans **l’appel LoadForm** . 
    
4. L’application cliente appelle [la méthode IPersistMessage::Load](ipersistmessage-load.md) pour charger les données de message dans l’objet de formulaire. 
    
5. L’application cliente appelle [IMAPIForm::D oVerb](imapiform-doverb.md) pour appeler le verbe ouvert, en passant le pointeur d’interface [IMAPIViewContext](imapiviewcontextiunknown.md) facultatif. 
    
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaires](form-server-interactions.md)

