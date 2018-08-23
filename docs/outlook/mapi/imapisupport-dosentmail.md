---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 82490dbe597ebd3f7198aa7e0c904a10202ecd77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568209"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Traite un message envoy�.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpMessage_
  
> [in] Pointeur vers le message ouvert pour lequel un message doit �tre g�n�r� dans le dossier d�sign� pour contenir les �l�ments envoy�s.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.
  
 **DoSentMail** effectue les t�ches suivantes : 
  
- Vérifie le message de la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) déterminer si le message doit être supprimé après son envoi.
    
- D�termine l'emplacement du dossier �l�ments envoy�s.
    
- Lance le raccordement de message pour n'importe quel hooks d�finies sur le dossier �l�ments envoy�s de traitement.
    
- D�place le message vers le dossier �l�ments envoy�s, �l�ments supprim�s, dossier, ou vers un autre dossier.
    
- Publie le message.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[Propri�t� canonique PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

