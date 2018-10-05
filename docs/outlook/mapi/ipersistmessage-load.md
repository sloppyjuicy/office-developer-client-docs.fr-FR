---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395937"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Charge le formulaire de message spécifié.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Paramètres

 _pMessageSite_
  
> [in] Pointeur vers le site de message pour le formulaire à charger.
    
 _pMessage_
  
> [in] Pointeur vers le message pour lequel le formulaire doit être chargé.
    
 _ulMessageStatus_
  
> [in] Un masque de bits d’indicateurs défini par le client ou défini par le fournisseur, copié à partir de la propriété du message **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)), qui fournissent des informations sur l’état du message.
    
 _ulMessageFlags_
  
> [in] Un masque de bits d’indicateurs, copié à partir de la propriété du message **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), qui fournissent des informations supplémentaires sur l’état du message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a été chargé.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IPersistMessage::Load** pour charger un formulaire pour un message existant. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

 **Charge** est appelé uniquement lorsqu’un formulaire est dans un des états suivants : 
  
- [Non initialisée](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Si une visionneuse de formulaire appelle **charge** lorsque le formulaire est dans un autre état, la méthode renvoie E_UNEXPECTED. 
  
Si votre formulaire comporte une référence à un site de message actif différent de celui qui est passé en **charge**, version du site d’origine, car il sera ne plus être utilisé. Stocker des pointeurs vers le site de message et le message à partir des paramètres _pMessageSite_ et _pMessage_ et appelez des deux objets [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) pour incrémenter son décompte de références. 
  
Une fois terminé, **AddRef** stocker les propriétés des paramètres _ulMessageStatus_ et _ulMessageFlags_ dans le formulaire. Effectuer la transition du formulaire à son état [Normal](normal-state.md) avant de les afficher et informer des visionneuses en appelant leurs méthodes [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Si aucune erreur ne se produire, retournent S_OK. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[État non initialisé](uninitialized-state.md)
  
[État HandsOffAfterSave](handsoffaftersave-state.md)
  
[État HandsOffFromNormal](handsofffromnormal-state.md)
  
[États de formulaire](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

