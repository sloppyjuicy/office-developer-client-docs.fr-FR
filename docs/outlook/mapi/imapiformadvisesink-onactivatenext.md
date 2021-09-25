---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8cf28a3c5b6cdcfc8873a9613ac1fef2b5e7640a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579928"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Masque de bits d’indicateurs définis par le client ou par un fournisseur, copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message suivant à afficher, qui fournit des informations d’état concernant la table des matières dans qui le message est inclus.
    
 _ulMessageFlags_
  
> [in] Pointeur vers un masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message suivant à afficher qui indique l’état actuel du message.
    
 _ppPersistMessage_
  
> [out] Pointeur vers un pointeur vers l’implémentation [IPersistMessage](ipersistmessageiunknown.md) pour l’objet de formulaire utilisé pour le nouveau formulaire, si un nouveau formulaire est requis. Un pointeur vers NULL peut être renvoyé si l’objet de formulaire actuel peut être utilisé pour afficher et enregistrer le message suivant. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi et le formulaire peut gérer le message suivant.
    
S_FALSE 
  
> Le formulaire ne gère pas la classe de message du message suivant.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent la méthode **IMAPIFormAdviseSink::OnActivateNext** pour aider le formulaire à déterminer s’il peut afficher le message suivant dans un dossier. Le message suivant peut être un message de n’importe quelle classe, mais il s’agit généralement de la même classe ou d’une classe associée. Cela rend le processus de lecture de plusieurs messages de la même classe plus efficace en permettant aux applications clientes de réutiliser des objets de formulaire chaque fois que cela est possible. 
  
La plupart des objets de formulaire utilisent la classe de message pointée par le paramètre  _lpszMessageClass_ pour déterminer s’ils peuvent gérer le message suivant. En règle générale, un formulaire peut gérer les messages appartenant à des classes dont la classe par défaut du formulaire est une sous-classe, en plus des messages qui appartiennent à la classe par défaut. Toutefois, un formulaire peut utiliser d’autres facteurs pour déterminer sans doute si un message peut être géré, tel que l’état envoyé ou non envoyé du message suivant. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Renvoyer S_OK null dans le  _paramètre ppPersistMessage_ si le formulaire peut gérer la classe de message. Si le formulaire peut créer un formulaire capable de gérer le message qu’il n’est pas en mesure de gérer, suivez les étapes suivantes : 
  
1. Appelez la fabrique de classes de votre formulaire pour créer une instance d’un nouvel objet de formulaire.
    
2. Stockez cette instance dans le contenu du paramètre de pointeur _ppPersistMessage._ 
    
3. Elles retournent S_OK.
    
La visionneuse de formulaire charge le message à l’aide de la méthode [IPersistMessage::Load](ipersistmessage-load.md) qui appartient à l’objet pointé par  _ppPersistMessage_.
  
Si ni le formulaire ni un formulaire que vous pouvez créer ne peuvent gérer le message suivant, renvoyez S_FALSE. Toutefois, en règle générale, les formulaires ne doivent pas renvoyer cette valeur, car elle entraîne une diminution des performances dans la visionneuse de formulaires.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI utilise la méthode **IMAPIFormAdviseSink::OnActivateNext** pour implémenter la méthode [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

