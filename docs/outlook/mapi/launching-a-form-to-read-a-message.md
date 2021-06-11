---
title: Lancement d’un formulaire pour lire un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425931"
---
# <a name="launching-a-form-to-read-a-message"></a>Lancement d’un formulaire pour lire un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les implémenteurs de serveur de formulaire doivent s’attendre à la séquence suivante d’appels de méthode à leur serveur de formulaires et à leurs objets de formulaire lorsqu’une application cliente charge un message :
  
1. L’application cliente ouvre le gestionnaire de formulaires avec un appel à la [fonction MAPIOpenFormMgr.](mapiopenformmgr.md) 
    
2. L’application cliente appelle [la méthode IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) qui renvoie un objet avec [IMAPIForm](imapiformiunknown.md). Le gestionnaire de formulaires peut être publié maintenant s’il ne sera pas utilisé pour d’autres activations de formulaires. Notez qu’un appel à **LoadForm** peut prendre un certain temps, car le gestionnaire de formulaires peut avoir à installer les fichiers exécutables du serveur de formulaires avant de poursuivre. 
    
3. L’application cliente peut éventuellement préparer [IMAPIViewContext](imapiviewcontextiunknown.md) pour contrôler les opérations qui peuvent entraîner le chargement du message précédent ou suivant dans le dossier par l’objet formulaire. L’application cliente peut utiliser la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) pour modifier le contexte d’affichage par défaut qui a été définie dans **l’appel LoadForm.** 
    
4. L’application cliente appelle [la méthode IPersistMessage::Load](ipersistmessage-load.md) pour charger les données de message dans l’objet de formulaire. 
    
5. L’application cliente appelle [IMAPIForm::D oVerb](imapiform-doverb.md) pour appeler le verbe ouvert, en passant le pointeur d’interface [IMAPIViewContext](imapiviewcontextiunknown.md) facultatif. 
    
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaires](form-server-interactions.md)

