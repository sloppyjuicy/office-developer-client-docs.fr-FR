---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412883"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine si un formulaire peut gérer ses propres conflits de messages. Un message est en conflit s’il a été modifié simultanément par plusieurs utilisateurs. Cela peut se produire pour les messages dans les dossiers publics.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameters

 _ulMessageFlags_
  
> [in] Pointeur vers un masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un message qui indique l’état actuel du message.
    
 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs définis par le client ou par un fournisseur copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) d’un message qui fournit des informations supplémentaires sur l’état du message.
    
 _szMessageClass_
  
> [in] Chaîne qui nomme la classe de message du message.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient le message. Le  _paramètre pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message). 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire ne gère pas ses propres conflits de messages.
    
S_FALSE 
  
> Le formulaire gère ses propres conflits de messages, ou le message pour lequel les informations ont été transmises n’est pas en conflit.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::IsInConflict** pour découvrir si un formulaire particulier ne gère pas ses propres conflits de messages. **IsInConflict** vérifie la présence d’un indicateur de conflit dans les paramètres _ulMessageFlags_ et _ulMessageStatus._ Si un indicateur de conflit est définie, **IsInConflict** résout la classe de message transmise dans le paramètre  _szMessageClass_ et renvoie S_OK si le formulaire ne gère pas ses propres conflits. **IsInConflict** renvoie S_FALSE si le formulaire gère ses propres conflits. 
  
Un formulaire qui ne gère pas ses propres conflits doit être ouvert à l’aide de la méthode [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) et ne peut pas réutiliser un objet de formulaire existant. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les applications clientes doivent généralement gérer les conflits lorsque les applications sont passées d’un message au message suivant ou précédent d’un dossier. Si un message est en conflit, mais que le serveur de formulaires de ce message peut gérer les conflits, l’application cliente doit exécuter son code habituel pour afficher le message suivant ou précédent. Si le serveur de formulaires ne peut pas gérer les conflits, l’application cliente doit continuer comme si elle n’avait pas connaissance de la classe de message du message suivant ou précédent. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

