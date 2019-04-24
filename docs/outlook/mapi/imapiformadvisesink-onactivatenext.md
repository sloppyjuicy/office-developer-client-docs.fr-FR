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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329434"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le formulaire peut gérer la classe de message du prochain message à afficher.
  
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
  
> dans Pointeur vers la classe de message du message suivant.
    
 _ulMessageStatus_
  
> dans Masque de bits des indicateurs définis par le client ou par le fournisseur, copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message suivant à afficher, qui fournit des informations sur l'état de la table de contenu du message. dans.
    
 _ulMessageFlags_
  
> dans Pointeur vers un masque de des indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du prochain message à afficher, qui indique l'état actuel du message.
    
 _ppPersistMessage_
  
> remarquer Pointeur vers un pointeur vers l'implémentation [IPersistMessage](ipersistmessageiunknown.md) pour l'objet Form utilisé pour le nouveau formulaire, si un nouveau formulaire est requis. Un pointeur vers une valeur NULL peut être renvoyé si l'objet de formulaire actif peut être utilisé pour afficher et enregistrer le message suivant. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi et le formulaire peut gérer le message suivant.
    
S_FALSE 
  
> Le formulaire ne gère pas la classe de message du message suivant.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormAdviseSink:: OnActivateNext** pour aider la forme à déterminer si elle peut afficher le message suivant dans un dossier. Le message suivant peut être un message de n'importe quelle classe, mais il s'agit généralement de la même classe ou d'une classe connexe. Le processus de lecture de plusieurs messages de la même classe est ainsi plus efficace en permettant aux applications clientes de réutiliser des objets de formulaire chaque fois que cela est possible. 
  
La plupart des objets Form utiliseront la classe de message désignée par le paramètre _lpszMessageClass_ pour déterminer s'ils peuvent gérer le message suivant. En règle générale, un formulaire peut gérer les messages qui appartiennent à des classes dont la classe par défaut du formulaire est une sous-classe, en plus des messages qui appartiennent à la classe par défaut. Toutefois, un formulaire peut utiliser d'autres facteurs pour déterminer sans question s'il est possible de gérer un message, comme l'état envoyé ou non envoyé du message suivant. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Renvoie S_OK et NULL dans le paramètre _ppPersistMessage_ si le formulaire peut gérer la classe de message. Si le formulaire peut créer un nouveau formulaire qui peut gérer le message que le formulaire ne peut pas gérer, procédez comme suit: 
  
1. Appelez la classe Factory de votre formulaire pour créer une instance d'un nouvel objet Form.
    
2. Stockez cette instance dans le contenu du paramètre de pointeur _ppPersistMessage_ . 
    
3. Elles retournent S_OK.
    
La visionneuse de formulaire chargera le message à l'aide de la méthode [IPersistMessage:: Load](ipersistmessage-load.md) qui appartient à l'objet pointé par _ppPersistMessage_.
  
Si ni le formulaire ni un formulaire que vous pouvez créer ne peuvent gérer le message suivant, renvoyer S_FALSE. Toutefois, en règle générale, les formulaires ne doivent pas renvoyer cette valeur, car cela entraîne une diminution des performances dans la visionneuse de formulaires.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CMyMAPIFormViewer:: ActivateNext,  <br/> |MFCMAPI utilise la méthode **IMAPIFormAdviseSink:: OnActivateNext** pour implémenter la méthode [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md) .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

