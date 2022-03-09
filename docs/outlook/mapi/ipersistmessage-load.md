---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
ms.openlocfilehash: e972e6c7983afe65a04e5345908fccc6cc29afb5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370364"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Charge le formulaire pour un message spécifié.
  
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
  
> [in] Pointeur vers le site du message pour le formulaire à charger.
    
 _pMessage_
  
> [in] Pointeur vers le message pour lequel le formulaire doit être chargé.
    
 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs définis par le client ou par un fournisseur, copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message, qui fournissent des informations sur l’état du message.
    
 _ulMessageFlags_
  
> [in] Masque de bits d’indicateurs, copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message, qui fournit des informations supplémentaires sur l’état du message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a été chargé avec succès.
    
## <a name="remarks"></a>Remarques

Les visionneuses de **formulaires appellent la méthode IPersistMessage::Load** pour charger un formulaire pour un message existant. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

 **Le** chargement est appelé uniquement lorsqu’un formulaire se trouve dans l’un des états suivants : 
  
- [Nonnitialisé](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Si une visionneuse de formulaire appelle **Load** alors que le formulaire est dans un autre état, la méthode renvoie E_UNEXPECTED. 
  
Si votre formulaire a une référence à un site de messages actif autre que celui qui est transmis à **Load**, release the original site because it will no longer be used. Stockez les pointeurs vers le site de message et le message à partir des paramètres  _pMessageSite_ et  _pMessage_ et appelez les méthodes [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) des deux objets pour incrémenter leur nombre de références. 
  
Une **fois AddRef** terminé, stockez les  _propriétés des paramètres ulMessageStatus_ et  _ulMessageFlags_ dans le formulaire. Transition du formulaire vers son état [Normal](normal-state.md) avant de l’afficher et avertir les visionneuses inscrites en appelant leurs méthodes [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Si aucune erreur ne se produit, renvoyez S_OK. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[État nonnitialisé](uninitialized-state.md)
  
[HandsOffAfterSave, état](handsoffaftersave-state.md)
  
[HandsOffFromNormal State](handsofffromnormal-state.md)
  
[États de formulaire](form-states.md)


[IPersistStorage::Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream::Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile::Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

