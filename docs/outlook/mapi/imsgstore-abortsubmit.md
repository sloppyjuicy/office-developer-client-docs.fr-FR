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
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784253"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**S’applique à**: Outlook 
  
Tente de supprimer un message de la file d’attente sortante.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à supprimer de la file d’attente sortante. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le message a été supprimé de la file d’attente sortante.
    
MAPI_E_NOT_IN_QUEUE 
  
> Le message identifié par _lpEntryID_ n’est plus dans la file d’attente de la banque de messages sortants, en règle générale, car il a déjà été envoyé. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Le message identifié par _lpEntryID_ est verrouillé par le spouleur MAPI, et l’opération ne peut pas être annulée. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::AbortSubmit** tente de supprimer un message envoyé à partir de la file d’attente sortante de la banque de messages. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Une fois un message est envoyé, abandon de l’envoi en appelant **AbortSubmit** est la seule action peut être effectuée sur le message. Ne pensez pas **AbortSubmit** réussissent toujours. Selon la façon dont le système de messagerie sous-jacent est implémenté, il est parfois pas possible d’annuler l’envoi du message. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI utilise la méthode **IMsgStore::AbortSubmit** pour annuler l’envoi du message sélectionné.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

