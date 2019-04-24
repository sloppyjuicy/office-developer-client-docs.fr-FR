---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348817"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tente de supprimer un message de la file d'attente sortante.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du message à supprimer de la file d'attente sortante. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été supprimé de la file d'attente sortante.
    
MAPI_E_NOT_IN_QUEUE 
  
> Le message identifié par _lpEntryID_ n'est plus dans la file d'attente sortante de la Banque de messages, généralement parce qu'il a déjà été envoyé. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Le message identifié par _lpEntryID_ est verrouillé par le spouleur MAPI et l'opération ne peut pas être abandonnée. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: AbortSubmit** tente de supprimer un message envoyé de la file d'attente sortante de la Banque de messages. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Après l'envoi d'un message, l'abandon de l'envoi en appelant **AbortSubmit** est la seule action pouvant être effectuée sur le message. Ne pas s'attendre à ce que **AbortSubmit** réussisse toujours. En fonction de la façon dont le système de messagerie sous-jacent est implémenté, il se peut que vous ne soyez pas en mesure d'annuler l'envoi du message. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnAbortSubmit  <br/> |MFCMAPI utilise la méthode **IMsgStore:: AbortSubmit** pour abandonner l'envoi du message sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

