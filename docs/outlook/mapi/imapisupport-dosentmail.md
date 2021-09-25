---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 296c2df4b3dbee93a54585a932ee06591aecb3aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596070"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Traite un message envoy�.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpMessage_
  
> [in] Pointeur vers le message ouvert pour lequel un message doit �tre g�n�r� dans le dossier d�sign� pour contenir les �l�ments envoy�s.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.
  
 **DoSentMail** effectue les t�ches suivantes : 
  
- Vérifie la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) pour déterminer si le message doit être supprimé après l’envoi.
    
- D�termine l'emplacement du dossier �l�ments envoy�s.
    
- Lance le raccordement de message pour n'importe quel hooks d�finies sur le dossier �l�ments envoy�s de traitement.
    
- D�place le message vers le dossier �l�ments envoy�s, �l�ments supprim�s, dossier, ou vers un autre dossier.
    
- Publie le message.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[Propri�t� canonique PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

