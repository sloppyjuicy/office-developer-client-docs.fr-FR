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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414381"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tente de supprimer un message de la file d’attente sortante.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à supprimer de la file d’attente sortante. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été supprimé de la file d’attente sortante.
    
MAPI_E_NOT_IN_QUEUE 
  
> Le message identifié par  _lpEntryID_ ne se trouve plus dans la file d’attente sortante de la boutique de messages, généralement parce qu’il a déjà été envoyé. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Le message identifié par  _lpEntryID_ est verrouillé par lepooler MAPI et l’opération ne peut pas être abandonnée. 
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::AbortSubmit** tente de supprimer un message envoyé de la file d’attente sortante de la boutique de messages. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Une fois qu’un message est envoyé, l’abandon de la soumission en appelant **AbortSubmit** est la seule action qui peut être effectuée sur le message. Ne vous attendez **pas à ce que AbortSubmit** réussisse toujours. Selon la façon dont le système de messagerie sous-jacent est implémenté, il peut être impossible d’annuler l’envoi du message. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI utilise la méthode **IMsgStore::AbortSubmit** pour abandonner l’envoi du message sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

