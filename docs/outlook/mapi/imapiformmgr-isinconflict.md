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
ms.openlocfilehash: 329771bf79e30f07c9de0a311aa2a836ca507c38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580032"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine si un formulaire peut gérer son propre conflits de message. Un message est en conflit si elle a été modifié simultanément par plusieurs utilisateurs. Cela peut se produire pour les messages dans les dossiers publics.
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Paramètres

 _ulMessageFlags_
  
> [in] Pointeur vers un masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un message qui indique l’état actuel du message.
    
 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs défini par le client ou défini par le fournisseur copiées à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) d’un message qui fournit des informations supplémentaires sur l’état du message.
    
 _szMessageClass_
  
> [in] Chaîne qui nomme la classe de message du message.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient le message. Le paramètre _pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message). 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire ne gère pas les conflits de son propre message.
    
S_FALSE 
  
> Le formulaire gère son propre conflits de message ou le message pour lequel les informations a été passées n’est pas en conflit.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode de **IMAPIFormMgr::IsInConflict** pour détecter si un formulaire particulier ne gère pas sa propre conflits de message. **IsInConflict** vérifie les masques de bits dans les paramètres _ulMessageFlags_ et _ulMessageStatus_ de la présence d’un indicateur de conflit. Si un conflit est défini, **IsInConflict** résout la classe de message transmise dans le paramètre _szMessageClass_ et renvoie S_OK si le formulaire ne gère pas son propre est en conflit. **IsInConflict** renvoie S_FALSE si le formulaire gère son propre est en conflit. 
  
Un formulaire qui ne gère pas sa propre conflits doit être ouverts à l’aide de la méthode [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) et ne peut pas réutiliser un objet de formulaire existant. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Applications clientes ont généralement à traiter les conflits lorsque les applications déplacement d’un message pour le message suivant ou précédent dans un dossier. Si un message est en conflit, mais le serveur de formulaire pour ce message peut gérer des conflits, l’application cliente doit exécuter son code habituel pour afficher le message suivant ou précédent. Si le serveur de formulaire ne peut pas gérer les conflits, l’application cliente doit continuer comme si elle n’a pas connaissance de la classe de message du message suivant ou précédent. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

