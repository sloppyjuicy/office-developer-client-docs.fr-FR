---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7e8fb69e7d25420186d7269943c5d957311e813d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581755"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique si le formulaire peut gérer la classe de message du message suivant à afficher.
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Paramètres

 _lpszMessageClass_
  
> [in] Pointeur vers la classe de message du message suivant.
    
 _ulMessageStatus_
  
> [in] Un masque de bits d’indicateurs défini par le client ou défini par le fournisseur, copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message suivant à afficher, qui fournit des informations d’état concernant la table des matières que le message est inclus dans.
    
 _ulMessageFlags_
  
> [in] Un pointeur vers un masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message suivant à afficher qui indique l’état actuel du message.
    
 _ppPersistMessage_
  
> [out] Pointeur vers un pointeur vers l’implémentation de [IPersistMessage](ipersistmessageiunknown.md) pour l’objet de formulaire utilisé pour le nouveau formulaire, si un nouveau formulaire est requis. Un pointeur null peut être obtenue si l’objet de formulaire en cours peut être utilisé pour afficher et enregistrer le message suivant. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La notification a réussi et que le formulaire peut gérer le message suivant.
    
S_FALSE 
  
> Le formulaire ne gère pas la classe de message du message suivant.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormAdviseSink::OnActivateNext** pour déterminer le formulaire s’il peut afficher le message suivant dans un dossier. Le message suivant peut être un message de n’importe quelle classe, mais il est généralement de la même classe ou une classe connexe. Ainsi, le processus de lecture de plusieurs messages de la même classe plus efficace en activant les applications clientes de réutiliser des objets de formulaire chaque fois que possible. 
  
La plupart des objets de formulaire utilise la classe de message indiquée par le paramètre _lpszMessageClass_ pour déterminer si elles peuvent gérer le message suivant. Généralement un formulaire peut gérer les messages qui appartiennent aux classes dont la classe du formulaire par défaut est une sous-classe, en plus des messages qui appartiennent à la classe par défaut. Toutefois, un formulaire peut utiliser autres facteurs pour déterminer sans question si un message peut être géré, telles que l’état envoyé ou en attente du message suivant. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Renvoie S_OK et NULL dans le paramètre _ppPersistMessage_ si le formulaire peut gérer la classe de message. Si le formulaire peut créer un formulaire qui peut gérer le message que le formulaire ne peut pas gérer, procédez comme suit : 
  
1. Appelez la fabrique de classe de votre formulaire pour créer une instance d’un nouvel objet de formulaire.
    
2. Stocker cette instance dans le contenu du paramètre pointeur _ppPersistMessage_ . 
    
3. Elles retournent S_OK.
    
La visionneuse de formulaire chargera le message à l’aide de la méthode [IPersistMessage::Load](ipersistmessage-load.md) qui appartient à l’objet désigné par _ppPersistMessage_.
  
Si le formulaire, ni un formulaire que vous pouvez créer peut gérer le message suivant, renvoie S_FALSE. Toutefois, en règle générale, les formulaires ne doivent pas renvoyer que cette valeur, car il engendre diminue les performances dans la visionneuse de formulaire.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI utilise la méthode **IMAPIFormAdviseSink::OnActivateNext** pour implémenter la méthode [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

