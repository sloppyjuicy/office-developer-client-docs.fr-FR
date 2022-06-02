---
title: IMsgStoreAbortSubmit
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMsgStore AbortSubmit, qui tente de supprimer un message de la file d’attente sortante.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
ms.openlocfilehash: 939e5cc640f3188e70a6379419f9364d931e174d
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828072"
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

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du message à supprimer de la file d’attente sortante. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été supprimé avec succès de la file d’attente sortante.
    
MAPI_E_NOT_IN_QUEUE 
  
> Le message identifié par  _lpEntryID_ ne se trouve plus dans la file d’attente sortante du magasin de messages, généralement parce qu’il a déjà été envoyé. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Le message identifié par  _lpEntryID_ est verrouillé par le spouleur MAPI et l’opération ne peut pas être abandonnée. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::AbortSubmit** tente de supprimer un message envoyé de la file d’attente sortante du magasin de messages. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Une fois qu’un message est envoyé, l’abandon de la soumission en appelant **AbortSubmit** est la seule action qui peut être effectuée sur le message. Ne vous attendez pas à **ce que AbortSubmit** réussisse toujours. Selon la façon dont le système de messagerie sous-jacent est implémenté, il peut ne pas être possible d’annuler l’envoi du message. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI utilise la méthode **IMsgStore::AbortSubmit** pour abandonner la soumission du message sélectionné. |
   
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

