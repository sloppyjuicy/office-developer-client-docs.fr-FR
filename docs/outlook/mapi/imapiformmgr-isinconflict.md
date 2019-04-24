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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321846"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine si un formulaire peut gérer ses propres conflits de messages. Un message est en conflit s'il a été modifié simultanément par plusieurs utilisateurs. Cela peut se produire pour les messages dans les dossiers publics.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Paramètres

 _ulMessageFlags_
  
> dans Pointeur vers un masque de des indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d'un message qui indique l'état actuel du message.
    
 _ulMessageStatus_
  
> dans Masque de bits des indicateurs définis par le client ou par le fournisseur, copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) d'un message qui fournit des informations supplémentaires sur l'état du message.
    
 _szMessageClass_
  
> dans Chaîne qui nomme la classe de message du message.
    
 _pFolderFocus_
  
> dans Pointeur vers le dossier qui contient le message. Le paramètre _pFolderFocus_ peut être null si ce dossier n'existe pas (par exemple, si le message est incorporé dans un autre message). 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire ne gère pas ses propres conflits de messages.
    
S_FALSE 
  
> Le formulaire gère ses propres conflits de messages ou le message pour lequel les informations ont été transmises n'est pas en conflit.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: IsInConflict** pour déterminer si un formulaire particulier ne gère pas ses propres conflits de messages. **IsInConflict** vérifie les masques de transparence dans les paramètres _ulMessageFlags_ et _ulMessageStatus_ pour la présence d'un indicateur de conflit. Si un indicateur de conflit est défini, **IsInConflict** résout la classe de message passée dans le paramètre _SZMESSAGECLASS_ et renvoie S_OK si le formulaire ne gère pas ses propres conflits. **IsInConflict** renvoie S_FALSE si le formulaire gère ses propres conflits. 
  
Un formulaire qui ne gère pas ses propres conflits doit être ouvert à l'aide de la méthode [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) et ne peut pas réutiliser un objet Form existant. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les applications clientes doivent généralement traiter les conflits lorsque les applications se déplacent d'un message vers le message suivant ou précédent dans un dossier. Si un message est en conflit, mais que le serveur de formulaires pour ce message peut gérer les conflits, l'application cliente doit exécuter son code habituel pour afficher le message suivant ou précédent. Si le serveur de formulaire ne peut pas gérer les conflits, l'application cliente doit continuer comme s'il n'était pas conscient de la classe de message du message suivant ou précédent. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

